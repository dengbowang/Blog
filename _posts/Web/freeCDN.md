---
title: 快速免费的公用 CDN —— jsDelivr
date: 2023-2-14
tags:
  - blog
  - web
  - CDN
categories:
  - 前端
cover: https://img2018.cnblogs.com/i-beta/1365470/202001/1365470-20200119104921111-1131459704.png
---

# 快速免费的公用 CDN —— jsDelivr - Rogn - 博客园

> ## Excerpt
> CDN的全称是Content Delivery Network，即内容分发网络。CDN是构建在网络之上的内容分发网络，依靠部署在各地的边缘服务器，通过中心平台的负载均衡、内容分发、调度等功能模块，使用

---
CDN的全称是Content Delivery Network，即内容分发网络。CDN是构建在网络之上的内容分发网络，依靠部署在各地的边缘服务器，通过中心平台的负载均衡、内容分发、调度等功能模块，使用户就近获取所需内容，降低网络拥塞，提高用户访问响应速度和命中率。CDN的关键技术主要有内容存储和分发技术。——百度百科

由于某些原因，很多公用免费的 CDN 资源在中国大陆并不很好用，就算是付费的，也有一定的限制，例如每天的刷新次数有限之类的。那有没有一款造福人类的，或者造福中国大陆的公用 CDN 呢？

## jsDelivr

先看看官方的介绍：

[![](https://img2018.cnblogs.com/i-beta/1365470/202001/1365470-20200119104921111-1131459704.png)](https://img2018.cnblogs.com/i-beta/1365470/202001/1365470-20200119104921111-1131459704.png)

这是在中国大陆唯一有 license 的公有 CDN，而且实际使用中的访问速度也是极快的（虽然官网打开速度慢

### 与 Github、NPM、WorldPress 整合

官网地址：[https://www.jsdelivr.com](https://liubing.me/goto/https://www.jsdelivr.com) 没梯子访问可能有点慢，不过CDN的节点是很快的 可以引用的资源包括NPM、github、wordpress的所有资源，github可以是任意体积小于50M的仓库。

以github为例，只需要通过符合 JSDelivr 规则的 URL 引用，即可直接使用 Github 中的资源。



```
// 用户名/仓库名@版本号/文件名
https://cdn.jsdelivr.net/gh/user/repo@version/file
// load jQuery v3.2.1
https://cdn.jsdelivr.net/gh/jquery/jquery@3.2.1/dist/jquery.min.js


// 使用一个范围内的版本
https://cdn.jsdelivr.net/gh/jquery/jquery@3.2/dist/jquery.min.js
https://cdn.jsdelivr.net/gh/jquery/jquery@3/dist/jquery.min.js


// 忽略版本号则默认使用最新版
// you should NOT use this in production
https://cdn.jsdelivr.net/gh/jquery/jquery/dist/jquery.min.js


// 在任意JS/CSS文件后添加 .min 能得到一个缩小版
// 如果它本身不存在，我们将会为你生成
https://cdn.jsdelivr.net/gh/jquery/jquery@3.2.1/src/core.min.js


// 在末尾加 / 则得到目录列表
https://cdn.jsdelivr.net/gh/jquery/jquery/
```



详细规则参考官网：[https://www.jsdelivr.com/](https://www.jsdelivr.com/)

以我一张图片为例：

原github链接：[https://raw.githubusercontent.com/growvv/img/master/images/20200118222911.jpeg](https://raw.githubusercontent.com/growvv/img/master/images/20200118222911.jpeg)

CDN后的链接：[https://cdn.jsdelivr.net/gh/growvv/img@master/images/20200118222911.jpeg](https://cdn.jsdelivr.net/gh/growvv/img@master/images/20200118222911.jpeg)

## 其他

除了`jsdelivr`， 推荐几个免费的且不限流量的CDN，还有 `staticaly` `githack` 都是全球通用的，

# staticaly

官网地址：[https://www.staticaly.com](https://liubing.me/goto/https://www.staticaly.com)  
轻松地从GitHub / GitLab / Bitbucket等加载您的项目 没有流量限制或限制。

文件通过超快速全球CDN提供。 在URL（不是分支）中使用特定标记或提交哈希。  
根据URL永久缓存文件。 除master分支外，文件在浏览器中缓存1年。 具体用法：



```
# GitHub CDN
https://cdn.staticaly.com/gh/:user/:repo/:tag/:file
https://cdn.staticaly.com/gh/growvv/growvv.github.io/master/README.md

# GitLab CDN
https://cdn.staticaly.com/gl/:user/:repo/:tag/:file

# Bitbucket CDN
https://cdn.staticaly.com/bb/:user/:repo/:tag/:file

# WordPress CDN
https://cdn.staticaly.com/wp/c/:version/wp-includes/:file  
https://cdn.staticaly.com/wp/p/:plugin_name/:version/:file  
https://cdn.staticaly.com/wp/t/:theme_name/:version/:file

# Imgpx CDN
https://cdn.staticaly.com/img/:image_url

# Favicons CDN
https://cdn.staticaly.com/favicons/:favicon_url
```



# githack

直接从GitHub，Bitbucket或GitLab提供原始文件  
官网地址：[http://raw.githack.com/](https://liubing.me/goto/http://raw.githack.com) 具体用法和上面的`staticaly`很类似



```
# Github CDN
//主分支
https://rawcdn.githack.com/liub1934/LB-Blog/master/wp-content/themes/Memory/emoji/xiaodianshi/baiyan.png

//版本分支
https://rawcdn.githack.com/liub1934/LB-Blog/8806f440d3f9a7cc3e6125d7d75564e40262c6a8/wp-content/themes/Memory/emoji/xiaodianshi/baiyan.png
```


参考链接：

1. [https://segmentfault.com/a/1190000020239193](https://segmentfault.com/a/1190000020239193)

2. [https://blog.csdn.net/qq\_36759224/article/details/86936453](https://blog.csdn.net/qq_36759224/article/details/86936453)

3. [https://liubing.me/recommend-several-free-unlimited-cdns.html](https://liubing.me/recommend-several-free-unlimited-cdns.html)

4. [https://fileem.com/jsdelivr-free-public-cdn-acceleration-service](https://fileem.com/jsdelivr-free-public-cdn-acceleration-service)

- [jsDelivr](https://www.cnblogs.com/lfri/p/12212878.html#tid-aikCyH)

- [与 Github、NPM、WorldPress 整合](https://www.cnblogs.com/lfri/p/12212878.html#tid-Z7bE3M)

- [其他](https://www.cnblogs.com/lfri/p/12212878.html#tid-dCjmb6)

- [staticaly](https://www.cnblogs.com/lfri/p/12212878.html#tid-EAW8M4)

- [githack](https://www.cnblogs.com/lfri/p/12212878.html#tid-Ey3BNf)

  
