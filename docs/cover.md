# 第四天知识点

## 循环的嵌套
```js
	for(var i = 0; i < 5; i++){
		for(var i = 0; i < 5; i++){
			//需要执行的语句
		}
	}
```
!>循环的嵌套，外层控制行，内部控制列
## 循环嵌套的应用
```js
三角形
	for(var j = 0; j < 5; j++){
		for(var i = 0; i < j+1; i++){
			document.write("*")
		}
		document.write("<br>")
	}
```
```js
梯形
	for(var j = 0; j < 5; j++){
		for(var i = 0; i < j+5; i++){
			document.write("*")
		}
		document.write("<br>")
	}
```
```js
//阶乘  1*1 1*2 1*2*3
	var sum = 0;
        for(var j = 1; j < 5; j++){
            var a = 1;
            for(var i = 1; i <= j; i++){
                a = a*i;
            }
            sum+=a;
        }
        console.log(sum);
```
```js
//乘法口诀表 
	for(var i = 1; i <= 9; i++) {
            for(var j = 1; j <= i; j++) {
                document.write(i+"*"+j+"="+i*j+"&nbsp;&nbsp;&nbsp;");
            }
            document.write("<br>")
        }
```
```js
//画棵树 tree
	for(var i = 1; i <= 9; i++) {
            for(var j = 9; j >= i; j--) {
                document.write(""+"&nbsp;&nbsp;");
            }
            for(var s = 1; s <= i+5; s++) {
                document.write("*"+"&nbsp;&nbsp;&nbsp;");
            }
            document.write("<br>")
        }
        for(var i = 1; i <= 9; i++) {
            for(var j = 9; j >= i; j--) {
                document.write(""+"&nbsp;&nbsp;");
            }
            for(var s = 1; s <= i+5; s++) {
                document.write("*"+"&nbsp;&nbsp;&nbsp;");
            }
            document.write("<br>")
        }
        for(var a = 0; a < 10;a++){
            for(var w = 0; w < 3;w++){
                document.write("&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;");
            }
            for(var t = 0; t < 10;t++){
                document.write("*");
            }
            document.write("<br>")
        }
```
## 函数 
### 1、概念
	- 函数表示功能
	- 封装的一个具有某个功能的，可以被执行或者调用的代码块
### 2、特点
	- 忽略细节
	- 重复调用
	- 选择执行
### 3、如何创建一个函数与使用函数

``` js
声明式创建
	function name（params）{
	
	}
	
赋值式创建
	var func = function() {
	
	}
执行函数的方法
	函数名（）  直接执行
	行为（事件）执行
	按钮.点击行为 = 函数名 /  按钮.点击行为 = function（）{}
	
```
### 4、函数的分类

- 有名函数：function name（）{}

>	正常函数，正常使用

- 无名函数：function（）{}

>	非正常函数，不允许直接存在，只能作为值存在  
>	
>	1、作为赋值式创建函数的值	（var a = function(){}  ）
>	
>	2、作为匿名函数的函数体	 （function（）{}）（）
>	
>	3、作为事件的处理函数存在   	按钮.点击行为 = function（）{}

!>	4、作为函数的参数  （回调函数）

!>	5 、作为函数的返回值  （闭包函数）

- 匿名函数：（function（）{}）（）

> 自动执行

> 利用匿名函数，生成一个独立的区域（作用域）；
	
### 5、函数的入口 - 参数

- 定义函数时，接收参数，形参
- 执行函数时，发送参数，实参
- 实参传给形参，将实参赋值给形参，形参类似于变量
- 传什么数据： 什么数据都可以传
- 传多少数据： 没有限制
- 关系：
	- 数量一致的时候，从左到右一一对应
	- 形参多的时候，从左到右一一赋值，实参不够的就是undefined
	- 实参多的时候，从左到右边分，多了的传不上
		- 但是函数时例外，多于的函数被存在了函数内部的内置对象arguments中  	
