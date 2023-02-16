---
title: 配置 | Hexo Aurora
date: 2022-1-12
tags:
  - blog
  - web
  - Around
categories:
  - 前端
cover: https://img-blog.csdnimg.cn/20210313122054101.png
---

# 配置 | Hexo Aurora

> ## Excerpt
> 迈向未来的 Hexo 极光主题

---
## [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E9%85%8D%E7%BD%AE) 配置

## [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6) 配置文件

一共有两个配置文件，一个是 **Hexo 自身**的配置，一个是**主题专用**的配置。

```
. # Hexo 项目根目录.
├─ _config.yml # Hexo 配置文件.
└─ _config.aurora.yml # 主题配置.
```

注意

大部分主题的功能都是使用主题配置文件的，但是有部分需要用到 Hexo 插件的就需要在 Hexo 的配置中修改。

## [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E5%9F%BA%E7%A1%80%E9%85%8D%E7%BD%AE) 基础配置

我们可以使用 `site` 来设置我们博客的主要信息和配置。

`site` 配置拥有以下选项：

| 选项 | 接受类型 | 使用说明 |
| --- | --- | --- |
| `subtitle` | String | 博客自标题，页面主标题后面会跟随这个标题内容。 |
| `author` | String | 博客作者名字，或者是博客名字。会在 **header 的 logo 区域**显示，也会在**博客简介**中显示。 |
| `nick` | String | 博客子名字，会在 header 的 logo 下方显示。 |
| `description` | String | 会在博客简介中显示，用几句话描述博主相关信息（支持 HTML 标签） |
| `language` | en, cn | 配置默认博客语言，en 是英文，cn 是中文。 |
| `multi_language` | true, false | 开启博客的多语言支持 |
| `logo` | String | Logo 的图片链接 image. |
| `avatar` | String | 头像的图片链接 image. |
| `beian` | Object | 网站备案信息 (从版本 1.1.0 开始，这个配置拥有两个属性) |

提示

如果每首设置 `avatar` 的图片链接，默认会去取 logo 的图片链接。

___

### [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E7%BD%91%E7%AB%99%E5%A4%87%E6%A1%88%E4%BF%A1%E6%81%AF) 网站备案信息

> `beian` 选项

| 选项 | 接受类型 | 使用说明 |
| --- | --- | --- |
| `number` | String | 备案编号. |
| `link` | String | 备案链接. |

___

### [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E5%85%AC%E5%AE%89%E5%A4%87%E6%A1%88%E4%BF%A1%E6%81%AF) 公安备案信息

> `police_beian` 选项

| 选项 | 接受类型 | 使用说明 |
| --- | --- | --- |
| `number` | String | 备案编号. |
| `link` | String | 备案链接. |

___

## [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E9%85%8D%E7%BD%AE%E4%BE%8B%E5%AD%90) 配置例子

```
# Site 配置
site:
  subtitle: TriDiamond's Blog
  author: 三钻
  nick: TriDiamond
  description: 一位正在重塑知识的技术人 <br /> @ <b>公众号：技术银河</b>
  language: cn
  multi_language: true
  logo: https://image-website.com/path-to-image.jpg
  avatar: https://image-website.com/path-to-image.jpg
  beian: # 如果不需要可以让 number 和 link 保持空白
    number: "123123123123"
    link: 'https://link-to-beian.com'
  police_beian:
    number: "123123123123"
    link: 'https://link-to-police-beian.com'
```

## [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E6%8E%A8%E8%8D%90%E6%96%87%E7%AB%A0) 推荐文章

Aurora 主题在首页有推荐板块，任何文章都可以设置在这里显示显示。

要设置一篇文章在推荐板块中显示，只需在 Front-Meta 中添加一个 `feature: true` 属性即可。

例如:

```
---
title: Article Title
date: 2020-08-15 18:49:36
tags:
  - Tag
categories:
  - Cate
cover: https://cover.png
feature: true
---
```



