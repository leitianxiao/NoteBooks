# JavaScript基础

## JavaScript介绍

### JavaScript是什么

> JavaScript 是运行在**客户端**的一种**脚本语言**。

Netscape在最初将其脚本语言命名为LiveScript，后来因与Sun合作之后将其改名为JavaScript。JavaScript最初受Java启发而开始设计，目的之一就是看上去像Java。因此语法上有类似之处，一些名称和命名规范也借自Java。但只是名字很像。

Java的解释器被称为JavaScript引擎，为浏览器的一部分，广泛用于客户端脚本语言，最早是在HTML网页上使用，用来增加动态功能。

JavaScript是什么：

1. 是一门脚本语言
2. 是一门解释性语言
3. 是一门动态类型的语言
4. 是一门基于对象的语言

编译语言：需要把代码翻译成计算机所认知的二进制语言，才能执行。

脚本语言：不需要编译，直接执行。

常见的脚本语言：t-sql、cmd

### JavaScript与HTML、CSS的区别

HTML：标记语言，展示数据的

CSS：美化页面

JS：用户和浏览器交互

### JavaScript现在的意义（应用场景）

1. 网页特效

2. 服务端开发（Node.js）

3. 命令行工具（Node.js）

4. 桌面程序（Electron）

5. App（Cordova）

6. 控制硬件-物联网

7. 游戏开发(cocos2d.js)

   

## JavaScript组成

JavaScript分为三个部分：

1. ECMAScript—js的基本语法

2. DOM—Document Object Model 文档对象模型

3. BOM—Browser Object Modern 浏览器对象模型



### ECMAScript

定义了JavaScript的语法规范  

JavaScript的核心，描述了语言的基本语法和数据类型，ECMAScript是一套标准，定义了一种语言的标准与具体实现无关

### DOM文档对象模型

一套操作页面元素的API

DOM可以把HTML看做是文档树，通过DOM提供的API可以对树上的节点进行操作

### BOM浏览器对象模型

一套操作浏览器功能的API

通过BOM可以操作浏览器窗口，比如：弹出框、控制浏览器跳转、获取分辨率等



## JavaScript代码书写位置

js代码可以写在三个地方：

1. html文件中,`<script>`标签中
2. html的标签中
3. js文件中，需要在html页面中引入 `<script>`标签的`src`属性中



js代码的注意问题

1. 在一对`<script>`的标签中有错误的js代码，那么该错误的代码后面的js代码不会执行。
2. 如果第一对`<script>`标签中有错误，不会影响后面的`<script>`中的js代码执行。
3. `<script>`标准写法是`<script type="text/javascript"> </script>`或`<script language="Javascript"> </script>`，但是如果使用HTML5的写法，type、language可以省略。
4. `<script>`在页面中可以出现多对。
5. `<script>`一般放在body的标签最后，有时也放在head标签中。
6. 如果这对`<script>`标签是引入外部js文件的作用，那么这对标签中不要写任何js代码，如果要写，重新写一堆`<script>`标签。



## 计算机组成

### 软件

- 应用软件：浏览器(Chrome/IE/Firefox)、QQ、Sublime、Word
- 系统软件：Windows、Linux、mac OSX

### 硬件

- 三大件：CPU、内存、硬盘    -- 主板
- 输入设备：鼠标、键盘、手写板、摄像头等
- 输出设备：显示器、打印机、投影仪等

![](../../110 - Work -Src | 源 /compute.png)

## 变量

### 什么是变量

- 什么是变量

  变量是计算机内存中存储数据的标识符，根据变量名称可以获取到内存中存储的数据
  
- 为什么要使用变量

  使用变量可以方便的获取或者修改内存中的数据



### 如何使用变量

- var声明变量

```javascript
var age;
```

- 变量的赋值

```javascript
var age;
age = 18;
```

- 同时声明多个变量

```javascript
var age, name, sex;
age = 10;
name = 'zs';
```

- 同时声明多个变量并赋值


```javascript
var age = 10, name = 'zs';
```

### 变量的命名规则和规范

- 规则 - 必须遵守的，不遵守会报错

  - 由字母、数字、下划线、$符号组成，不能以数字开头

  - 不能是关键字和保留字，例如：for、while。

  - 区分大小写

- 规范 - 建议遵守的，不遵守不会报错

  - 变量名必须有意义
  - 遵守驼峰命名法。首字母小写，后面单词的首字母需要大写。例如：userName、userPassword

- 变量声明和变量初始化
  - 变量声明：有var，有变量名，没有值
  - 变量初始化：有var，有变量名，有值

## 注释

### 单行注释

一般用在一行代码的上面

```javascript
//这是单行注释
```

### 多行注释

一般是用在函数或者一段代码上面

```javascript
/*
这是多行注释
*/
```

## 数据类型

原始数据类型：number、string、boolean、null、undefined、object

### Number

数字类型，整数和小数。

- 进制

  - 二进制：遇2进1，计算机只认识二进制，要将其他进制转换成二进制，计算机才能识别。

    ```
    00000001——1
    00000010——2
    00000011——3
    ```

  - 八进制：遇8进1，`0`开头

    ```
    00000001——1
    00000002——2
    00000003——3
    00000004——4
    00000005——5
    00000006——6
    00000007——7
    00000010——8
    ```

  - 十进制：遇10进1，生活中用的就是十进制

    ```
    00000001——1
    00000008——8
    00000009——9
    00000010——10
    00000011——11
    ```

  - 十六进制：遇f进1，0-9以及a-f，用`0x`开头

    ```
    00000001——1
    00000009——9
    0000000a——10
    0000000b——11
    0000000f——15
    00000010——16
    ```

- 数字类型的范围

  最小值：`console.log(Number.MIN_VALUE);//5e-324`

  最大值：`console.log(Number.MAX_VALUE);//1.7976931348623157e+308`

  无穷大：infinity

  无穷小：-infinity

- 数值判断
  
  - NaN：not a number
  
  - NaN 与任何值都不相等，包括他本身
  
    ```javascript
    var num;
    console.log(num+10==NaN);//false
    ```
  
  - isNaN: is not a number
  
    如何验证结果是不是NaN，使用`isNaN()`
  
    ```javascript
    var num;
    console.log(isNaN(num+10));//true
    ```

- 语言缺陷：不要用小数去验证小数

  ```javascript
  var x=0.1;
  var y=0.2;
  var sum=x+y;
  console.log(sum);//0.30000000000000004
  console.log(sum==0.3);//false,js语言本身的bug
  ```

### String

字符串类型，值一般用单引号或双引号括起来。

- 字符串长度

  length属性用来获取字符串的长度

  ```javascript
  var str = 'Hello World';
  console.log(str.length);
  ```

- 字符串拼接

  字符串拼接使用 + 连接

  ```javascript
  console.log(11 + 11);
  console.log('hello' + ' world');
  console.log('100' + '100');
  console.log('11' + 11);
  console.log('male:' + true);
  ```

  1. 两边只要有一个是字符串，那么+就是字符串拼接功能
  2. 两边如果都是数字，那么就是算术功能。

### Boolean

布尔类型，只有两个值，true(1)、false(0)。

### Null

空类型，值只有一个null，一个对象指向了空，此时赋值为null。要让变量为null，只能通过赋值。

### Undefined

未定义，值只有一个undefined

什么情况下结果是undefined？

1. 变量声明了，没有赋值，结果是undefined；
2. 函数没有明确返回值，如果接收了，结果也是undefined。

```javascript
var num;

console.log(num);//输出：undefined

console.log(num+10);//输出：NaN  //Not an Number 不是一个数字
```

如果一个变量的结果是undefined，和一个数字进行计算，结果是NaN，不是一个数字，也没有意义。

### Object

对象，后面讲。

### 如何获取变量的数据类型

使用`typeof`来获取。

语法：

`typeof 变量名` 

`typeof(变量名)` 

