---
title: Hexo环境搭建及文章置顶
categories: Hexo
author: Jack
tags:
    - Hexo
    - 文章置顶
cover_picture: images/code.jpg
top: 1
---

> _**路漫漫其修远兮，吾将上下而求索。**_ —屈原

## 环境搭建

### NVM安装及Node安装源配置（使用国内镜像）

``` bash
下载NVM并安装，NVM下载地址：https://github.com/coreybutler/nvm-windows/releases
配置node安装源：nvm node_mirror https://npm.taobao.org/mirrors/node/
配置npm安装源：nvm npm_mirror https://npm.taobao.org/mirrors/npm/
使用NVM安装Node：nvm install nodejs-version
使用node：nvm use nodejs-version
安装yarn：https://yarnpkg.com/latest.msi
```

### Hexo安装和更换博客主题

``` bash
安装Hexo命令行工具：npm install hexo-cli -g
新建Hexo项目：hexo init blog
下载主题文件放置到blog中的themes目录下
在blog的根目录下找到 _config.yml 配置文件将 theme: 你想安装的主题
```

More info: [More](https://hexo.io)

### 博客部署及搜索

``` bash
博客静态文件生成：hexo generate 简写：hexo g
博客文件本地预览：hexo server 简写：hexo s
部署：将生成好的静态文件上传至配置好的服务中即可;
安装搜索插件(需修改配置文件)：npm i -S hexo-generator-json-content
```

More info: [More](https://hexo.io/zh-cn/docs/index.html)

## 文章置顶

``` bash
找到该文件：generator.js(node_modules/hexo-generator-index/lib/generator.js)
在generator.js中添加如下代码：
posts.data = posts.data.sort(function(first, second) {
    if (first.top && second.top) { // 两篇文章top都有定义
        return first.top == second.top ? second.date - first.date : second.top - first.top //若top值一样则按照文章日期降序排, 否则按照top值降序排
    } else if (first.top && !second.top) { // 以下是只有一篇文章top有定义，将有top的排在前面
        return -1;
    } else if (!first.top && second.top) {
        return 1;
    } else {
        return second.date - first.date;  // 都没定义top，按照文章日期降序排
    }
});
在文章头部加入 top: 数字；值越大，文章越靠前;
```