# 菜单 | Hexo Aurora

> ## Excerpt
>
> 迈向未来的 Hexo 极光主题

---

## [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E8%8F%9C%E5%8D%95) 菜单

Aurora 主题的**菜单**是可以自主定义的，只需要通过在主题的 `_config.aurora.yaml` 中配置即可。

## [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E9%BB%98%E8%AE%A4%E8%8F%9C%E5%8D%95) 默认菜单

Aurora 拥有 3 个自带样式的页面，分别是**关于页**、**标签页**和**归档页**

首页和关于页默认是开启的，但是标签和归档页就可以通过修改主题配置里面的 `menu` 配置来开启或者关闭。

```
menu:
  About: false
  Tags: true
  Archives: true
```

如果把 `true` 改为 `false` 就会把特定的页面在导航中屏蔽掉。

## [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E8%87%AA%E5%AE%9A%E4%B9%89%E8%8F%9C%E5%8D%95) 自定义菜单

除了主题自带的默认页面可以在导航中显示之外，我们还可以添加自定义的页面和外部链接。

### [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E5%A4%96%E9%83%A8%E9%93%BE%E6%8E%A5) 外部链接

如果现在我们想添加一个通往我们 github 项目的外部链接，这个时候我们就可以在 menu 配置中这样写：

```
menu:
  Tags: true
  Archives: true
  # 一个 github 项目的外部链接
  Aurora:
    name: 'Aurora'
    path: 'https://github.com/Aurora/hexo-theme-Aurora'
```

自从版本 `v1.4.3`，外部链接也支持 `mailto` 链接。 这将把您的用户带到他们的电子邮件页面发送电子邮件。

```
menu:
  Tags: true
  Archives: true
  # External link for a github repo
  Email:
    name: 'Mail Me'
    path: 'mailto:code.tridiamond@gmail.com'
```

### [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E5%A4%9A%E7%BA%A7%E8%8F%9C%E5%8D%95) 多级菜单

有时候我们还可能想分组一些链接，把一些链接放到二级导航里面。没问题，Aurora 的菜单系统也是支持多级菜单的。要创建一个多级菜单，我们只需要在 menu 的链接中添加一个 `children` 属性即可。

比如，现在我们想把我们所有的 github 项目链接都放入一个 projects 的主导航之下。我们就可以这样配置我们的 menu 选项：

```
menu:
  Tags: true
  Archives: true
  # 多级 projects 菜单配置
  projects:
    name: 'Projects'
    children:
      obsidian:
        name: 'Obsidian Theme'
        path: 'https://github.com/tridiamond/hexo-theme-obsidian'
      Aurora:
        name: 'Aurora Theme'
        path: 'https://github.com/Aurora/hexo-theme-Aurora'
```

注意

顶级链接是不需要配置 `path` 属性的，因为当它被点击时是不会跳转页面的。

就算我们给顶级链接配置了 `path`，这个 path 地址也会被忽略的。

### [#](https://aurora.tridiamond.tech/zh/guide/menu.html#%E5%86%85%E9%83%A8%E9%93%BE%E6%8E%A5) 内部链接

提示

