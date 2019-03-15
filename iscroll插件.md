---
title: iscroll插件
date: 2019-03-14 21:50:33
tags:
---
## iscroll插件的使用

#### iscroll实现了客户端原生滚动效果

html结构：

```html
<div id = "wrapper">
    <ul>
        <li>..</li>
        <li>..</li>
    </ul>
</div>
```

引入iscroll.js文件

`<script src:"js/iscroll.js"></script>`

初始化

```javascript
<script>
    var myScroll = new IScroll('#wrapper');
</script>
```

只有容器元素的第一个子元素才能滚动，其他子元素完全被忽略，当DOM准备完成后iscroll需要初始化，最保险的办法就是再`window`的`onload`事件中​启动​初始化。

脚本需要知道​滚动​区域​的宽和高。通过为滚动器容器增加`position:relative`可以解决大多数滚动大小计算问题:blush:

参数

```javascript
<script>
    var myScroll = new IScroll('#wrapper',{
        mouseWheel: true, //开启鼠标滚轮支持
        scrollbars: true //滚动条支持
    });
</script>
```

一些参数：

* 通过改变`CSStransform`的值来进行滚动 
* `scrollbars: true` 产生滚动条 父级要设相对定位
* `snap: true`能对齐到固定的位置或者元素 也可以跟元素`snap: li`

