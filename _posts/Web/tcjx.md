---
title: 图片镜像缓存服务—防盗链图片、imgur 等国内无法访问图片的解决方案
date: 2023-2-12
tags:
  - web
  - blog
  - 图床
categories:
  - 前端
cover: https://w.wallhaven.cc/full/3l/wallhaven-3l9z69.png
---
**https://images.weserv.nl 是一款图片镜像缓存服务**，原用于加速图片访问，但有时候有很多妙用。

比如 imgur 等国内无法访问图床的图片，使用它就能够访问了。

> 图片镜像缓存服务可以用来做什么？

-   可以将有防盗链的图片引用到网页，并成功显示。
-   可以将 http 图片引用到 https 页面而不出现证书问题。
-   可以将 xxx 的图片，成功加载。
-   可以将比较慢的图片资源，加快显示。

使用方法：

`https://images.weserv.nl/?url=原始图片链接`

例如：

`https://i1.funletu.com/img/Jvh1OQm.jpg`

效果：

![](https://images.weserv.nl/?url=https://i1.funletu.com/img/unnamed-file.jpg)

又比如一些防盗链网站的图片是无法直接放在自己的博客上使用的，例如知乎、微信等，但图片地址上加上镜像缓存服务就可以了。

示例：

`https://mmbiz.qpic.cn/mmbiz_png/do0Sayk3PeZBUlWW7NQHX6kicGI0Nf60TYW8A1OIbxKxhURmESZMs0bQzss1pibdJPB62yys3qwNIaZ3VtMYJVug/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1`

![](https://i1.funletu.com/img/Snipaste_2021-08-29_09-48-16.png)

转换后：

`https://images.weserv.nl/?url=mmbiz.qpic.cn/mmbiz_png/do0Sayk3PeZBUlWW7NQHX6kicGI0Nf60TYW8A1OIbxKxhURmESZMs0bQzss1pibdJPB62yys3qwNIaZ3VtMYJVug/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1`

![图片](https://images.weserv.nl/?url=https://i1.funletu.com/img/640.jpg)

这样转换后，放在网站中就可以正常显示了

以下是网络中收集的一些**图片镜像缓存服务**，持续更新。

```
https://img.noobzone.ru/getimg.phpurl=

https://collect34.longsunhd.com/source/plugin/yzs1013_pldr/getimg.php?url=

https://ip.webmasterapi.com/api/imageproxy/https://images.weserv.nl/?url=

https://pic1.xuehuaimg.com/proxy/https://search.pstatic.net/common?src=
```

部分服务图片链接可以不添加 `http://` 或 `https://` 协议。

```
https://ip.webmasterapi.com/api/imageproxy/

https://i.imgur.com/hWghm6oh.jpg

https://images.weserv.nl/?url=i.imgur.com/hWghm6oh.jpg

https://pic1.xuehuaimg.com/proxy/i.imgur.com/hWghm6oh.jpg

```



点点赞赏，手留余香

还没有人赞赏，快来当第一个赞赏的人吧！
