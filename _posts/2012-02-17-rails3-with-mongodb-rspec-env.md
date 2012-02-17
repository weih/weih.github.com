---
layout:       post
title:        "搭建Mac + Rails + Mongodb + Rspec开发环境"
description: 
banner: "/img/posts/geekdoor02.png"
categories: 
- development
- rails
- code
- database
---
鉴于要做`极客的任意门`这东东，这里简单记录下一个最基本的开发环境的搭建，以及注意事项，供大家参考。

环境为Mac + Ruby 1.9.3 + Rails 3.2.1 + Mongodb + Rspec，没用过，这次正好都用最新的看看。

# 一、Mongodb
安装不多，官网很详细，推荐[homebrew][1]。若使用homebrew安装，安装完之后记得看info，里面有让mongodb默认daemon启动方法以及开机启动的代码，复制粘贴即可。

开启mongod进程后就可以使用mongodb连接该服务端了，并且可以在http://localhost:28017中看到简单的mongod控制面板（mongod的监听端口默认是27017，控制面板端口为该端口号加1000），这样mongodb就算好了
# 二、rvm

这个没什么好说的，一定要用的的，安装不说了，说下之后的使用：

{% highlight bash %}
$ mkdir rails_3.2.1_project
$ cd rails_3.2.1_project
$ mate .rvmrc # add rvm use 1.9.3@project_name --create
{% endhighlight %} 

这样在这个目录下都是用ruby 1.9.3，然后有自己的gemset，下面在目录下：

{% highlight bash %}
$ gem install rails # 在project_name这个gemset下安装最新版rails，目前是3.2.1。这样就可以在此目录下生成最新的rails项目了
$ rails new app -T # -T 表示不生成/test目录，我们用rspec
{% endhighlight %}

ruby-china的wiki里有一个[实用指南][2]，值得一看

# 三、Gemfile

之后再Gemfile中加入：

{% highlight ruby %}
gem "mongoid", "2.4.3" # Mongodb的ODM，类似ActiveRecord
gem "bson_ext", "1.5.2" # Mongodb的bson格式扩展，能很大的提高效率，因为用C写的

group :development, :test do
  gem 'rspec-rails'
  gem 'guard' # guard用来自动化测试，自动刷新浏览器
  gem 'guard-rspec'
  gem 'guard-livereload'
end
{% endhighlight %} 

并删除：

{% highlight ruby %}
# gem 'sqlite3'
{% endhighlight %} 

然后：

{% highlight bash %}
$ bundle install
{% endhighlight %} 

# 四、删除Active_Record内容

首先删除config/database.yml

编辑config/application.rb，不加载active_record
{% highlight ruby %}
# require "active_record/railtie"
require "action_controller/railtie"
require "action_mailer/railtie"
require "active_resource/railtie"
require "sprockets/railtie"
{% endhighlight %} 

编辑config/enviroments/development.rb，注释掉如下两行active_record相关代码
{% highlight ruby %}
# Raise exception on mass assignment protection for Active Record models
# config.active_record.mass_assignment_sanitizer = :strict

# Log the query plan for queries taking more than this (works
# with SQLite, MySQL, and PostgreSQL)
# config.active_record.auto_explain_threshold_in_seconds = 0.5
{% endhighlight %} 

# 五、config

在rails项目目录下：
{% highlight bash %}
$ rails generate mongoid:config # 默认配置就可用了
$ rails generate rspec:install

$ rails s # 启动webrick
{% endhighlight %} 

大概就这么多，希望你能不出问题。

好吧，其实配置rails不出问题往往是困难的，但是记得看log，以及一次又一次在水深火热之时帮助我们的Google算法（是Google算法，不是Baidu短发，rails的问题往往Google能解决而Baidu不行）。

[1]: http://mxcl.github.com/homebrew/
[2]: http://ruby-china.org/wiki/rvm-guide
