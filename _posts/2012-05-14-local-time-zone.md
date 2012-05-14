---
layout:       post
title:        "Rails 3.2使用本地时间的正确方法"
description: 
banner: 
categories: 
- development
- rails
- code
---

在VPS上希望ActiveRecord使用本地时间，不要将从db中取出来的数据转换为UTC，经过Google，正确的设置如下：

{% highlight ruby %}
# config/application.rb

config.time_zone = 'Beijing'
config.active_record.default_timezone = :local
config.active_record.time_zone_aware_attributes = false # this is important!
{% endhighlight %}

最后一行很重要，只有加了这一行，AR才不会将date, datetime类型的行转换为UTC时间。