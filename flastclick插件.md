---
title: flastclick插件
date: 2019-03-14 21:49:42
tags:
---
##touch事件点透问题，应用fastclick插件解决

1. 点透问题的原理

   当通过touch事件来点击按钮的时候，此时下一层的按钮也会被选中。

2. 如何解决

   touch 会产生点透，click不会产生点透但是会产生300延迟，需要通过fastclick来解决

3. fastclick使用方法

   引入fastclick.js

   ```javascript
   <script src="js/fastclick.js"></script>
   ```

   初始化(原生写法)

   ```javascript
   if('addEventListener' in document){
       document.addEventListener('DOMContentLoaded',function(){
           fastClick.attach(document.body) //此处document.body为页面所有元素都绑定fastclick
       },false);
   }
   ```

   jQuery写法

   ```	javascript
   $(function(){
       FastClick.attach(document.body);
   })
   ```

4. 然后就可以绑定事件了，之后直接使用封装好的click绑定事件

   ```javascript
   li.addEventListener("click",function(){
       li.style.visibility = 'hidden';
   })
   ```

   