```javascript
  <script>
      var num=20;
      var str="hello!";
      var bol=true;
      var undef;
      var nul=null;
      var obj=new Object();
      console.log(typeof num);//number
      console.log(typeof str);//string
      console.log(typeof bol);//boolean
      console.log(typeof undef);//undefined
      console.log(typeof nul);//object,null是指一个对象指向了空，所以类型是对象。
      console.log(typeof obj);//object
  </script>
```

## 数据类型转换

### 转为数字类型

#### parseInt() 转为整数

```javascript
var num1 = parseInt("12.3abc");  // 返回12，如果第一个字符是数字会解析知道遇到非数字结束
var num2 = parseInt("abc123");   // 返回NaN，如果第一个字符不是数字或者符号就返回NaN
```

#### parseFloat() 转为小数

```javascript
console.log(parseFloat("10"));//10
console.log(parseFloat("10.98.11"));//10.98
console.log(parseFloat("10.98edef"));//10.98
console.log(parseFloat("109385ggg"));//109385
console.log(parseFloat("fds10.1ggg"));//NaN
```

`parseFloat`会解析第一个`. `遇到第二个`.`或者非数字结束如果解析的内容里只有整数，解析成整数。

#### Number() 转为数字

```javascript
console.log(Number("10"));//10
console.log(Number("10.121"));//10.121
console.log(Number("10.98.11"));//NaN
console.log(Number("10.98edef"));//NaN
console.log(Number("109385ggg"));//NaN
console.log(Number("fds10.1ggg"));//NaN
```

比上两种方式严格

### 转为字符串类型

#### .toString()

```javascript
var num=10;
console.log(num.toString());//10
```

#### String()

```javascript
var num=10;
console.log(String(num));//10
```

区别：

如果变量有意义，使用`.toString()`转换；

如果变量没有意义，如null、undefined，使用`string()`转换，使用`.toString()`会报错。

一般来说，不会转没有意义的变量，所以主要用`.toString()`，为了保险可以用`.toString()`。

### 转为布尔类型

#### Boolean();

```javascript
console.log(Boolean(1));//true,非0数字都是true
console.log(Boolean(0));//false
console.log(Boolean(11));//true
console.log(Boolean(-11));//true
console.log(Boolean("hello"));//true,非空字符串也是true
console.log(Boolean(""));//false,空字符串是false
console.log(Boolean(null));//false,没有意义的是false
console.log(Boolean(undefined));//false,没有意义的是false
```

## 操作符

### 算数运算符

`+、-、*、/、%`

- 算数运算表达式

由算术运算符连接起来的表达式

### 一元运算符

只需要一个操作数就可以运算的符号` ++、--`

` ++`可以分为前`++`和后`++`

` --`可以分为前` --`和后` --`

如果没有参与运算，在前在后结果都一样。

num++ +10; //++在后，如果参与运算，先运算，再自身加1

++num +10; //++在前，如果参与运算，先自身加1，再运算

### 二元运算符

只需要两个操作数就可以运算的符号

### 三元运算符

只需要三个操作数就可以运算的符号

### 复合运算符（赋值运算符）

`+=、-=、*=、/=、%=`

- 复合运算表达式

由复合运算符连接的表达式

### 关系运算符

`>、<、>=、 <=、 ==(不严格，比较值)、===(严格，判断类型和值)、!=、!==`

- 关系运算表达式

由关系运算符连接的表达式，值是true或false

### 逻辑运算符

&&——逻辑与——>并且

|| ——逻辑或——>或者

！ ——逻辑非——>取反

- 逻辑运算表达式

由逻辑运算符连接的表达式。

`表达式1&&表达式2` 如果有1个表达式为false，则为false，两个表达式为ture才为true

`表达式1||表达式2` 如果一个表达式为true，则为true，两个表达式都为false才为false

`!表达式1` 如果表达式1为ture，则为false，如果表达式1为false，则为true

### 运算符的优先级

优先级从高到低：

  		1. ()  优先级最高
  		2. 一元运算符  ++   --   !
  		3. 算数运算符  先*  /  %   后 +   -
  		4. 关系运算符  >   >=   <   <=
  		5. 相等运算符   ==   !=    ===    !==
  		6. 逻辑运算符 先&&   后||
  		7. 赋值运算符

例：

`4 >= 6 || '人' != '阿凡达' && !(12 * 2 == 144) && true`

`false || true && true && true && true`——>true

## 表达式和语句 

### 表达式

>一个表达式可以产生一个值，有可能是运算、函数调用、有可能是字面量。表达式可以放在任何需要值的地方。

### 语句

>语句可以理解为一个行为，循环语句和判断语句就是典型的语句。一个程序有很多个语句组成，一般情况下;分割一个一个的语句。

## 流程控制

>程序的三种基本结构

### 顺序结构

 从上到下执行的代码就是顺序结构

**程序默认就是由上到下顺序执行的**

### 分支结构	

根据不同的情况，执行对应代码

### 循环结构

循环结构：重复做一件事情

## 分支结构

### if语句

语法结构

```javascript
//第一种
if (/* 条件表达式 */) {
  // 执行语句
}

//第二种
if (/* 条件表达式 */){
  // 成立执行语句
} else {
  // 否则执行语句
}

//第三种
if (/* 条件1 */){
  // 成立执行语句
} else if (/* 条件2 */){
  // 成立执行语句
} else if (/* 条件3 */){
  // 成立执行语句
} else {
  // 最后默认执行语句
}
```

### 三元运算符
	表达式1 ? 表达式2 : 表达式3

是对if……else语句的一种简化写法。

```javascript
var num=prompt("请输入一个数：");
var pri=num%2==0?"这是一个偶数":"这是一个奇数";
console.log(pri);
```

### switch语句

语法格式:
```javascript
switch (expression) {
  case 常量1:
    语句;
    break;
  case 常量2:
    语句;
    break;
  case 常量3:
    语句;
    break;
  …
  case 常量n:
    语句;
    break;
  default:
    语句;
    break;
}
```
break可以省略，如果省略，代码会继续执行下一个case
switch 语句在比较值时使用的是全等操作符, 因此不会发生类型转换（例如，字符串'10' 不等于数值 10）



## 循环结构

> 在javascript中，循环语句有三种，while、do..while、for循环。

### while语句

基本语法：

```javascript
// 当循环条件为true时，执行循环体，
// 当循环条件为false时，结束循环。
while (循环条件) {
  //循环体
  //计数器++
}
```

代码示例：

```javascript
// 计算1-100之间所有数的和
// 初始化变量
var i = 1;
var sum = 0;
// 判断条件
while (i <= 100) {
  // 循环体
  sum += i;
  // 自增
  i++;
}
console.log(sum);
```

### do...while语句

> do..while循环和while循环非常像，二者经常可以相互替代，但是do..while的特点是不管条件成不成立，都会执行一次。

基础语法：

```javascript
do {
  // 循环体;
  //计数器++
} while (循环条件);
```

代码示例：

```javascript
// 初始化变量
var i = 1;
var sum = 0;
do {
  sum += i;//循环体
  i++;//自增
} while (i <= 100);//循环条件
```

### for语句

>  while和do...while一般用来解决无法确认次数的循环。for循环一般在循环次数确定的时候比较方便

for循环语法：

```javascript
// for循环的表达式之间用的是;号分隔的，千万不要写成,
for (初始化表达式1; 判断表达式2; 自增表达式3) {
  // 循环体4
}
```

执行顺序：1243  ----  243   -----243(直到循环条件变成false)

1. 初始化表达式
2. 判断表达式
3. 自增表达式
4. 循环体

案例：

```
打印1-100之间所有数
求1-100之间所有数的和
求1-100之间所有数的平均值
求1-100之间所有偶数的和
同时求1-100之间所有偶数和奇数的和
打印正方形
// 使用拼字符串的方法的原因
// console.log 输出重复内容的问题
// console.log 默认输出内容介绍后有换行
var start = '';
for (var i = 0; i < 10; i++) {
  for (var j = 0; j < 10; j++) {
    start += '* ';
  }
  start += '\n';
}
console.log(start);
打印直角三角形
var start = '';
for (var i = 0; i < 10; i++) {
  for (var j = i; j < 10; j++) {
    start += '* ';
  }
  start += '\n';
}
console.log(start);

打印9*9乘法表
var str = '';
for (var i = 1; i <= 9; i++) {
  for (var j = i; j <=9; j++) {
    str += i + ' * ' + j + ' = ' + i * j + '\t';
  }
  str += '\n';
}
console.log(str);
```

