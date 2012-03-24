---
layout:       post
title:        "Contributing to Opensource"
description: 
banner: "/img/posts/pull-request.jpg"
categories: 
- development
- github
- code
---
<center>
  <a href="/img/posts/pull-request.jpg" class="folio-image-wrapper"><img class="bordered" alt="screenshot" src="/img/posts/pull-request.jpg" style="margin-top:20px; width:100%;" /></a>
</center>

就在昨天，终于向开源界贡献了一次代码，贡献的内容如此之简单，说来都不好意思：
{% highlight bash %}
# <div class="box">
<div class="box" style="text-align:center;">
<h2><%= link_to(@node.name,  node_topics_path(@node))%></h2>
{% endhighlight %} 

这是[Ruby China][1]的一段代码，我将第一行改成了第二行。好吧，我其实只加了一个selector，让一个button居中而已。

不只是你觉得没什么，我自己也觉得这真是无关紧要，不过这个问题最少存在了有一个月之久，我想看到这里有问题的人应该怎么说都有上百人（Ruby China当时共有1200+会员，提交过代码的共26人），我自己也觉得很奇怪为什么这么明显的一个并且简单的问题没有人来修改？

我想问题并不出在[huacnlee][2]、[ashchan][3]等几位的身上，不同等级的人注重的地方不一样（好像他们最近在忙着为ruby-china加api中）。不过作为能力不足的程序员来说，当发现这种即明显又简单的bug时，难道不应该贡献自己一份力量吗？

最好的情况：fork一份ruby-china的代码，然后修改，pull-request。这样做的你很棒，不过不是什么人都愿意或者说都能这么做。首先你要会使用git以及github；其次你要能把ruby-china的源代码在本地跑起来（我想这是阻碍绝大多数人贡献代码的原因），最后你还要能看到源代码，知道问题出在哪（看懂部分也是完全没问题的）。

较好的情况：如果你不具备上一种情况的几种条件的话，你也有自己可以做的。去[github][4]提交一个issue，告诉有能力进行修改的人，你发现了问题。恩，简单粗暴，我想谁都能做，就开有没有心了。

经过这一次折腾，不仅让我知道了怎么将Ruby China的源代码跑起来，也知道了向github项目贡献代码的整个流程，让我受益匪浅。

[1]: http://ruby-china.org
[2]: https://github.com/huacnlee
[3]: https://github.com/ashchan
[4]: https://github.com/huacnlee/ruby-china