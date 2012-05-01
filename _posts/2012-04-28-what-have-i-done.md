---
layout:       post
title:        "神隐一个半月做了些啥？"
description: 
banner: 
categories: 
- development
- 胡说八道
---

隐匿了一个半月了，虽然没写Blog，但做了很多事，是时候总结下了，大概分成Screencasts、Books、Gems几个部分

# Screencasts

<strong>Railscasts</strong>

Railscasts是所有Rails开发者都会去拜访的网站，我大概花了大半年的时间把Railscasts的视频都看了一遍，虽然并不是每一个视频都对目前的我来说有帮助，但毫无疑问的是作为一个Rails程序员，任何一期你都漏不得

<strong>Codeschool</strong>

花9刀买了一个月，感觉值90刀啊，真是收益匪浅。感觉Envy Lab的各位真是会玩，能将基于Web的交互式教程做到这种程度真是不简单。个人感觉整个课程安排的十分合理，寻寻渐进，引人入胜。虽说大多内容都是面向初学者，但是任何一个Rails程序员都很有必要去看看。整体课程以Rails为核心，加上HTML、CSS、Javascript这三项前端技术。而且完成了课程还有相应的奖励，包括Peepcode的免费视频，Railscasts的一个月免费等，不得不说这9刀花的实在是太值，推荐所有有可以刷美刀信用卡的Rails程序员们去订阅一个月，你绝对不会后悔的。

# Books

看的书有点略多，不一一介绍，很多都是必读的。

<strong>《Rails 3 Way》</strong>

Rails进阶必读

<strong>《The RSpec Book》</strong>

Rspec作者的著作，只看了Rspec的部分，Cucumber的部分跳过了，我还是觉得Cucumber太过了

<strong>《Rails View》</strong>

pragprog.com 4月新书

<strong>《Rails Recipes》</strong>

看的Rails 3的版本，感觉很好，很多的tips都在Railscasts中见到了影子，我想ryanb也从2上一版中学到了不少，而且ryanb还出现在了这个版本的Acknowledgement中

<strong>《Emacs Manual 23》</strong>

Stallman亲笔的超长手册，文笔一流，边用边学，告别Textmate

<strong>《jQuery 攻略》</strong>

算是本速查手册，适合与从没听过jQuery的同学阅读

<strong>《Javascript高级程序设计（第三版）》</strong>

经典延续，不过觉得并不完全适合我，作者花了很多的笔墨在浏览器兼容性上，对Javascript的变成方法和技巧介绍的比较少

<strong>《CSS CookBook》</strong>

看的中文第二版，看完后觉得好老啊，好多内容都过时了五六年了

<strong>《HTML 5与CSS 3权威指南》</strong>

国内的书看得比较少，这本还不错，HTML5与CSS3的新特性说的还是挺简单明了，配合Codeschool的教程效果更加

<strong>《MongoDB 权威指南》</strong>

写第一个项目时心血来潮用了Mongodb和Mongoid，稍微了解和学习了下Mongodb，短小精悍的手册，官方团队编写

<strong>《Git 权威指南》</strong>

很有深度的Git书籍，国内难得的好书，使用Git的同学必读

<strong>《写给大家看的设计书》</strong>

好书啊，算是看了两边，让我对什么是好的设计有了更深的认识。作者还有一本关于Web设计的书我也看了，但是这本感觉就觉得不如这本

<strong>《启示录》</strong>

经常在程序员杂志上看到节选，索性就买了一半来看，有些地方有些共鸣。不过我还是更喜欢37singals的那两本，哪两本你懂得

# Gems

在公司没事的时候自己用Rails写了些小玩意，并学习了几个Gem的使用，总结下

<strong>twitter-bootstrap-rails</strong>

很多人不推荐使用bootstrap，因为它不像Buorben和Compass只是提供了Mixin，而是直接修改了所有的样式（当然可以部分import），不过我觉得对于CSS和设计苦手的后端程序员来说，还是很有意义的。而且其提供的12个jQuery插件也能很好的提升用户体验，用起来也十分的方便

<strong>simple_form</strong>

Jose Valim出品，必属精品，而且2.0和bootstrap的整合也对前端蹩脚的我提供了不小的便利

<strong>sorcery</strong>

没去用devise或者Omniauth，选了个简单、轻量的sorcery，目前觉得够用了，以后不用自己完全从底层实现用户系统啦

<strong>carrierwave</strong>

好用的File uploader，优先于Paperclip，个人觉得将uploader和modal分离是比较好的实现

<strong>delayed job</strong>

采用active_record做为backend的background job，用起来比resque要简单的多

<strong>slim</strong>

slim比haml更简单，同时吸取了node.js的模版语言jade与haml，的确是让view部分的代码量少了很多。还没遇到表达不出来的语法，不过也有几种相对erb来说看起来要更啰嗦（当然可能是我没找对方法）

<strong>sass</strong>

学了sass之后才知道css还能这么写，之前写第一个Rails项目的时候也没有用sass，仅用了普通的css，sass配合Bourbon和Compass的组合的确是非常强大，不过目前觉得Bourbon + Bootstrap的组合比较适合我

<hr />

大概就这么多吧，还有些pragprog.com的基本小书就不提了，我也没想到这一个半月做了这么多事，几乎无时无刻不在学习，算是比较充实吧。之前虽然有twitter但是很少看，这段时间偶尔没事的时候拿手机上了下，发现推上的信息还是很有营养的，和国内微博还是有本质的差别，所以决定好好用起来。
