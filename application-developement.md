# 系统功能的设计与实现

## 开发工具和运行环境[DONE]

<table>
    <tr>
        <td>操作系统</td>
        <td>Ubuntu 14.04</td>
    </tr>

    <tr>
        <td>数据库</td>
        <td>SQLite</td>
    </tr>

    <tr>
        <td>Web服务器</td>
        <td>Webrick</td>
    </tr>

    <tr>
        <td>开发框架</td>
        <td>Rails 4.1.5</td>
    </tr>

    <tr>
        <td>开发语言</td>
        <td>Ruby 2.1.2p95</td>
    </tr>

    <tr>
        <td>文本编辑器</td>
        <td>Sublime Text 3</td>
    </tr>

</table>

## 系统实现的相关技术[DONE]

### [Ruby语言](http://www.w3cschool.cc/ruby/ruby-intro.html)

Ruby是一种纯粹的面向对象编程语言。
它由日本的松本行弘（まつもとゆきひろ/YukihiroMatsumoto）创建于1993年。
Ruby的特性与Smalltalk、Perl和Python类似。
Perl、Python和Smalltalk是脚本语言。
Smalltalk是一个真正的面向对象语言。
Ruby，与Smalltalk一样，是一个完美的面向对象语言。
使用Ruby的语法比使用Smalltalk的语法要容易得多。

Ruby的特性：

* Ruby是开源的，在Web上免费提供，但需要一个许可证。
* Ruby是一种通用的、解释的编程语言。
* Ruby是一种真正的面向对象编程语言。
* Ruby是一种类似于Python和Perl的服务器端脚本语言。
* Ruby可以用来编写通用网关接口（CGI）脚本。
* Ruby可以被嵌入到超文本标记语言（HTML）。
* Ruby语法简单，这使得新的开发人员能够快速轻松地学习Ruby。
* Ruby与C++和Perl等许多编程语言有着类似的语法。
* Ruby可扩展性强，用Ruby编写的大程序易于维护。
* Ruby可用于开发的Internet和Intranet应用程序。
* Ruby可以安装在Windows和POSIX环境中。
* Ruby支持许多GUI工具，比如Tcl/Tk、GTK和OpenGL。
* Ruby可以很容易地连接到DB2、MySQL、Oracle和Sybase。
* Ruby有丰富的内置函数，可以直接在Ruby脚本中使用。


### [Ruby on Rails (Rails)框架](http://zh.wikipedia.org/wiki/Ruby_on_Rails)

Ruby on Rails简称Rails，是一个使用Ruby语言写的开源Web应用框架。
Ruby语言以自然、简洁、快速著称，全面支持面向对象程序设计，而Rails则是Ruby广泛应用方式之一，在Rails平台上设计出一套独特的MVC开发架构，采取模型（Model）、外观（View）、控制器（Controller）分离的开发方式，不但减少了开发中的问题，更简化了许多繁复的动作。
它努力使自身保持简单，来使实际的应用开发时的代码更少，使用最少的配置。
Rails的设计原则包括“不做重复的事”（Don't Repeat Yourself）和“惯例优于设置”（Convention Over Configuration)。

### [SASS](http://blog.csdn.net/lee_magnum/article/details/11776785)

Sass 是一种基于ruby编写的CSS预处理器。
它诞生于2007年，是最早也是最成熟的一款CSS预处理器语言。
它可以使用变量、嵌套、混入、继承，运算，函数等功能，使得CSS的开发，变得简单清晰可维护，同时也大大节省了设计者的时间，提高了效率。

### [jQuery](http://zh.wikipedia.org/wiki/JQuery#.E7.89.B9.E7.82.B9)

jQuery是一套跨浏览器的JavaScript库，简化HTML与JavaScript之间的操作。
由John Resig在2006年1月的BarCamp NYC上发布第一个版本。
目前是由Dave Methvin领导的开发团队进行开发。
全球前10000个访问最高的网站中，有65%使用了jQuery，是目前最受欢迎的JavaScript库。<br />

jQuery是开源软件，使用MIT许可证授权。jQuery的语法设计使得许多操作变得容易，如操作文档对象（document）、选择DOM元素、创建动画效果、处理事件、以及开发Ajax程序。jQuery也提供了给开发人员在其上创建插件的能力。这使开发人员可以对底层交互与动画、高级效果和高级主题化的组件进行抽象化。模块化的方式使jQuery函数库能够创建功能强大的动态网页以及网络应用程序。

### [AJAX](http://zh.wikipedia.org/wiki/AJAX)

#### AJAX简介

