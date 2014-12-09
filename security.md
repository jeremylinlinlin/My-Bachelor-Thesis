# 系统安全性

## 简介

网页程序框架的作用是帮助开发者构建网页程序。有些框架还能增强网页程序的安全性。其实框架之间无所谓谁更安全，只要使用得当，就能开发出安全的程序。Rails 提供了很多智能的帮助方法，例如避免 SQL 注入的方法，可以避免常见的安全隐患。

网页程序面对的威胁包括：窃取账户，绕开访问限制，读取或修改敏感数据，显示欺诈内容。攻击者有可能还会安装木马程序或者来路不明的邮件发送程序，用于获取经济利益，或者修改公司资源，破坏企业形象。

## 跨站请求伪造

跨站请求伪造（cross-site request forgery，简称 CSRF）攻击的方法是在页面中包含恶意代码或者链接，攻击者认为被攻击的用户有权访问另一个网站。如果用户在那个网站的会话没有过期，攻击者就能执行未经授权的操作。简单的例子如：
* 小强访问一个留言板，其中有篇由黑客发布的帖子，包含一个精心制造的 HTML 图片元素。这个元素指向 小强的项目管理程序中的某个操作，而不是真正的图片文件。
* 图片元素的代码为 <img src="http://www.xiaoqiang.com/project/1/destroy">。
* 小强在 www.xiaoqiang.com 网站上的会话还有效，因为他并没有退出。
* 查看这篇帖子后，浏览器发现有个图片标签，尝试从 www.xiaoqiang.com 加载这个可疑的图片。如前所述，浏览器会同时发送 cookie，其中就包含可用的会话 ID。
* www.xiaoqiang.com 验证了会话中的用户信息，销毁 ID 为 1 的项目。请求得到的响应页面浏览器无法解析，因此不会显示图片。
* 小强并未察觉到被攻击了，一段时间后才发现 ID 为 1 的项目不见了。

为了防止这种伪造请求，Rails 增加了安全权标的使用，这个权标只有自己的网站知道，其他网站不知道。我们要在请求中加入这个权标，且要在服务器上做验证。在 Rails 中， 我们只需在全局控制器 application_controller.rb 中加入一行

    protect_from_forgery

加入这行代码后，Rails 生成的所有表单和 Ajax 请求中都会包含安全权标。如果安全权标和预期的值不一样，程序会重置会话。

## Mass Assignment

Mass Assignment 是个 Rails 的一个专属。因为 Rails 的各种操作太方便而造成的安全性议题。Active Record 对象在新建或修改时，可以直接传入一个 Hash 来设定属性(这一功能叫做 Mass Assignment)：

    def create
      params[:user] #=> {:name => “example”, :is_admin => true}
      @user = User.create(params[:user])
    end

    def update
      @user = User.update_attributes(params[:user])
    end

但是如果这个模型中包含一些敏感属性，例如此例中 is_admin 是个辨别是否是管理员的布尔值，它不应该让使用者可以修改。这时候我们就必须用**健壮参数**（Strong Parameters）来保护这些属性：

加入健壮参数功能后，Action Controller 的参数禁止在 Avtive Model 中批量赋值，除非参数在白名单中。也就是说，你要明确选择那些属性可以批量更新，避免意外把不该暴露的属性暴露了。

而且，还可以标记哪些参数是必须传入的，如果没有收到，会交由 raise/rescue 处理，返回“400 Bad Request”。

如在 products_controller.rb 中，我们就在私有方法中定义了一个

    private
      def product_params
        params.require(:product).permit(:name, :description, :category, :price)
      end

而 create 动作则定义如下：

    def create
      @product = Product.new(product_params)
    end

这样，在 create 动作中，只有在白名单的四个属性允许被修改，除此之外的都会被过滤掉。