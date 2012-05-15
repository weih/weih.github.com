---
layout:       post
title:        "狗熊榜 redesign!"
description: 
banner: "/img/posts/armory_second_step.jpg"
categories: 
- development
- rails
- code
- game
---
<center>
  <a href="/img/posts/armory_second_step.jpg" class="folio-image-wrapper"><img class="bordered" alt="screenshot" src="/img/posts/armory_second_step.jpg" style="margin-top:20px; width:100%;" /></a>
</center>

加点图片发现就不一样了，PS了个Logo（PS自咬人画的格罗姆），然后用Blizzard API取人物头像地址，目前效果如上图，还算满意。

PS：我没直接用Blizzard API，用的老外写的一个wrapper [github.com/BinaryMuse/battlenet][1]，不过在处理大陆地区的数据时有些问题，仅能返回人物的基本信息，详细信息（items, talent...）获取不到，但是美服是可以，应该是编码方面有些问题，暂时用不到，也就没详细去修复这个bug。


[1]: https://github.com/BinaryMuse/battlenet