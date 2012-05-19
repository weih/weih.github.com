---
layout:       post
title:        "山口山狗熊榜记录器上线咯"
description: 
banner: 
categories: 
- development
- rails
- code
- game
---

地址在这里：[www.wowarmory.me][1]

UI基本没变，这几天下班后主要在修复各式各样的Bug，目前还有几个不太好解决的问题：

1. 英雄榜上角色的造型图有时候只能获取预设图。这应该是官方为了为服务器减压，限定了某一个IP在短时间内可以请求的图片数量，这个限制在游戏角色头像上也有（当你看到头像或者造型图变成黑影时，说明此时你并未请求到该图片，官方传给了你一个预设图），目前还没想到很好的解决方法。

2. 由于用了一张还大的背景图片，所以设置了background-size: 100%。不过由于我还用了Bootstrap的Collapse来显示角色的过去英雄榜，在进行展开和关闭操作时，如果涉及到页面上其它元素的位置发生变化，则会变的很卡。不过如果不设置background-size: 100%，则不会有问题。这可能跟Bootstrap Collapse的实现方式有关，现在只好指定父级元素为固定大小，以便避免这个问题。

写这个小项目也学了不少东西，像Nginx + Unicorn的配置，Capistrano的使用（这东西真是值得弄懂，意义重大）。

如果你希望可以记录下角色的成长历史，只要上去简单查看一次自己的角色，服务器就会记录角色每天的英雄榜了。

git repo: [https://github.com/weih/armory-recorder][2]，没什么License，各位随意。

[1]: http://www.wowarmory.me
[2]: https://github.com/weih/armory-recorder