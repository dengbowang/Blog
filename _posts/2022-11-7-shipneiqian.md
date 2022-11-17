---

layout:       post
title:        "哔哩哔哩视频内嵌入"
author:       "dengbowang"
header-style: text
catalog:      true
tags:
    - 哔哩哔哩
    - Markdown

---


<iframe src="//player.bilibili.com/player.html?aid=944583285&bvid=BV1UW4y1j7Gg&cid=875050848&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
稍微解释一下上面代码的含义：

page -> 起始下标为 1 (默认值也是为1)

as_wide -> 是否宽屏 【1: 宽屏, 0: 小屏】





<iframe src="//player.bilibili.com/player.html?aid=944583285&bvid=BV1UW4y1j7Gg&cid=875050848&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

high_quality -> 是否高清 【1: 高清(最高1080p) / 0: 最低视频质量(默认)】

danmaku -> 是否开启弹幕 【1: 开启(默认), 0: 关闭】

allowfullscreen -> allowfullscreen= "ture" 允许全屏，使用该参数可以在浏览器中全屏播放 

```c

BILIBILI 地址PC端参数    

&high_quality=1   (1=最高画质 0=最低画质)  

&danmaku=0   (1=打开弹幕 0=关闭弹幕) 

iframe 参数    
allowfullscreen="allowfullscreen" #移动端全屏    
sandbox="allow-top-navigation allow-same-origin allow-forms allow-scripts" #禁止弹出网页
```
<iframe src="//player.bilibili.com/player.html?aid=251643277&bvid=BV1av411M7XG&cid=441250782&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="100%" height="100%"scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="100%" height="100%"> </iframe> 
