# 闭包是什么

## 闭包的概念

闭包就是有权访问另一个函数作用域中变量的函数.

1. 闭包是定义在函数中的函数.
2. 闭包能访问包含它的函数的变量.
3. 即使包含它的函数执行完了,被闭包引用的变量也不会得到释放.

* __闭包引用的变量被放在`堆`中就好理解了__

## 事例

```JavaScript
function add() {
    var i = 0
    arr = [];
    for (; i < 10; i++) {
        arr.push(function () {  //arr数组添加10个函数.
            alert(i);
        });
    }
    return arr;
}
var temp = add();  //获得arr数组
temp[0]();  //取第一个函数值:10
```

也可以稍微改变一下使arr数组存放数值,而不是函数.

```JavaScript
function add() {
    var i = 0
    arr = [];
    for (; i < 10; i++) {
        arr.push(
            (function (n) {  //使一个匿名函数用括号包围可以得到函数变量,紧接着添加()运行函数.
                return function () {
                    alert(n);
                }
            })(i)
        );
    }
    return arr;
}
var temp = add();
temp[0]();
```

## 参考链接

[彻底搞清js中闭包(Closure)的概念 - tinkbell](https://www.cnblogs.com/tinkbell/p/3173293.html)

[立即执行函数表达式（IIFE）- 叙帝利](https://www.cnblogs.com/nzbin/p/5713406.html)
