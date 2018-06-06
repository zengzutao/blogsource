---
title: PWA 和 ServiceWorker
categories: ServiceWorker
author: Jack
tags:
    - ServiceWorker
    - PWA
cover_picture: images/trace.jpg
top: 0
---

> _**雄关漫道真如铁，而今迈步从头越。**_ —毛泽东

## Service Worker

### 一、定义

1.Chrome 团队提出和力推的一个 WEB API。
2.用于给 web 应用提供高级的可持续的后台处理能力。

### 二、特点

1.本质上充当Web应用程序与浏览器之间的代理服务器。
2.能够创建有效的离线体验。
3.只能使用HTTPS，拦截网络请求。
4.允许访问推送通知和后台同步API。
5.不能操作页面 DOM,但可以通过事件机制来处理。
6.结合 Fetch、Cache、Push、postMessage 和 Notification等API的能力

### 三、功能

1.离线缓存。
2.消息推送。
3.静默更新。

### 四、生命周期

1.下载。
2.安装。
3.激活。

* 备注：install -> installed -> actvating -> Active -> Activated -> Redundant

### 五、使用场景

1.后台数据同步。
2.响应来自其它源的资源请求。
3.集中接收计算成本高的数据更新，比如地理位置和陀螺仪信息，这样多个页面就可以利用同一组数据。
4.在客户端进行CoffeeScript，LESS，CJS/AMD等模块编译和依赖管理（用于开发目的）。
5.后台服务钩子。
6.自定义模板用于特定URL模式。
7.性能增强，比如预取用户可能需要的资源，比如相册中的后面数张图片。

## PWA（谷歌）

### 一、定义

1.Progressive Web Apps 渐进式增强 WEB 应用。
2.Service Worker API 为核心实现的 web 应用。

### 二、特点

1.渐进增强 – 能够让每一位用户使用，无论用户使用什么浏览器，因为它是始终以渐进增强为原则。
2.响应式用户界面 – 适应任何环境：桌面电脑，智能手机，笔记本电脑，或者其他设备。
3.不依赖网络连接 – 通过 Service Workers 可以在离线或者网速极差的环境下工作。
4.类原生应用 – 有像原生应用般的交互和导航给用户原生应用般的体验，因为它是建立在 app shell model 上的。
5.持续更新 – 受益于 Service Worker 的更新进程，应用能够始终保持更新。
6.安全 – 通过 HTTPS 来提供服务来防止网络窥探，保证内容不被篡改。
7.可发现 – 得益于 W3C manifests 元数据和 Service Worker 的登记，让搜索引擎能够找到 web 应用。
8.再次访问 – 通过消息推送等特性让用户再次访问变得容易。
9.可安装 – 允许用户保留对他们有用的应用在主屏幕上，不需要通过应用商店。
10.可连接性 – 通过 URL 可以轻松分享应用，不用复杂的安装即可运行。

#### 参考

* Service Worker的使用 、安全、桌面图标下次详谈
* http://lzw.me/a/pwa-service-worker.html
* https://developer.mozilla.org/zh-CN/docs/Web/API/Service_Worker_API