Ajax即“Asynchronous JavaScript and XML”（异步的JavaScript与XML技术），指的是一套综合了多项技术的浏览器端网页开发技术。Ajax的概念由Jesse James Garrett所提出。<br />

传统的Web应用允许用户端填写表单（form），当提交表单时就向Web服务器发送一个请求。
服务器接收并处理传来的表单，然后送回一个新的网页，但这个做法浪费了许多带宽，因为在前后两个页面中的大部分HTML码往往是相同的。
由于每次应用的沟通都需要向服务器发送请求，应用的回应时间依赖于服务器的回应时间。
这导致了用户界面的回应比本机应用慢得多。<br />

与此不同，Ajax应用可以仅向服务器发送并取回必须的数据，并在客户端采用JavaScript处理来自服务器的回应。
因为在服务器和浏览器之间交换的数据大量减少（大约只有原来的5%）,服务器回应更快了。
同时，很多的处理工作可以在发出请求的客户端机器上完成，因此Web服务器的负荷也减少了。

#### Rails中的Ajax

Ajax（异步JavaScript与XML）是一种异步传输接口，可以借由浏览器使用JavaScript和XML或其他数据格式来处理传输请求，而将Web服务器作为后台来处理，这样无须载入额外的网页。
Rails内置有Prototype套件来实现这个技术。
Ajax已经和Ruby on Rails结合在了一起成为了一个新的系统叫做“Ajax on Rails”。
Rails提供一些助手工具来更方便地实现Ajax应用。
Rails提供了一些Helper，可以在服务器一端用纯Ruby语言生成给浏览器用的JavaScript代码，从而让Rails的开发者不需掌握JavaScript就可以简单方便的开发出Ajax的应用。


## 系统模型和数据库的设计
### 创建模型
### 系统数据库的设计

无需设计数据库？？

### 模型之间建立关联

## 系统主要模块的实现
### RubyGems

RubyGems（简称 gems）是一个用于对 Ruby 组件进行打包的 Ruby 打包系统，它使得定位、安装、升级和卸载Ruby包变得容易。
它提供一个分发 Ruby 程序和库的标准格式，还提供一个管理程序包安装的工具。
RubyGems的功能类似于 Linux 下的 apt-get 。

### [Bundler](http://www.yakjuly.com/2010/07/rails3-use-bundler-manage-gems.html)

Bundler 是为 Rails 量身打造的基于 RubyGems 的更高阶 Ruby 组件管理工具，它适合让 Rails 应用管理多套 gems 依存关系的复杂情境。
而在 Rails 中要使用的 gems，也都必须包括在它的 Gemfile 里。
在使用 Bundler 的环境中，要使用任何的 RubyGem 都必须通过 Gemfile 管理。

Gemfile 的写法大致如下：

    # 第二个参数可以指定版本
    gem "rails", "4.1.5"
     
    # 如果 require 的名称不同，可以加上 :require
    gem "sqlite3-ruby", :require => "sqlite3"
     
    # 可以用 Git 当做来源，甚至可以指定 branch, tag 或 ref。
    gem "authlogic", :git => "git://github.com/odorcicd/authlogic.git",
    :branch => "rails3"
     
    # 可以直接用电脑裡的其他目录
    gem "rails", :path => "/Users/ihower/github/rails"
     
    # Group 功能可以让特定环境才会载入
    group :test do
        gem "rspec-rails", ">= 2.0.0.beta.8"
        gem "webrat"
    end

本系统所用到的 gems 如下图所示：

![Gems needed for the app](application-developement/gems.jpg)

在设定好 Gemfile 之后，我们主要用到以下指令：

* bundle install : 安装所有需要的套件。
如果修改了 Gemfile ，就应执行bundle install，这样 Bundler 就会检查并安装这些 gems ，并产生一个Gemfile.lock 文件。 
Gemfile.lock 文件会详细列出所有使用到的 RubyGems 的版本，
所以这个文件也应使用 git commit 命令添加入版本控制系统，这样其他开发者及上线的版本就都会安装完全一样的版本了。

* bundle update : 执行 bundle update gem_name 会更新这个 gem 的版本，
而 bundle update 则会检查所有 gem 并更新到最新版本。
一般来说只需要在每次修改 Gemfile 后，执行 bundle install 即可。
如果 gem 之间有依赖性问题 bundle install 无法解决，则会提示执行 bundle update 。

### 用户注册登录模块

Devise 是 Ruby on Rails 中最常用的 gem 之一。
它是一个第三方权限认证组件，它为 Rails 程序提供了一套易用的用户认证方案，通过它可以无需编码在几分钟内快速生成一个带有登陆、注册、权限认证和重置密码的用户认证模块。