作业：

```
求1-100之间所有数的乘积
求1-100之间所有奇数的和
计算1-100之间能3整除的数的和
计算1-100之间不能被7整除的数的和
// 讲解思路。如果不会写程序，可以先把数学公式准备好
本金10000元存入银行，年利率是千分之三，每过1年，将本金和利息相加作为新的本金。计算5年后，获得的本金是多少？
有个人想知道，一年之内一对兔子能繁殖多少对？于是就筑了一道围墙把一对兔子关在里面。已知一对兔子每个月可以生一对小兔子，而一对兔子从出生后第3个月起每月生一对小兔子。假如一年内没有发生死亡现象，那么，一对兔子一年内（12个月）能繁殖成多少对？（兔子的规律为数列，1，1，2，3，5，8，13，21）
```


### continue和break

> break:立即跳出整个循环，即循环结束，开始执行循环后面的内容（直接跳到大括号）
>
> continue:立即跳出当前循环，继续下一次循环（跳到i++的地方）

案例：

```javascript
求整数1～100的累加值，但要求碰到个位为3的数则停止累加
求整数1～100的累加值，但要求跳过所有个位为3的数
```

作业：

求1-100之间不能被7整除的整数的和（用continue）
求200-300之间所有的奇数的和（用continue）
求200-300之间第一个能被7整数的数（break）

### 调试

- 过去调试JavaScript的方式
  - alert()
  - console.log()
- 断点调试

>断点调试是指自己在程序的某一行设置一个断点，调试时，程序运行到这一行就会停住，然后你可以一步一步往下调试，调试过程中可以看各个变量当前的值，出错的话，调试到出错的代码行即显示错误，停下。

- 调试步骤

```javascript
浏览器中按F12-->sources-->找到需要调试的文件-->在程序的某一行设置断点-->刷新页面即可观察
```

- 调试中的相关操作

```javascript
Watch: 监视，通过watch可以监视变量的值的变化，非常的常用。
F10: 程序单步执行，让程序一行一行的执行，这个时候，观察watch中变量的值的变化。
F8：跳到下一个断点处，如果后面没有断点了，则程序执行结束。
```

tips: ***监视变量，不要监视表达式，因为监视了表达式，那么这个表达式也会执行。***

1. 代码调试的能力非常重要，只有学会了代码调试，才能学会自己解决bug的能力。初学者不要觉得调试代码麻烦就不去调试，知识点花点功夫肯定学的会，但是代码调试这个东西，自己不去练，永远都学不会。
2. 今天学的代码调试非常的简单，只要求同学们记住代码调试的这几个按钮的作用即可，后面还会学到很多的代码调试技巧。





## 数组

### 为什么要学习数组

