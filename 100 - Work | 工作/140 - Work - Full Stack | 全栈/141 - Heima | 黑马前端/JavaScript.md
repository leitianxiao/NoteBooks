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

![](/Users/leitianxiao/Documents/GitHub/NoteBooks/100 - Work | 工作/110 - Work -Src | 源 /compute.png)

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

```
//这是单行注释
```

### 多行注释

一般是用在函数或者一段代码上面

```
/*
这是多行注释
*/
```

