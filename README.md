[Frange Zone](https://frangezone.github.io)
================================

> I never expect this becomes popular.

![](http://huangxuan.me/img/blog-desktop.jpg)


## 使用 Jekyll 搭建个人博客

* 开始
	* [博客介绍](#博客介绍)
	* [环境](#环境)
	* [开始](#开始)
	* [撰写博文](#撰写博文)
* 组件
	* [侧边栏](#侧边栏)
	* [推荐标签](#featured-tags)
	* [好友链接](#friends)
* 高级部分
	* [自定义](#customization)
	* [标题底图](#header-image)
	* [搜索展示标题-头文件](#seo-title)

## 开始

### 博客介绍

该博客基于 [GitHub Pages](https://pages.github.com/) 和 [Jekyll](http://jekyllcn.com/) 打造而成，是目前较为主流的搭建博客的方式之一。

### 环境

如果你安装了 [jekyll](http://jekyllcn.com/)，那你只需要在命令行输入`jekyll serve` 或 `jekyll s`就能在本地浏览器中输入`http://127.0.0.1:4000/`预览主题，对主题的修改也能实时展示（需要清理浏览器的本地缓存）。


### 开始

Jekyll主题的代码文件结构如下
```
|-- _config.yml         # 用来配置主页上的个人信息
|-- _include            # 
|-- _layouts            # 用来全局设置各类页面的布局
|-- _posts          # 保存已经写好的md格式的文章
|-- css
|-- fonts
|-- img
```

你可以通过修改 `_config.yml`文件来轻松的开始搭建自己的博客:

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
Jekyll官方网站还有很多的参数可以调，比如设置文章的链接形式...网址在这里：[Jekyll - Official Site](http://jekyllrb.com/) 中文版的在这里：[Jekyll中文](http://jekyllcn.com/).



### 撰写博文

要发表的文章一般以 **Markdown** 的格式放在这里`_posts/`，你只要看看这篇模板里的文章你就立刻明白该如何设置。

yaml 头文件长这样:

```
---
layout:     post
title:      博客迁移
subtitle:   "HelloWorld，Again"       # 记得使用引号
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

## 组件

### 侧边栏

设置是在 `_config.yml`文件里面的`Sidebar settings`那块。

```
# Sidebar settings
sidebar: true  # 添加侧边栏
sidebar-about-description: "简单的描述一下你自己"
sidebar-avatar: /img/avatar-by.jpg     # 你的个人头像，请使用绝对地址.注意：名字区分大小写！后缀名也是
```

侧边栏是响应式布局的，当屏幕尺寸小于992px的时候，侧边栏就会移动到底部。具体请见bootstrap栅格系统 <http://v3.bootcss.com/css/>



### Featured Tags

这个模块现在是独立的，可以呈现在所有页面，包括主页和发表的每一篇文章标题的头上。

```
# Featured Tags
featured-tags: true  
featured-condition-size: 1     # A tag will be featured if the size of it is more than this condition value
```

唯一需要注意的是`featured-condition-size`: 如果一个标签的 size ，也就是使用该标签的文章数大于上面设定的条件值，这个标签就会在首页上被推荐。
 
内部有一个条件模板 `{% if tag[1].size > {{site.featured-condition-size}} %}` 是用来做筛选过滤的.

### Friends

友链会在所有页面显示。

设置是在 `_config.yml` 文件里面的 `Friends` 那块，自己 DIY 就行。

```
# Friends
friends: [
    {
        title: "xzd",
        href: "https://github.com/xzd1621"
    },
    {
        title: "Apple",
        href: "https://www.apple.com/"
    }
]
```

## 高级部分

### 定制化

如果你喜欢折腾，你可以去自定义这个模板的 Code。

如果你可以理解 `_include/` 和 `_layouts/`文件夹下的代码（这里是整个界面布局的地方），你就可以使用 Jekyll 使用的模版引擎 [Liquid](https://github.com/Shopify/liquid/wiki)的语法直接修改/添加代码，来进行更有创意的自定义界面啦！

### Header Image

博客每页的标题底图是可以自己选的，看看几篇示例post你就知道如何设置了。
  
标题底图的选取完全是看个人的审美了。每一篇文章可以有不同的底图，你想放什么就放什么，最后宽度要够，大小不要太大，否则加载慢啊。

> 上传的图片最好先压缩，这里推荐 imageOptim 图片压缩软件，让你的博客起飞。

但是需要注意的是本模板的标题是**白色**的，所以背景色要设置为**灰色**或者**黑色**，总之深色系就对了。当然你还可以自定义修改字体颜色，总之，用github pages就是可以完全的个性定制自己的博客。

### SEO Title

我的博客标题是 **“Frange Zone”** 但是我想要在搜索的时候显示 **“Xu's Blog | Frange Zone”** ，这个就需要 SEO Title 来定义了。

其实这个 SEO Title 就是定义了<head><title>标题</title></head>这个里面的东西和多说分享的标题，你可以自行修改的。

## 致谢

1. 该模板 Fork 自 [Hux](https://github.com/Huxpro/huxpro.github.io) 这里, 感谢该作者。 
2. 感谢 Jekyll、Github Pages 和 Bootstrap!
3. 博客的搭建参考了 [Yousanflics](https://blog.csdn.net/siwangtt/article/details/112943095)和 [李小肥的YY](https://blog.csdn.net/siwangtt/article/details/112943095) 的教程，十分感谢！

## License

遵循 MIT 许可证。有关详细,请参阅 [LICENSE](https://github.com/qiubaiying/qiubaiying.github.io/blob/master/LICENSE)。
