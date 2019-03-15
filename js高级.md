---
title: js高级
date: 2019-01-18 16:51:56
tags:
- JavaScript
---
#### 1.0  组合继承

​	通过 call 方法调用父类型的构造函数，实现了属性的继承

​	通过父类型的 实例对象 把子类型的原型替换掉，并且手动修改构造器(constructor)



​	为什么要用继承？

​		提取多个 类型的 属性和方法，减少代码冗余



#### 2.0 函数的创建方式



```javascript
// 第一种 函数声明
function fn() {
  	console.log("afsa")
}
fn()

// 第二种 函数表达式
var fn2 = function() {
  console.log("afsa")
}
fn2()

// 第三种 new Function()
// 这种方式将要执行的语句通过字符串的形式写在构造函数的括号内，不推荐使用
```



​	通过介绍第三种方式，得知函数也是一个对象

​	那么如果是个对象，就会有对应的成员，比如属性和方法



#### 2.0 函数的内置方法



​	bind() 

​		改变this的指向，不调用函数

​		注意两种方式

​			1， 函数有名字的时候，需要使用函数名调用，会返回一个新的函数

​			2，如果是匿名函数，就是没有名字的函数，就直接在函数体后面打点调用，比较推荐

​	call()   apply()

​		改变this的指向，会立即调用函数

​		注意点：

​			第一个参数都是表示函数内部this需要指向的对象

​			后面的参数call方法传的是零散的，而apply方法传入的是数组



#### 3.0 关于this的指向

​		要了解函数的调用形式

```javascript
     //1 普通函数调用    this指向window
     function fn() {
       console.log(this);
     }
     fn();

    // 2 方法调用     this指向调用该方法的对象
     var obj = {
       fn: function () {
         console.log(this);
       }
     }
     obj.fn();

    // 3 作为构造函数调用   构造函数内部的this指向由该构造函数创建的对象
    function Student() {
      this.aaa = "abc";
      this.con = function() {
        console.log(this.aaa)
      }
    }
    var s1 = new Student();
    s1.con()


    // 4 作为事件的处理函数   触发该事件的对象
    btn.onclick = function() {
      console.log(this);
    }

    // 5 作为定时器的参数   this指向window
    setInterval(function () {
      console.log(this);
    }, 1000);
```



> ### 函数内部的this，是由函数调用的时候来确定其指向的	

​	重点：

​		1， 有没有调用，

​		2，有没有对象的参与



#### 4.0 高阶函数

##### 4.1 将函数作为参数

​	回调函数。

##### 4.2 将函数作为返回值

​	会出现闭包

​	