> 之前学习的数据类型，只能存储一个值(比如：Number/String。我们想存储班级中所有学生的姓名，此时该如何存储？

###  数组的概念

> 所谓数组，就是将多个元素（通常是同一类型）按一定顺序排列放到一个集合中，那么这个集合我们就称之为数组。
### 数组的定义
> 数组是一个有序的列表，可以在数组中存放任意的数据，并且数组的长度可以动态的调整。

通过构造函数创建数组

```javascript
/*
arr是数组名，Array()就是构造函数，new是创建
此时没有数据，是一个空数组
*/
var arr = new Array();
/*
数字表示数组长度
如果数组没有数据，但是有长度，数组中的每个值就是undefined
*/
var 数组名 = new Array(一个数字);
//如果new Array()中有多个数字，表示数组中就有数据了，数组长度就是数据的个数。
var 数组名 = new Array(20,30,40,50);
```

通过数组字面量创建数组

```javascript
// 创建一个空数组
var arr1 = []; 
// 创建一个包含3个数值的数组，多个数组项以逗号隔开
var arr2 = [1, 3, 4]; 
// 创建一个包含2个字符串的数组
var arr3 = ['a', 'c']; 

// 可以通过数组的length属性获取数组的长度
console.log(arr3.length);
// 可以设置length属性改变数组中元素的个数
arr3.length = 0;
```

### 获取数组元素

数组的取值

```javascript
// 格式：数组名[下标]	下标又称索引
// 功能：获取数组对应下标的那个值，如果下标不存在，则返回undefined。
var arr = ['red','green', 'blue'];
arr[0];	// red
arr[2]; // blue
arr[3]; // 这个数组的最大下标为2,因此返回undefined
```

### 遍历数组

> 遍历：遍及所有，对数组的每一个元素都访问一次就叫遍历。

数组遍历的基本语法：

```javascript
for(var i = 0; i < arr.length; i++) {
	// 数组遍历的固定结构
}
```
### 数组中新增元素
数组的赋值

```javascript
// 格式：数组名[下标/索引] = 值;
// 如果下标有对应的值，会把原来的值覆盖，如果下标不存在，会给数组新增一个元素。
var arr = ["red", "green", "blue"];
// 把red替换成了yellow
arr[0] = "yellow";
// 给数组新增加了一个pink的值
arr[3] = "pink";
```
### 案例

```
求一组数中的所有数的和和平均值
求一组数中的最大值和最小值，以及所在位置
将字符串数组用|或其他符号分割
要求将数组中的0项去掉，将不为0的值存入一个新的数组，生成新的数组
    var arr=[20,0,30,0,40,50,0];
    var newArr=[];
    for (var i=0;i<arr.length;i++){
        if (arr[i]!=0){
        newArr[newArr.length]=arr[i];

        }
    }
    console.log(newArr);
    console.log(newArr.length);
    //把新数组的长度作为下标使用，数组的长度是可以改变的。
    
翻转数组
		var arr=[10,20,30,4,0];//反转：0 4 30 20 10
				//下标为0和下标为4换位置，下标1和下标3换位置，下标2不用换
				//换位置的次数是arr.length/2，互换位置的是下标为i和arr.length-1-i的两个数
        for (var i=0;i<=arr.length/2;i++){
            temp=arr[i];
            arr[i]=arr[arr.length-1-i];
            arr[arr.length-1-i]=temp;
        }
    console.log(arr);
    
提示用户输入总人数、成绩，求平均分、最高分、最低分。
 	//提示用户输入人数，prompt输入为字符串类型要转换为数字
    var total=parseInt(prompt("请输入班级总人数"));
    var perScore=[];
    //获取用户输入每个人的成绩，prompt输入为字符串类型要转换为数字
    for (var i=0;i<total;i++){
    		perScore[perScore.length]=parseInt(prompt("请输入第"+(i+1)+"个人的分数："));
    }

冒泡排序，从小到大
    var arr=[3,30,100,0,50,70,6];
            //外for循环控制比较轮数
            for (var i=0;i<arr.length-1;i++){
                //内for循环控制每轮比较次数
                for (var j=0;j<arr.length-1-i;j++){
                    //if判断大小，通过temp交换值
                    if (arr[j]>arr[j+1]){
                        var temp=arr[j];
                        arr[j]=arr[j+1];
                        arr[j+1]=temp;
                    }
                }
            }
            alert(arr);
```



## 函数
### 什么是函数

>把一段相对独立的具有特定功能的代码块封装起来，形成一个独立实体，就是函数，起个名字（函数名），在后续开发中可以反复调用
>
>函数的作用就是封装一段代码，将来可以重复使用，代码的重用

### 函数的定义

- 函数声明

```javascript
function 函数名(){
  // 函数体
}
```

- 函数表达式

```javascript
var fn = function() {
  // 函数体
}
```

- 注意：

  函数声明的时候，函数体并不会执行，只要当函数被调用的时候才会执行
  函数一般都用来干一件事情，需用使用动词+名词，表示做一件事情 `tellStory` `sayHello`等
  
  函数的命名遵循驼峰命名法
  
  函数名一旦重名，后面会把前面的函数覆盖
  
  ctrl+鼠标左键，转到函数定义(mac是command+鼠标左键)

### 函数的调用
- 调用函数的语法：

```javascript
函数名();
```

- 特点：

  函数体只有在调用的时候才会执行，调用需要()进行调用。
  可以调用多次(重复使用)

代码示例：

```javascript
// 声明函数
function sayHi() {
  console.log("吃了没？");
}
// 调用函数
sayHi();

// 求1-100之间所有数的和
function getSum() {
  var sum = 0;
  for (var  i = 0; i < 100; i++) {
    sum += i;
  }
  console.log(sum);
}
// 调用
getSum();
```
### 函数的参数

- 为什么要有参数

```javascript
function getSum() {
  var sum = 0;
  for (var i = 1; i <= 100; i++) {
    sum += i;
  }
  console.log();
}

// 虽然上面代码可以重复调用，但是只能计算1-100之间的值
// 如果想要计算n-m之间所有数的和，应该怎么办呢？
```

- 语法：

```javascript
// 函数内部是一个封闭的环境，可以通过参数的方式，把外部的值传递给函数内部
// 带参数的函数声明
// 参数不用加var
function 函数名(形参1, 形参2, 形参...){
  // 函数体
}

// 带参数的函数调用
函数名(实参1, 实参2, 实参3);
```

- 形参和实参

  > 1. 形式参数：在声明一个函数的时候，为了函数的功能更加灵活，有些值是固定不了的，对于这些固定不了的值。我们可以给函数设置参数。这个参数没有具体的值，仅仅起到一个占位置的作用，我们通常称之为形式参数，也叫形参。即，函数在定义时，小括号里的变量。
  > 2. 实际参数：如果函数在声明时，设置了形参，那么在函数调用的时候就需要传入对应的参数，我们把传入的参数叫做实际参数，也叫实参。即，函数在调用时，小括号里的变量或值

```javascript
var x = 5, y = 6;
fn(x,y); 
function fn(a, b) {
  console.log(a + b);
}
//x,y实参，有具体的值。函数执行的时候会把x,y复制一份给函数内部的a和b，函数内部的值是复制的新值，无法修改外部的x,y
```

- 实参个数可以与形参个数不一致
  - 实参个数>形参个数，按参数顺序接收，后面的实参没有参数接收，不影响结果。
  - 实参个数<形参个数，形参已声明但是没有值时undefined，值+undefeated=NaN

### 案例

- 求1-n之间所有数的和
- 求n-m之间所有数额和
- 圆的面积
- 求2个数中的最大值
- 求3个数中的最大值
- 判断一个数是否是素数

### 函数的返回值

>当函数执行完的时候，并不是所有时候都要把结果打印。我们期望函数给我一些反馈（比如计算的结果返回进行后续的运算），这个时候可以让函数返回一些东西。也就是返回值。函数通过return返回一个返回值

返回值语法：

```javascript
//声明一个带返回值的函数
function 函数名(形参1, 形参2, 形参...){
  //函数体
  return 返回值;
}

//可以通过变量来接收这个返回值
var 变量 = 函数名(实参1, 实参2, 实参3);
```

函数的调用结果就是返回值，因此我们可以直接对函数调用结果进行操作。

返回值详解：
    如果函数没有显示的使用 return语句 ，那么函数有默认的返回值：undefined
    如果函数使用 return语句，那么跟再return后面的值，就成了函数的返回值
    如果函数使用 return语句，但是return后面没有任何值，那么函数的返回值也是：undefined
    函数使用return语句后，这个函数会在执行完 return 语句之后停止并立即退出，也就是说return后面的所有其他代码都不会再执行。

    推荐的做法是要么让函数始终都返回一个值，要么永远都不要返回值。

### 案例

- 求阶乘

- 求1!+2!+3!+....+n!

- 求一组数中的最大值

- 求一组数中的最小值

- 输入年，月，日，获取这个日期是这一年的第几天

- ```javascript
  /*
  输入年，月，日，获取这个日期是这一年的第几天
   */
  function getDays(year,month,day) {
      //定义变量存储对应的天数
      var days=day;
      //如果month=1,则days就是一月的天数day,不需要再计算
      if (month==1){
         return days;
      }
      //声明一个数组存放每个月的天数---平年
      var months=[31,28,31,30,31,30,31,31,30,31,30,31];
      //如果month>=2，且是平年
      for(var i=0;i<month-1;i++){
          days=months[i]+days;
      } //end for
    	//如果month>=2,是闰年
      if (isLeapYear(year)&&month>2){
          days++;
      }
      return days;
  }//end function
  
  //判断年份是不是闰年
  function isLeapYear(year) {
      if (year%4==0&&year%100!=0||year%400==0){
          return true;
      }
      return false;
  }
  
  console.log(getDays(2000,3,1));
  ```

### arguments的使用

> JavaScript中，arguments对象是比较特别的一个对象，实际上是当前函数的一个内置属性。也就是说所有函数都内置了一个arguments对象，arguments对象中存储了传递的所有的实参。arguments是一个伪数组，因此可以进行遍历

- 案例
```javascript
求任意个数的最大值
求任意个数的和
function getSum() {
    var sum=0;
    for (var i=0;i<arguments.length;i++) {
      sum=sum+arguments[i];
    }
    return sum;
}
console.log(getSum(10,20,30,100));
console.log(getSum(10,20));
```

### 案例

```javascript
求斐波那契数列Fibonacci中的第n个数是多少？      1 1 2 3 5 8 13 21...
翻转数组，返回一个新数组
对数组排序，从小到大
输入一个年份，判断是否是闰年[闰年：能被4整数并且不能被100整数，或者能被400整数]
输入某年某月某日，判断这一天是这一年的第几天？
```

## 函数其它

### 匿名函数

> 匿名函数：没有名字的函数
>
> 命名函数：函数有函数名

匿名函数如何使用：

	将匿名函数赋值给一个变量，这样就可以通过变量进行调用

函数的两种定义方式：

第一种：函数声明

```javascript
function 函数名(){
  //函数体
}
```

第二种：函数表达式

```javascript
var 变量名=function () {
  //函数体
};//注意加分号
```

### 自调用函数

>匿名函数不能通过直接调用来执行，因此可以通过匿名函数的自调用的方式来执行
自执行函数（匿名函数自调用）的作用：防止全局变量污染。

```javascript
//调用
(匿名函数代码)();
//示例
(function () {
  alert(123);
})();
```
特点：

自调用函数是一次性的。

不会出现命名冲突问题。

### 函数是一种数据类型

```javascript
function fn() {}
console.log(typeof fn);//函数的数据类型为function
```

- 函数作为参数

因为函数也是一种类型，可以把函数作为一个函数的参数，在一个函数中调用。

如果一个函数作为参数，那么我们说这个参数（函数），叫回调函数。

只要是一个函数作为参数使用，它就是回调函数。

- 函数做为返回值

因为函数是一种类型，所以可以把函数可以作为返回值从函数内部返回，这种用法在后面很常见。

```javascript
function f1() {
    console.log("f1被调用");
    return function () {
      console.log("匿名函数被调用");
    };
}
		
    var ff=f1();//调用f1函数，执行了console.log("f1被调用"); ，返回值是 function () {console.log("匿名函数被调用");},所以ff变成一个函数
		
    console.log(ff);//打印ff函数的代码function () {console.log("匿名函数被调用");}

    console.log(ff());//调用ff函数，执行了console.log("匿名函数被调用"); , 返回值是undefined
```

### 代码规范
    1.命名规范	
    2.变量规范   
    	var name = 'zs';	
    3.注释规范
    	// 这里是注释
    4.空格规范
    5.换行规范
    	var arr = [1, 2, 3, 4];
    	if (a > b) {
          
    	}
    	for(var i = 0; i < 10; i++) {
          
    	}
    	function fn() {
          
    	}


## 作用域
作用域：变量可以起作用的范围

### 全局变量和局部变量

- 全局变量

  在任何地方都可以访问到的变量就是全局变量，对应全局作用域。

- 局部变量

  只在固定的代码片段内可访问到的变量，最常见的例如函数内部。对应局部作用域(函数作用域)

注意：

使用var声明的变量是全局变量，函数内部定义的变量是局部变量。

函数外部不能使用，除了函数内部，其他位置定义的变量都是全局变量。

局部变量退出作用域之后会释放内存空间。

全局变量关闭网页或浏览器才会释放，就会占空间，消耗内存，所以尽量少使用全局变量。

### 隐式全局变量

> 隐式全局变量：声明的变量时没有var，作用与全局的变量。
>

```javascript
function sum() {
  	var sum3=40;
    var sum1=10;
    sum2=20;
}
console.log(sum1);// sum1 is not defined
console.log(sum2+10);//sum2 is not defined
sum();//调用函数
console.log(sum2+10);//写在函数中的不带var的变量，被调用后,变成全局变量
delete sum3;
delete sum2;
console.log(typeof sum3);//number
console.log(typeof sum2);//undefined
```

注意：

使用var 定义变量不会被删除，隐式全局变量可以被删除。

### 块级作用域

任何一对花括号（｛和｝）中的语句集都属于一个块，在这之中定义的所有变量在代码块外都是不可见的，我们称之为块级作用域。
**在es5之前没有块级作用域的的概念,只有函数作用域**，现阶段可以认为JavaScript没有块级作用域

### 词法作用域
变量的作用域是在定义时决定而不是执行时决定，也就是说词法作用域取决于源码，通过静态分析就能确定，因此词法作用域也叫做静态作用域。

**在 js 中词法作用域规则:**

- 函数允许访问函数外的数据.
- 整个代码结构中只有函数可以限定作用域.
- 作用域规则首先使用提升规则分析
- 如果当前作用规则中有名字了, 就不考虑外面的名字

```javascript
var num = 123;
function foo() {
  console.log( num );
}
foo();

if ( false ) {
    var num = 123;
}
console.log( num ); // undefiend
```

### 作用域链
	只有函数可以制造作用域结构， 那么只要是代码，就至少有一个作用域, 即全局作用域。凡是代码中有函数，那么这个函数就构成另一个作用域。如果函数中还有函数，那么在这个作用域中就又可以诞生一个作用域。
	
	将这样的所有的作用域列出来，可以有一个结构: 函数内指向函数外的链式结构。就称作作用域链。
示例：

sum现在3级作用域找，如果没有，再向上级作用域找。

![](/Users/leitianxiao/Documents/GitHub/NoteBooks/100 - Work | 工作/110 - Work -Src | 源 /zuoYongYulLian.png)



## 预解析

> JavaScript代码的执行是由浏览器中的JavaScript解析器来执行的。JavaScript解析器执行JavaScript代码的时候，分为两个过程：预解析过程和代码执行过程

预解析过程：

1. 把变量的声明提升到当前作用域的最前面，只会提升声明，不会提升赋值。
2. 把函数的声明提升到当前作用域的最前面，只会提升声明，不会提升调用。
3. 先提升var，在提升function
4. 预解析会分段（多个script标签中的函数重名，预解析时不冲突）



JavaScript的执行过程

```javascript
var a = 25;
function abc (){
  alert(a);//undefined
  var a = 10;
}
abc();
// 如果变量和函数同名的话，函数优先
console.log(a);
function a() {
  console.log('aaaaa');
}
var a = 1;
console.log(a);
```



### 全局解析规则
### 函数内部解析规则
### 变量提升

- 变量提升

  定义变量的时候，变量的声明会被提升到作用域的最上面，变量的赋值不会提升。

- 函数提升

  JavaScript解析器首先会把当前作用域的函数声明提前到整个作用域的最前面

```javascript
// 1、-----------------------------------
var num = 10;
fun();
function fun() {
  console.log(num);
  var num = 20;
}
//2、-----------------------------------
var a = 18;
f1();
function f1() {
  var b = 9;
  console.log(a);
  console.log(b);
  var a = '123';
}
// 3、-----------------------------------
f1();
console.log(c);//9 隐式全局变量
console.log(b);//9 隐式全局变量
console.log(a);//报错
function f1() {
  var a = b = c = 9;
  //var a;
  //a=9; 局部变量
  //b=9; 隐式全局变量
  //c=9; 隐式全局变量
  console.log(a);//9
  console.log(b);//9
  console.log(c);//9
}
```

## 编程思想概述

面向过程：凡事都要亲力亲为，每件事的具体过程都要知道，注重过程。

面向对象：只需要根据需求找对象，所有的事情对象来做，注重结果。

面向对象特性：封装、继承、多态（抽象性）。

js不是面向对象的语言，但是可以模拟面向对象的思想。

js是一门基于对象的语言，本身系统有很多对象可以拿来用，不用创建对象，但是可以模拟面向对象。



## 对象

### 为什么要有对象

```javascript
function printPerson(name, age, sex....) {
}
// 函数的参数如果特别多的话，可以使用对象简化
function printPerson(person) {
  console.log(person.name);
  ……
}
```

### 什么是对象

```
现实生活中：万物皆对象，对象是一个具体的事物，一个具体的事物就会有行为和特征。
举例： 一部车，一个手机
车是一类事物，门口停的那辆车才是对象
	特征：红色、四个轮子
	行为：驾驶、刹车
```

### JavaScript中的对象
```
JavaScript中的对象其实就是生活中对象的一个抽象
JavaScript的对象是无序属性的集合。
	其属性可以包含基本值、对象或函数。对象就是一组没有顺序的值。我们可以把JavaScript中的对象想象成键值对，其中值可以是数据和函数。
对象的行为和特征
	特征---属性
	行为---方法
```

+ 事物的特征在对象中用属性来表示。
+ 事物的行为在对象中用方法来表示。

### 对象字面量
> 字面量：11 'abc'  true  [] {}等

```javascript
var o = {
  name: 'zs,
  age: 18,
  sex: true,
  sayHi: function () {
    console.log(this.name);
  }
};
```

思考：

```javascript
如何把学生对象、老师对象、英雄对象改写成字面量的方式
```
### 对象创建方式

- 调用系统构造函数new Object()创建对象（又叫实例化一个对象）

```javascript
//实例化对象
var obj = new Object();
/*
对象有特征和行为
特征----> 属性
行为----> 方法/函数
*/
//添加属性
obj.name="xiao";
obj.age=23;
obj.sex="female";
//添加方法
obj.sayHi=function () {
  console.log("hello world");
};
obj.play=function () {
  console.log("我喜欢玩手机");
};
//获取属性、调用方法
console.log(obj.name);
obj.sayHi();
```

- 对象字面量创建对象
```javascript
//var obj={}; 看到花括号就要想到是对象
var o = {
  //属性和方法使用键值对方式表示
  name: 'zs',
  age: 18,
  sex: true,
  sayHi: function () {
    console.log(this.name);
  }
};   
```

- 自定义构造函数创建对象

```javascript
function Person(name,age,job){
  this.name = name;
  this.age = age;
  this.job = job;
  this.sayHi = function(){
  	console.log('Hello,everyBody');
  }
  //注意这里没有return
}
//注意这里有个new
var p1 = new Person('张三', 22, 'actor');
```

- 工厂函数创建对象

```javascript
//把创建对象的过程，放在函数中，返回这个对象
function createPerson(name, age, job) {
  var person = new Object();
  person.name = name;
  person.age = age;
  person.job = job;
  person.sayHi = function(){
    console.log('Hello,everyBody');
  }
  return person;
}
//调用方法创建对象
var p1 = createPerson('张三', 22, 'actor');
var p2 = createPerson('王五', 23, 'actor');
```

- 创建对象时内存空间示意图：

![](../../110 - Work -Src | 源 /new.png)

- 如何获取变量（对象）是不是属于什么类型？

  语法：变量 instance of 类型名字; 结果是布尔类型，true/false 

- 字面量创建对象的缺陷

  一次性的对象，相当于写死了，不能传值进去。

- 点语法

  对象.名字=值；//添加属性

  对象.名字=方法; //添加方法

- js是一门动态语言，何解？

  1.代码（变量）只有执行到这个位置的时候，才知道这个变量中到底存储的是什么，如果是对象就有对象的属性和方法，如果是变量，就是变量的作用。

  2.对象没有什么，只要点了，就可以为对象添加属性或方法。

- 访问属性的另一种写法

```javascript
function Pic(picWidth,picHeight,picSize) {
    this.picWidth=picWidth;
    this.picHeight=picHeight;
    this.picSize=picSize;
    this.show=function () {
      console.log("内容");
    };
}
var obj=new Pic(100,200,300);
console.log(obj.picWidth);//100
//访问属性的另一种写法---> 对象["属性"]
//调用方法的另一种写法---> 对象["方法"]();
obj["picWidth"]=30;
console.log(obj["picWidth"]);//30
```

### 属性和方法

	如果一个变量属于一个对象所有，那么该变量就可以称之为该对象的一个属性，属性一般是名词，用来描述事物的特征
	如果一个函数属于一个对象所有，那么该函数就可以称之为该对象的一个方法，方法是动词，描述事物的行为和功能
### new关键字
> 构造函数 ，是一种特殊的函数。主要用来在创建对象时初始化对象， 即为对象成员变量赋初始值，总与new运算符一起使用在创建对象的语句中。

1. 构造函数用于创建一类对象，首字母要大写。
2. 构造函数要和new一起使用才有意义。

new在执行时会做四件事情

```
new会在内存中创建一个新的空对象
new 会让this指向这个新的对象
执行构造函数  目的：给这个新对象加属性和方法
new会返回这个新对象
```
### this详解
	JavaScript中的this指向问题，有时候会让人难以捉摸，随着学习的深入，我们可以逐渐了解
	现在我们需要掌握函数内部的this几个特点
		1. 函数在定义的时候this是不确定的，只有在调用的时候才可以确定
		2. 一般函数直接执行，内部this指向全局window
		3. 函数作为一个对象的方法，被该对象所调用，那么this指向的是该对象
		4. 构造函数中的this其实是一个隐式对象，类似一个初始化的模型，所有方法和属性都挂载到了这个隐式对象身上，后续通过new关键字来调用，从而实现实例化
## 对象的使用

### JSON数据的遍历

> JSON数据：成对出现，键值对形式
>
> JSON也是一个对象，数据都是成对的，一般JSON格式的数据无论是键还是值都要用引号引起来

```javascript
//对象的属性和方法是无序的，没有索引，不能通过for循环遍历
var json={
  "name":"乔峰",
  "age":"23",
  "sex":"男"
}
console.log(json.school);//undefinded
/*
因为js是一门动态语言，对象没有什么点就有了，但是只有声明，没有赋值，(此时对象有这个属性，但是没赋值)，所以是undefinded
*/

//key是一个变量，存的是该对象的属性名字
for (var key in json){
  console.log(key);//json对象中属性的名字
  console.log(json[key]);//json对象中属性的值
  console.log(json.key);//undefined
  //访问属性时，对象中确实有这个属性，可以用 对象.名字 或者 对象["属性名"]，如果没有这个属性，不能这么写。
  
}

```

### 遍历对象的属性

> 通过for..in语法可以遍历一个对象

```javascript
var obj = {};
for (var i = 0; i < 10; i++) {
  obj[i] = i * 2;
}
for(var key in obj) {
  console.log(key + "==" + obj[key]);
}
```
### 删除对象的属性
```javascript
function fun() { 
  this.name = 'mm';
}
var obj = new fun(); 
console.log(obj.name); // mm 
delete obj.name;
console.log(obj.name); // undefined
```

### 简单类型和复杂类型的区别
>基本类型又叫做值类型，复杂类型又叫做引用类型
>
>值类型：简单数据类型，基本数据类型，number、string、boolean在存储时，变量中存储的是值本身，因此叫做值类型。
>
>引用类型：复杂数据类型，object，在存储是，变量中存储的仅仅是地址（引用），因此叫做引用数据类型。
>
>空类型：undefined 、null

- 堆和栈

  ```
  堆栈空间分配区别：
  　　1、栈（操作系统）：由操作系统自动分配释放 ，存放函数的参数值，局部变量的值等。其操作方式类似于数据结构中的栈；
  　　2、堆（操作系统）： 存储复杂类型(对象)，一般由程序员分配释放， 若程序员不释放，由垃圾回收机制回收，分配方式倒是类似于链表。
  　　
  值类型的值在哪一块空间存储？值在栈上
  
  引用类型的值在哪一块空间存储？对象在堆上，地址在栈上
  
  值类型之间传递的是值，引用类型之间传递的是地址。 
  ```

- 注意：JavaScript中没有堆和栈的概念，此处我们用堆和栈来讲解，目的方便理解和方便以后的学习。



#### 基本类型在内存中的存储

![](../../110 - Work -Src | 源 /basics-neicun.png)

#### 复杂类型在内存中的存储

![](../../110 - Work -Src | 源 /comp-neicun.png)

#### 基本类型作为函数的参数

![](../../110 - Work -Src | 源 /basics-hanshu.png)

#### 复杂类型作为函数的参数

![](../../110 - Work -Src | 源 /comp-hanshu.png)

```javascript
// 下面代码输出的结果
function Person(name,age,salary) {
  this.name = name;
  this.age = age;
  this.salary = salary;
}
function f1(person) {
  person.name = "ls";
  person = new Person("aa",18,10);
}

var p = new Person("zs",18,1000);
console.log(p.name);
f1(p);
console.log(p.name);
```

思考：

```javascript
//1. 
var num1 = 10;
var num2 = num1;
num1 = 20;
console.log(num1);
console.log(num2);

//2. 
var num = 50;
function f1(num) {
    num = 60;
    console.log(num);
}
f1(num);
console.log(num);

//3. 
var num1 = 55;
var num2 = 66;
function f1(num, num1) {
  num = 100;
  num1 = 100;
  num2 = 100;
  console.log(num);
  console.log(num1);
  console.log(num2);
}

f1(num1, num2);
console.log(num1);
console.log(num2);
console.log(num);
```
## 内置对象

JavaScript中的对象分为3种：

- 内置对象：js自带的对象
- 浏览器对象：BOM
- 自定义对象：自定义构造函数创建的对象

怎么验证变量是不是对象？

```java
console.log(变量 instanceof Object);//返回true就是对象,返回false不是对象
var obj={};
console.log(obj instanceof Object);//true
console.log(Array instanceof Object);//true
obj就是自定义创建的对象，Array就是内置对象
```

实例对象：通过构造函数创建出来，实例化的对象。

静态对象：不需要创建，直接就是一个对象，静态方法直接通过这个对象名字调用。

实例方法通过实例对象调用，必须要通过new的方式创建的对象（实例对象）来调用的方法。

静态方法通过大写的对象调用，直接通过大写的构造函数的名字调用的方法（直接通过大写的对象名字调用的）

JavaScript 提供多个内置对象：Math/Array/Number/String/Boolean...

对象只是带有**属性**和**方法**的特殊数据类型。

学习一个内置对象的使用，只要学会其常用的成员的使用（通过查文档学习）

可以通过MDN/W3C来查询

内置对象的方法很多，我们只需要知道内置对象提供的常用方法，使用的时候查询文档。

### MDN

Mozilla 开发者网络（MDN）提供有关开放网络技术（Open Web）的信息，包括 HTML、CSS 和万维网及 HTML5 应用的 API。

- [MDN](https://developer.mozilla.org/zh-CN/)
- 通过查询MDN学习Math对象的random()方法的使用


### 如何学习一个方法？

1. 方法的功能
2. 参数的意义和**类型**
3. 返回值意义和**类型**
4. demo进行测试

### Math对象

Math对象不是构造函数，它具有数学常数和函数的属性和方法，都是以静态成员的方式提供

跟数学相关的运算来找Math中的成员（求绝对值，取整）

[Math](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math)

演示：Math.PI、Math.random()、Math.floor()/Math.ceil()、Math.round()、Math.abs()	、Math.max()

```javascript
Math.PI						// 圆周率
Math.random()				// 生成随机数
Math.floor()/Math.ceil()	 // 向下取整/向上取整
Math.round()				// 取整，四舍五入
Math.abs()					// 绝对值
Math.max()/Math.min()		 // 求最大和最小值
Math.sin()/Math.cos()		 // 正弦/余弦
Math.pow()/Math.sqrt()	 // 求指数次幂/求平方根
```

#### 案例

- 求10-20之间的随机数

```javascript
/*  随机10-20 */
function suiJi() {
  return (Math.random()*10+10);
}
console.log(suiJi());
```

- 随机生成颜色RGB

```javascript
//随机RGB颜色
function rgb() {
   var red=Math.floor((Math.random()*255));
   var green=Math.floor((Math.random()*255));
   var blue=Math.floor((Math.random()*255));
   return (red+","+green+","+blue);
 }
console.log(rgb());

//随机十六进制颜色
function yanSe() {
  var str="#";
  var arr=["0","1","2","3","4","5","6","7","8","9","A","B","C","D","E","F"];
  for (var i=0;i<6;i++) {
    str=str+arr[(parseInt(Math.random()*16))];
  }
  return str;
}
console.log(yanSe());
```

- 模拟实现max()/min()

### Date对象

创建 `Date` 实例用来处理日期和时间。Date 对象基于1970年1月1日（世界标准时间）起的毫秒数。

~~~javascript
// 获取当前时间，UTC世界时间，距1970年1月1日（世界标准时间）起的毫秒数
//创建实例对象
var now = new Date();//不传时间，就是当前服务器的时间
console.log(now.valueOf());	// 获取距1970年1月1日（世界标准时间）起的毫秒数

Date构造函数的参数//传时间就是对应的时间
1. 毫秒数 1498099000356		new Date(1498099000356)
2. 日期格式字符串  '2015-5-1'	 new Date('2015-5-1')
3. 年、月、日……				  new Date(2015, 4, 1)   // 月份从0开始
~~~

- 获取日期的毫秒形式

```javascript
var now = new Date();
// valueOf用于获取对象的原始值
console.log(date.valueOf())	

// HTML5中提供的方法，有兼容性问题
var now = Date.now();	 //毫秒数

// 不支持HTML5的浏览器，可以用下面这种方式
var now = + new Date();			// 调用 Date对象的valueOf() 
```

- 日期格式化方法

```javascript
toString()		// 转换成字符串
valueOf()		// 获取毫秒值
// 下面格式化日期的方法，在不同浏览器可能表现不一致，一般不用
toDateString()//英文的日期 --> Wed Jul 03 2019
toTimeString()//16:23:24 GMT+0800 (中国标准时间)
toLocaleDateString()//数字格式 --> 2019/7/3
toLocaleTimeString()//下午4:23:24
```

- 获取日期指定部分

```javascript
getTime()  	  // 返回毫秒数和valueOf()结果一样，valueOf()内部调用的getTime()
getMilliseconds() 
getSeconds()  // 返回0-59
getMinutes()  // 返回0-59
getHours()    // 返回0-23
getDay()      // 返回星期几 0周日   6周6
getDate()     // 返回当前月的第几天
getMonth()    // 返回月份，***从0开始***真实月份需要加1
getFullYear() //返回4位的年份  如 2016
```

#### 案例

- 写一个函数，格式化日期对象，返回yyyy-MM-dd HH:mm:ss的形式

```javascript
//需求：将时间转换为yyyy-MM-dd HH:mm:ss
function transTime(dt) {
  //如果不是时间格式
    if(!dt instanceof Date){
      	document.write(dt+" 不是时间格式,请重试");
      	return;
    }
    //提取年月日时分秒
    var year=dt.getFullYear();
    var month=dt.getMonth()+1;
    var day=dt.getDate();
    var hour=dt.getHours();
    var minute=dt.getMinutes();
    var second=dt.getSeconds();
    //三元表达式，月日时分秒为10以下时，前面加0
    month=month<10?("0"+month):month;
    day=day<10?("0"+day):day;
    hour=hour<10?("0"+hour):hour;
    minute=minute<10?("0"+minute):minute;
    second=second<10?("0"+second):second;
    //返回时间格式为yyyy-MM-dd HH:mm:ss
    return year+"-"+month+"-"+day+" "+hour+":"+minute+":"+second;
  }
    var dt=new Date();
    console.log(transTime(dt));
```

- 计算时间差，返回相差的天/时/分/秒

```javascript
function getInterval(start, end) {
  var day, hour, minute, second, interval;
  interval = end - start;
  interval /= 1000;
  day = Math.round(interval / 60 /60 / 24);
  hour = Math.round(interval / 60 /60 % 24);
  minute = Math.round(interval / 60 % 60);
  second = Math.round(interval % 60);
  return {
    day: day,
    hour: hour,
    minute: minute,
    second: second
  }
}
```

### String对象

>string(首字母小写) — 字符串类型 — 基本类型
>
>String(首字母大写) — 字符串类型 — 引用类型

- 字符串的不可变

```javascript
var str = 'abc';
str = 'hello';
// 当重新给str赋值的时候，常量'abc'不会被修改，依然在内存中
// 重新给字符串赋值，会重新在内存中开辟空间，这个特点就是字符串的不可变
// 由于字符串的不可变，在大量拼接字符串的时候会有效率问题
```

- 遍历字符串中的字符

```javascript
//字符串可以看成是字符组成的数组，但js中是没有字符概念的。
//遍历字符串中的字符
var str="abcdef";
for (var i=0;i<str.length;i++){
      console.log(str[i]);
} 
str[1]="W";//无效,字符串可以通过索引访问字符串中的某个值，但只是可以访问，不可以修改（即字符串不可变）
str="hello";//开辟了新的空间了。str有了新的地址，指向改变了。
console.log(str);//hello
```

- 创建字符串对象

```javascript
var str = new String('Hello World');
// 获取字符串中字符的个数
console.log(str.length);//String的属性 length
```

- 字符串对象的常用方法

  字符串所有的方法，都不会修改字符串本身(字符串是不可变的)，操作完成会返回一个新的字符串

```javascript
// 1 字符方法
charAt(index)    	//获取指定索引位置处字符,不填默认是0,索引越界返回空字符
charCodeAt()  	//获取指定位置处字符的ASCII码
str[0]   		//HTML5，IE8+支持 和charAt()等效
// 2 字符串操作方法
concat()   		//拼接字符串，等效于+，+更常用
slice(start index,end index)  //从start位置开始，截取到end位置，end取不到
substring() 	//从start位置开始，截取到end位置，end取不到
substr(start index,lenght)   		//从start位置开始，截取length个字符
// 3 位置方法
indexOf()   	//返回指定内容在元字符串中的位置,找不到返回-1
lastIndexOf() 	//从后往前找，只找第一个匹配的
// 4 去除空白   
trim()  		//只能去除字符串前后的空白,中间的不去掉
// 5 大小写转换方法
to(Locale)UpperCase() 	//转换大写
to(Locale)LowerCase() 	//转换小写
// 6 其它
search()
replace(原字符串，新字符串)//替换，原字符串不会改变
split("分割符(符号或字符)"，切割留下的个数)//按照指定分割符，分割，返回一个数组 
fromCharCode()
// String.fromCharCode(65, 66, 67);	 //ABC, 把ASCII码转换成字符串
```

#### 案例

- 截取字符串"我爱中华人民共和国"，中的"中华"

```javascript
var s = "我爱中华人民共和国";
s = s.substr(2,2);
console.log(s);
```

- "abcoefoxyozzopp"查找字符串中所有o出现的位置

```javascript
var str="abcoefoxyozzopp";
var index=0;
while (str.indexOf("o",index)!=-1){
  index=str.indexOf("o",index);
  console.log(index);
  index=index+1;
}
```

- 把字符串中所有的o替换成!

```javascript
var s = 'abcoefoxyozzopp';
do {
  s = s.replace('o', '');
} while (s.indexOf('o') > -1);
console.log(s);

console.log(s.replace(/o/ig, ''));
```

- 判断一个字符串中出现次数最多的字符，统计这个次数

```javascript

/*
字符串中每个字符的出现次数
 */
var str="aAabfBffCoApjskAqqwsedfCFSA";
//统计字符出现次数，不区分大小写，所以先转化为全大写或全小写
str=str.toLocaleLowerCase();//转为小写
//创建一个对象，把字母作为键，次数作为值
var obj={};
//遍历字符串中的字符
for (var i=0;i<str.length;i++){
  //把遍历的每个字符都放进key里；
  var key=str[i];
  if (obj[key]){//如果有这个key
    obj[key]++;
  }else {//如果没有这个key
    obj[key]=1;
  }
}
//遍历对象
for(key in obj){
  console.log(key+"出现了"+obj[key]+"次");
}

```

作业

```
给定一个字符串如：“abaasdffggghhjjkkgfddsssss3444343”问题如下： 
1、 字符串的长度 
2、 取出指定位置的字符，如：0,3,5,9等 
3、 查找指定字符是否在以上字符串中存在，如：i，c ，b等 
4、 替换指定的字符，如：g替换为22,ss替换为b等操作方法 
5、 截取指定开始位置到结束位置的字符串，如：取得1-5的字符串
6、 找出以上字符串中出现次数最多的字符和出现的次数 
7、 遍历字符串，并将遍历出的字符两头添加符号“@”输出至当前的文档页面。
```

### Array对象

- 创建数组对象的两种方式
  - 字面量方式
  - new Array()

```javascript
// 1. 使用构造函数创建数组对象
// 创建了一个空数组
var arr = new Array();
// 创建了一个数组，里面存放了3个字符串
var arr = new Array('zs', 'ls', 'ww');
// 创建了一个数组，里面存放了4个数字
var arr = new Array(1, 2, 3, 4);


// 2. 使用字面量创建数组对象
var arr = [1, 2, 3];

// 获取数组中元素的个数
console.log(arr.length);
```

- 检测一个对象是否是数组

  - instanceof
  - Array.isArray()     HTML5中提供的方法，有兼容性问题

  函数的参数，如果要求是一个数组的话，可以用这种方式来进行判断

- toString()/valueOf()

  - toString()		把数组转换成字符串，逗号分隔每一项
  - valueOf()         返回数组对象本身

- 数组常用方法

  演示：push()、shift()、unshift()、reverse()、sort()、splice()、indexOf()

```javascript
// 1 栈操作(先进后出)
push() //把值追加到数组最后
pop() 		//取出数组中的最后一项，修改length属性
// 2 队列操作(先进先出)
push()
shift()		//取出数组中的第一个元素，修改length属性
unshift() 	//在数组最前面插入项，返回数组的长度
// 3 排序方法
reverse()	//翻转数组
sort(); 	//即使是数组sort也是根据字符，从小到大排序
// 带参数的sort是如何实现的？
// 4 操作方法
concat()  	//把参数拼接到当前数组
slice(start index,end index) 	//从当前数组中截取一个新的数组，不影响原来的数组，参数start从0开始,end从1开始
splice()	//删除或替换当前数组的某些项目，参数start, deleteCount, options(要替换的项目)
// 5 位置方法
indexOf()、lastIndexOf()   //如果没找到返回-1
// 6 迭代方法 不会修改原数组(可选)
every()、filter()、forEach()、map()、some()
// 7 方法将数组的所有元素连接到一个字符串中。
join()//分割
```

- 清空数组

```javascript
// 方式1 推荐 
arr = [];
// 方式2 
arr.length = 0;
// 方式3
arr.splice(0, arr.length);
```

#### 案例

- 将一个字符串数组输出为|分割的形式，比如“刘备|张飞|关羽”。使用两种方式实现

```javascript
function myJoin(array, seperator) {
  seperator = seperator || ',';
  array = array || [];
  if (array.length == 0){
    return '';
  }
  var str = array[0];
  for (var i = 1; i < array.length; i++) {
    str += seperator + array[i];
  }
  return str;
}
var array = [6, 3, 5, 6, 7, 8, 0];
console.log(myJoin(array, '-'));

console.log(array.join('-'))
```

- 将一个字符串数组的元素的顺序进行反转。["a", "b", "c", "d"] -> [ "d","c","b","a"]。使用两种种方式实现。提示：第i个和第length-i-1个进行交换

```javascript
function myReverse(arr) {
  if (!arr || arr.length == 0) {
    return [];
  }
  for (var i = 0; i < arr.length / 2; i++) {
    var tmp = arr[i];
    arr[i] = arr[this.length - i - 1];
    arr[arr.length - i - 1] = tmp;
  }
  return arr;
}

var array = ['a', 'b', 'c'];
console.log(myReverse(array));

console.log(array.reverse());
```

- 工资的数组[1500, 1200, 2000, 2100, 1800],把工资超过2000的删除

```javascript
// 方式1
var array =  [1500,1200,2000,2100,1800];
var tmpArray = [];
for (var i = 0; i < array.length; i++) {
  if(array[i] < 2000) {
    tmpArray.push(array[i]);
  }
}
console.log(tmpArray);
// 方式2
var array =  [1500, 1200, 2000, 2100, 1800];
array = array.filter(function (item, index) {
  if (item < 2000) {
    return true;
  }
  return false;
});
console.log(array);
```

- ["c", "a", "z", "a", "x", "a"]找到数组中每一个a出现的位置

```javascript
var array =  ['c', 'a', 'z', 'a', 'x', 'a'];
do {
  var index = array.indexOf('a',index + 1);
  if (index != -1){
    console.log(index);
  }
} while (index > 0);
```

- 编写一个方法去掉一个数组的重复元素

```javascript
var array =  ['c', 'a', 'z', 'a', 'x', 'a'];
function clear() {
  var o = {};
  for (var i = 0; i < array.length; i++) {
    var item = array[i];
    if (o[item]) {
      o[item]++;
    }else{
      o[item] = 1;
    }
  }
  var tmpArray = [];
  for(var key in o) {
    if (o[key] == 1) {
      tmpArray.push(key);
    }else{
      if(tmpArray.indexOf(key) == -1){
        tmpArray.push(key);
      }
    }
  }
  returm tmpArray;
}

console.log(clear(array));
```



### 基本包装类型

普通变量不能直接调用属性和方法。对象可以直接调用属性和方法。

基本包装类型：本身是基本类型，在执行代码的过程，如果这种类型的变量调用了属性或者方法，那么这种类型就不再是基本类型，而是基本包装类型。这个变量也不再是普通的变量，而是基本包装类型对象。

为了方便操作基本数据类型，JavaScript还提供了三个特殊的引用类型：String/Number/Boolean

```javascript
// 下面代码的问题？
// s1是基本类型，基本类型是没有方法的
var s1 = 'zhangsan';
var s2 = s1.substring(5);

// 当调用s1.substring(5)的时候，先把s1包装成String类型的临时对象，再调用substring方法，最后销毁临时对象, 相当于：
var s1 = new String('zhangsan');
var s2 = s1.substring(5);
s1 = null;
```

```javascript
// 创建基本包装类型的对象
var num = 18;  				//数值，基本类型
var num = Number('18'); 	//类型转换，不是new
var num = new Number(18); 	//基本包装类型，对象
// Number和Boolean基本包装类型基本不用，使用的话可能会引起歧义。例如：
var b1 = new Boolean(false);
var b2 = b1 && true;		// 结果是什么，
//如果 对象&&true 结果是true ；如果是 true&&对象 结果是对象
```
