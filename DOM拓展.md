---
title: DOM拓展
date: 2019-03-14 19:31:57
tags:
---
###DOM拓展

1. 获取元素

   `document.querySelector() //获取单个元素，如果获取的不止一个则返回满足条件的第一个。`

   `docment.querySlectorAll() //获取满足条件的所有元素。`

2. 样式操作

   `classList.add() //为元素添加指定名称的样式，一次只能添加一个样式。`

   `classList.item() //获取样式`

   `classList.remove() //为元素移除指定名称的样式，一次只能移除一个。`

   `classList.toggle() //切换元素样式，如果之前没有则添加，有则移除。`

   `classList.contains() //判断元素是否包含此样式名，返回true/false`

3. 自定义属性

    ```javascript
   <p data-school-name = "wut" data-wut = "awqe"> wut </p>
    ```

   获取自定义属性，因为**dataset**是一个对象，有两种获取方法：

   1. `dataset["schoolName"]`

   2. `dataset.schoolName` 

      