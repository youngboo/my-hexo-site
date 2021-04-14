---
title: webpack错误日志
date: 2018-04-25 11:58:20
tags: [webpack]
categories: [前端]
---

如果我们在打包的入口js文件中import了css文件，并且想要把css文件作为 style 的内容插入到模版文件，这时候我们要用到webpack的css-loader和style-loader，前者用于在js中加载css，后者把加载的css作为style标签内容插入到html中。
在安装css-loader和style-loader插件然后import css文件：
require("../css/style.css");
运行后会报错：
![aaa](https://cdn.jsdelivr.net/gh/youngboo/image-hosting@master/20210414/aaa.28iw7ibivgro.png)
需要改为：require("style-loader!css-loader!../css/style.css");