为使用这个 gem ，我们首先将

    gem 'devise'
添加入 Gemfile ，执行 bundle install 后，需要安装 devise 到系统，对 devise 执行初始化：

    rails generate devise:install
之后执行

    rails g devise User 
    // 在 Rails 命令中，generate 可直接简写为，类似的有 rails sever 简写为 rails s ; rails console 简写为 rails c ; destroy 简写为 d 等
该命令会
* 在 app/models 文件夹下产生了一个 user.rb ，也就是创建了一个用户模型
* 在 db/migrate 文件夹下产生了一个 migration 文件, 用于数据库的迁移
* 在 config/routes.rb 文件中添加了一行 devise_for :users，这一行代码添加了各种用户注册、登录等的默认路径。

之后我们执行

    rake db:migrate
生成 User 数据表。
此时，我们进入 http://localhost:3000/users/sign_up 和 http://localhost:3000/users/sign_up ，发现已经实现了用户注册和用户登录功能了。

![user_signup](application-developement/user_signup.png)
![user_signin](application-developement/user_signin.png)

另外 devise 还提供了一些控制器的 filters 和帮助方法 (helper) 。

若在触发某控制器的某个或所有动作之前需要验证用户是否登录，我们可以调用回调函数

    before_action :authenticate_user!

如果用户在未登录状态下触发了该控制器页面则会自动跳转到登录页面。

* 若我们需要验证用户是否登录，可使用

        user_signed_in?

* 若要指向当前登录用户，可使用

        current_user

接着我们利用 rake routes 来查看 devise 这个 gem 为我们生成的所有控制器和动作 (action) 。

![devise_rake_routes](application-developement/devise_rake_routes.png)

这些信息足以让我们能在任意页面创建用户登录和注册的链接了

    <% if user_signed_in? %>
        Signed in as <%= current_user.email %>. Not you? 
        <%= link_to "Sign out", destroy_user_session_path, method: :delete %>
    <% else %>
        <%= link_to "Sign up", new_user_registration_path %> or <%= link_to "Sign in", user_session_path %>
    <% end %>

在应用全局模板文件 /online-store/app/views/layouts/application.html.erb 内插入以上代码并刷新页面，可以发现用户登录和注册链接已经被创建

![sign in and up links](application-developement/sign_in_and_up_links.png)

登录后则显示

![signed_in_link](application-developement/signed_in_link.png)

至此，普通用户的注册于登录模块已基本完成。

### 权限管理模块

