[Frange Zone](https://frangezone.github.io)
================================

> I never expect this becomes popular.

![](http://huangxuan.me/img/blog-desktop.jpg)


[User Manual 👉](_doc/Manual.md)
--------------------------------------------------

## 目录
* [博客介绍](#博客介绍)
* [项目配置](#项目配置)
* [开始](#开始)
* [撰写博文](#撰写博文)
* [定制化](#定制化)

### 博客介绍

该博客基于 [GitHub Pages](https://pages.github.com/) 和 [Jekyll](http://jekyllcn.com/) 打造而成，是目前较为主流的搭建博客的方式之一。

### 项目配置

Jekyll主题的代码文件结构如下
<br/><img src="http://frangezone.github.io/img/Jekyll_theme_code.png" width="200"/><br/>
`_posts`保存已经写好的md格式的文章

`assets文件夹`保存一些图片和css的一些文件

`_config.yml`用来配置主页上的个人信息

### 开始

你可以通用修改 `_config.yml`文件来轻松的开始搭建自己的博客:

```
# Site settings
title: Frange Zone                    # 你的博客网站标题
SEOTitle: Xu's Blog | Frange Zone		# SEO 标题
description: "Forever Young"	   	   # 随便说点，描述一下

# SNS settings      
github_username: frangezone     # 你的github账号

# Build settings
# paginate: 10              # 一页你准备放的文章数目
```


### 撰写博文

要发表的文章一般以 **Markdown** 的格式放在这里`_posts/`，你只要看看这篇模板里的文章你就立刻明白该如何设置。

yaml 头文件长这样:

```
---
layout:     post
title:      博客迁移
subtitle:   "HelloWorld，Again"       #记得使用引号
date:       2021-08-24
author:     frange
header-img: img/post-bg-rwd.jpg
catalog: 	 true
tags:
    - 生活
    - 代码
    - 随想
---

```

### 定制化

如果你喜欢折腾，你可以去自定义这个模板的 Code。

如果你可以理解 `_include/` 和 `_layouts/`文件夹下的代码（这里是整个界面布局的地方），你就可以使用 Jekyll 使用的模版引擎 [Liquid](https://github.com/Shopify/liquid/wiki)的语法直接修改/添加代码，来进行更有创意的自定义界面啦！



## 致谢

1. 该模板 Fork 自 [Hux](https://github.com/Huxpro/huxpro.github.io) 这里, 感谢该作者。 
2. 感谢 Jekyll、Github Pages 和 Bootstrap!
3. 博客的搭建参考了 [Yousanflics](https://blog.csdn.net/siwangtt/article/details/112943095)和 [李小肥的YY](https://blog.csdn.net/siwangtt/article/details/112943095) 的教程，十分感谢！

## License

遵循 MIT 许可证。有关详细,请参阅 [LICENSE](https://github.com/qiubaiying/qiubaiying.github.io/blob/master/LICENSE)。