内部链接需要结合自定义页面使用，这部分的使用指南请移步到文档的[页面](https://aurora.tridiamond.tech/zh/guide/page.html)指南中详细了解。

## [#](https://aurora.tridiamond.tech/zh/guide/menu.html#i18n-%E8%8F%9C%E5%8D%95) I18n 菜单

由于主题支持 I18n 多语言，所以菜单名也支持多语言设置。目前主题支持菜单的英文和中文翻译。(_在不久的将来会支持更多。_)

要为菜单设置多语言，我们只需要配置 `i18n` 属性，而这个属性有**2 个选项**:

-   `cn` - 中文翻译
-   `en` - 英文翻译





# Markdown | Hexo Aurora

> ## Excerpt
>
> 迈向未来的 Hexo 极光主题

---

**更新记录**

> -   版本 `1.5.0+`
>     -   Aurora 添加了 markdown [自定义容器](https://aurora.tridiamond.tech/zh/guide/markdown.html#custom-containers).
>     -   Font-Meta 中的`Feature`属性会影响在置顶模式下的置顶状态

___

Aurora 主题有它自己的自定义前置元属性，他们是用来配置特定的功能。

### [#](https://aurora.tridiamond.tech/zh/guide/markdown.html#feature-%E5%B1%9E%E6%80%A7) Feature 属性

这个`feature`属性将允许 Aurora 引擎找到这些文章，并将它们添加到推荐列表或置顶列表数据中。使用[推荐布局模式](https://aurora.tridiamond.tech/zh/guide/theme.html#%E6%8E%A8%E8%8D%90%E5%B8%83%E5%B1%80%E6%A8%A1%E5%BC%8F)或[置顶布局模式](https://aurora.tridiamond.tech/zh/guide/theme.html#%E7%BD%AE%E9%A1%B6%E5%B8%83%E5%B1%80%E6%A8%A1%E5%BC%8F)。

___

## [#](https://aurora.tridiamond.tech/zh/guide/markdown.html#%E8%87%AA%E5%AE%9A%E4%B9%89%E5%AE%B9%E5%99%A8) 自定义容器

所有的自定义容器都使用这种格式:

```
:::[type] [title]
文本内容
:::
```

-   `type` 是容器的类型
-   `title` 是可选的，可以用来重命名容器的标题

### [#](https://aurora.tridiamond.tech/zh/guide/markdown.html#tip-%E5%AE%B9%E5%99%A8) Tip 容器

```
:::tip
Normal Tips Container
:::
```

![](https://aurora.tridiamond.tech/images/screenshots/tip.png)

如果你不想使用默认的标题`TIP`，你可以使用以下方法重命名你的容器标题:

```
:::tip Custom header

Custom header

- tips content
- tips new line

:::
```

![](https://aurora.tridiamond.tech/images/screenshots/tip-rename.png)

### [#](https://aurora.tridiamond.tech/zh/guide/markdown.html#warning-%E5%AE%B9%E5%99%A8) Warning 容器

```
:::warning
Warning!!!
:::
```

![](https://aurora.tridiamond.tech/images/screenshots/warning.png)

### [#](https://aurora.tridiamond.tech/zh/guide/markdown.html#danger-%E5%AE%B9%E5%99%A8) Danger 容器

![](https://aurora.tridiamond.tech/images/screenshots/danger.png)

### [#](https://aurora.tridiamond.tech/zh/guide/markdown.html#details-%E5%AE%B9%E5%99%A8) Details 容器

这是一种特殊类型的容器。如果你看过 GitHub 中的 `details` 容器，你可能会猜出它的功能是什么。

是的，您可以隐藏某些内容，并单击来展开它。

````
:::details Click to see more

Fusce rutrum venenatis eros in hendrerit. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nullam eget risus egestas, aliquet ipsum sed, volutpat tortor. Proin finibus tortor ac mauris finibus rutrum. Nullam tincidunt arcu eu urna ullamcorper, eu ultricies turpis ornare. Morbi id sollicitudin orci. Proin lobortis vehicula nibh a ornare. Cras sodales eu ligula quis fermentum. Proin eu ultrices leo, quis iaculis justo. Sed dictum, nulla sit amet imperdiet commodo, libero sapien semper justo, ut lobortis elit nunc vitae ante. Nullam lobortis odio quam, ac condimentum elit posuere vitae. Sed ornare, odio et rutrum varius, lorem eros gravida urna, in pharetra sapien justo non magna.

- details content
- details new line

```javascript
console.log('hello world')
```

:::
````

**关闭状态:**

![](https://aurora.tridiamond.tech/images/screenshots/detail.png)

**展开状态:**

![](https://aurora.tridiamond.tech/images/screenshots/detail-opened.png)