[CanCan](https://github.com/ryanb/cancan) 是最流行的在 Rails 应用中进行权限管理的 gem 。
它负责角色建立、对角色授权、在页面中根据授权是否显示元素，以及模型中超出授权时抛出异常。
所有的权限都在单文件 ability.rb 中设定。
然而， CanCan 的原作者 [Ryan Bates](https://github.com/ryanb)在去年9月就对该项目停止了更新，使得该项目中的部分特性不能支持之后推出的 Rails 4 。
于是， CanCan 社区的开发者们为了该项目的延续，自发对其进行更新（开源精神），并取名为 [CanCanCan](https://github.com/CanCanCommunity/cancancan) ，使其完美支持至今为止的所有 Rails 版本。

同样，我们首先把这个 gem 包含入 Gemfile 中

    gem 'cancancan'

之后，根据 CanCanCan GitHub主页的 README ，我们使用以下命令生成设定权限的 ability.rb

    rails g cancan:ability

在这个文件中定义不同角色的用户权限

    def initialize(user)
        user ||= User.new
        if user.admin?
            can :manage, :all
        else
            can :manage, Order
            can :read, Category
            can :read, Product
        end
    end
代码中，:manage 和 :all 分别表示 CRUD 中所有的动作，和系统中的所有模型。
也即：若用户为管理员，则他将拥有对所有模型的所有动作的操作权。
而对于非管理员用户，他们只能拥有对于商品、分类的读取权限以及（自己的）订单的控制权限。

最后要将以上权限设定应用到各个模型中，只需在该模型控制器文件中添加一行
    
    load_and_authorize_resource 

即可在该控制器的任意行为被触发之前通过 before_action 回调函数来验证用户对于该动作的权限。

### 购物车模块
### 订单模块
### 邮件发送模块
### 多国语言模块

## 版本控制系统Git[DONE]
### Git简介

Git是一个开源的分布式版本控制系统，用以有效、高速的处理从很小到非常大的项目版本管理。

从一般开发者的角度来看，git有以下功能：

1. 从服务器上克隆数据库（包括代码和版本信息）到单机上。
2. 在自己的机器上创建分支，修改代码。
3. 在单机上自己创建的分支上提交代码。
4. 在单机上合并分支。
5. 新建一个分支，把服务器上最新版的代码fetch下来，然后跟自己的主分支合并。
6. 生成补丁（patch），把补丁发送给主开发者。
7. 看主开发者的反馈，如果主开发者发现两个一般开发者之间有冲突（他们之间可以合作解决的冲突），就会要求他们先解决冲突，然后再由其中一个人提交。如果主开发者可以自己解决，或者没有冲突，就通过。
8. 一般开发者之间解决冲突的方法，开发者之间可以使用pull 命令解决冲突，解决完冲突之后再向主开发者提交补丁。

### [Git主要命令介绍](http://blog.csdn.net/hangyuanbiyesheng/article/details/6731629)

* git init : 初始化当前目录为Git版本控制的目录,在当前目录中产生一个.git 的子目录。
以后，所有的文件变化信息都会保存到这个目录下。
* git add : 添加至暂存区，但并未提交至服务器。
git add . 是表示把当前目录下的所有更新添加至暂存区。
* git commit : 提交当前工作目录的修改内容。
直接调用git commit命令，会提示填写提交版本描述。
通过如下方式在命令行就可填写提交描述：git commit -m "这里填写描述"。
git commit还有一个-a的参数，可以将那些没有通过git add添加的已被跟踪的文件（较上一版本的新文件为“未被跟踪的文件”(Untracked files)）变化一并强行提交。
如需同时使用-a和-m参数可直接使用-am。
* git status : 查看版本库的状态。
可以得知哪些文件发生了变化，
哪些文件还没有添加到git库中等等。 
建议每次commit前都要通过该命令确认库状态。
* git branch ： 列出本地Git库中的所有分支。
在列出的分支中，若分支名前有*，则表示此分支为当前分支。
在Git版本库中创建分支的成本几乎为零，所以，不必吝啬多创建几个分支。
当第一次执行git init时，系统就会创建一个名为“master”的分支。
而其它分支则通过手工创建。
* git checkout 分支名 : 切换到某个分支。（只有当前工作分支的更改全部通过git commit提交后才可允许切换分支）
* git checkout -b 分支名 : 创建该分支名同时将当前工作分支切换到了该分支上。 
* git merge : 把服务器上下载下来的代码和本地代码合并，或者进行分支合并。
* git push origin branch-name ： 提交本地分支branch-name至在线版本库
（origin只相当于一个别名，运行git remote –v或者查看.git/config可以看到origin的含义，一般指git版本库，如需将代码部署至Heroku则需将origin改为heroku)，
只有当前工作分支的更改全部通过git commit提交后使用git push命令才能上传更新后的源码。
* git log : 查看历史日志，包含每次的版本变化。
每次版本的变化都会生成一个对应的唯一的SHA-1哈希值(hash)，作为指纹字符串。
该字符串由40个十六进制字符（0-9及a-f）组成。
Git的工作完全依赖于这类指纹字串，所有保存在Git数据库中的东西都是用此哈希值来作为索引的。

### 本系统运用Git进行版本控制的主要流程
![Git flowchart](application-developement/git-flowchart.jpg) // Lacks the branch part
### GitHub简介

[GitHub](http://zh.wikipedia.org/wiki/GitHub#.E4.B8.AD.E5.9B.BD.E5.A4.A7.E9.99.86)是目前最流行的Git访问站点，它是一个共享虚拟主机服务，用于存放使用Git版本控制的软件代码和内容项目。
GitHub同时提供付费账户和为开源项目提供的免费账户。
许多赫赫有名的程序库、开发框架都采用GitHub作为为主版本控制平台，其中包括[jQuery](https://github.com/jquery/jquery
), [PHP](https://github.com/php
), 以及本系统使用的开发语言[Ruby](https://github.com/ruby/ruby
)和开发框架[Rails](https://github.com/rails/rails/
)。

### Git在本系统中的运用

#### 分支 (branch)

本系统中的[所有代码](https://github.com/jeremylinlin/online-bookstore)利用GitHub提供的免费账户进行代码托管，其中包含若干个分支(branch)和一个主分支(master)。
一般说来，一个分支通常被用来完成某种特定的功能，当此分支的功能被完成后则会被合并(merge)至master分支。
在开源项目中，不同分支往往被不同开发者创建，用来完成不同的功能。
在本系统中，分支主要被用来区分开发的不同阶段。

#### 提交 (commit)

对于普通用户来说，所谓的版本往往意味着如：Alpha 0.14, Beta 2.05等，
然而这一些数字对于开发者而言完全没有任何实际意义。
当以数字编号的版本多至七、八，甚至数十个以后，开发人员根本不可能记得请每个版本号后对应功能的增删。<br />
在Git中，通过使用git commit命令对当前工作目录所做的修改进行提交，这一次提交可被算作为一个“版本”，而-m参数则表示该版本的描述。
某版本中初次使用git commit提交前必须使用git add .("."表示当前目录的所有文件)或在使用git commit时同时加上-a参数。
另外，初次提交必须含有-m参数，否则会自动进入默认命令行编辑器提示输入提交版本描述。
![Commit Message](application-developement/commit-message.jpg)
每提交完一次，Git系统就会自动生成一个SHA-1值，利用git log可查看各版本提交的历史。
如在若干版本提交之后发觉之前某一版本删除了某重要功能，此时则可利用“git checkout 对应SHA-1值”即时返回至该版本之前的某一版本，根据需要进行各种操作。
Git版本控制的主要功能由此实现，即自从首次提交(Initial Commit)那一刻起，每一次版本的提交就相当于对所有数据进行了一次保存。（实际并不是真正的保存，具体原理可参考Scott Chacon的[Pro Git](http://git-scm.com/book)一书）<br />
本系统的[GitHub主页](https://github.com/jeremylinlin/online-bookstore)中，在任何分支里都可查看到该分支中每一个源码文件最新版本所对应的最近一次版本提交信息。（若某文件在某次版本提交中未被修改则不会被提交）
![Commit Messages](application-developement/commit-messages.jpg)

## 云应用部署平台Heroku[DONE]

### [Heroku简介](http://baike.baidu.com/view/4931959.htm?fr=aladdin)
Heroku是一个支持多种编程语言的[云平台即服务](http://baike.baidu.com/view/1734078.htm)。
在2010年被 Salesforce.com 收购。
Heroku作为最开始的云平台之一，从2007年6月起开发，当时它仅支持Ruby，但后来增加了对Java、Node.js、Scala、Clojure、Python以及（未记录在正式文件上）PHP和Perl的支持。<br />
Heroku 最受人喜爱的地方之一，就是它提供免费额度：
网站空间部分，每个项目的限制是100MB，这对于一般的小型的项目来说已经足够了;
而对于数据库，每个项目的大小限制则是5MB，而且有 SQLite、MySQL、PostgreSQL 可以选用。


### [搭建 Heroku 部署环境](http://railstutorial-china.org/chapter1.html#section-1-4-1)

Heroku 让 Rails 应用程序的部署变得异常简单，只要把源码纳入了 Git 版本控制系统就行了。
在本系统中，要成功使用 Heorku 对源代码进行部署前，需要进行一些简单的配置（注册账户等在此省略）。<br />
由于 Heroku 使用 PostgreSQL数据库，所以我们要把 pg 加入生产组，Rails 才能和 PostgreSQL 通信：

    group :production do
      gem 'pg', '0.15.1'
    end
同时使 sqlite3 仅适用于开发组和测试组，

    group :development, :test do  
      gem 'sqlite3'  
    end 
随后执行 bundle install，并指定旗标：

    $ bundle install --without production
之后还要做一些设置来生成 Heroku 服务静态资源所需的文件，例如图片和 CSS。
首先要确保 config/environments/production.rb 中

    config.serve_static_assets = true
之后执行

    heroku run rake assets:precompile
至此，Heroku部署Rails的初始配置全部完成，最后只需提交更改，如：

    git commit -m "Finish setting up Heroku"

即可通过

    git push heroku 分支名

来上传源代码至Heroku。

### Heroku 其他命令

在配置完 Heroku 之后我们将主要使用 git push heroku 来上传代码，但还有另一些与 Heroku 相关的命令值得一提：

1. 在本地 Rails 服务器中我们通过

        rails server
或

        rails s
启动服务器的同时即可看见命令窗口中的即时服务器运行日志。
而要查看 Heroku 平台上的应用的即时日志信息，则可通过

    heroku logs --tail
而

    heroku logs -n 50
则表示显示当前 Heroku 应用最新运行日志的最后50行。
2. 在本地 Rails 中我们通过

        rake db:migrate
来将所有未实施的迁移任务实施到目标数据库上。而在 Heroku 平台上，我们则通过

        heroku rake db:migrate
进行远程数据库的数据迁移任务。
3. 在本地 Rails 中我们通过

        rails console
或

        rails c
进入 Rails 控制台。
而我们同时可以通过

        heroku run rails console
或

        heroku run rails c

直接进入远程服务器的 rails 控制台。

## 系统展示
