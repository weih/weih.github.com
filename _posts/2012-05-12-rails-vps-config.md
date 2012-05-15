---
layout:       post
title:        "Deploying to a VPS"
description: 
banner:
categories: 
- development
- rails
- code
---

昨天晚上买了20刀一月Linode，准备体验下这个口碑最好的vps，目前感觉良好，这里作下记录。

{% highlight bash %}
root@li413-47:~# apt-get update
root@li413-47:~# apt-get install build-essential bison openssl libreadline6 libreadline6-dev curl git-core zlib1g zlib1g-dev libssl-dev libyaml-dev libsqlite3-0 libsqlite3-dev sqlite3 libxml2-dev libxslt-dev autoconf python-software-properties
root@li413-47:~# bash < <(curl -sk https://raw.github.com/wayneeseguin/rvm/master/binscripts/rvm-installer)

root@li413-47:~# adduser deployer --ingroup admin
root@li413-47:~# su deployer

root@li413-47:~# rvm install 1.9.3
root@li413-47:~# rvm use 1.9.3 --default

root@li413-47:~# rvm add-apt-repository ppa:nginx/stable
root@li413-47:~# apt-get update
root@li413-47:~# rvm apt-get install nginx
root@li413-47:~# service nginx start

root@li413-47:~# add-apt-repository ppa:chris-lea/node.js
root@li413-47:~# apt-get update
root@li413-47:~# apt-get install nodejs

root@li413-47:~# gem install bundler --no-ri --no-rdoc


contiune.....
{% endhighlight %} 
