## JavaScript的学习
（前面和c、python大同小异）

---
----

## 对象、属性、方法
-----

|对象|属性|方法|
|---|---|---|
|car|car.color|car.start()|
|<font color='red'>**attention**</font>：不要把字符串、数值、布尔值声明为对象|所有car都拥有相同的属性，属性值因车而异|所有car都拥有相同的方法，但方法执行时间因车而异（方法是作为属性储存的函数）|

### 访问对象属性、方法

属性：
两种方式：
- objectName.propertyName
- objectName["propertyName"]

方法：
一种方式：
- objectName.methodName()
（如果不使用**（）*访问方法，则将返回函数定义）

---
---

## 事件

### HTML事件
for example：
- HTML网页完成加载
- HTML按钮被点击
  
>HTML事件是发生在HTML元素上的事情；当HTML页面使用JavaScript时，JavaScript能够应对这些事件，即通过JavaScript代码，HTML允许向HTML元素添加事件处理程序。


- 事件处理程序可用于处理、验证用户输入、用户动作和浏览器动作：

  - 每当页面加载时应该做的事情
  - 当页面被关闭时应该做的事情
  - 当用户点击按钮时应该被执行的动作
  - 当用户输入数据时应该被验证的内容
  - 等等


- 让 JavaScript 处理事件的不同**方法**有很多：

  - HTML 事件属性可执行JavaScript 代码
  - HTML 事件属性能够调用 JavaScript 函数
  - 您能够向 HTML 元素分配自己的事件处理函数
  - 您能够阻止事件被发送或被处理
  - 等等


----
----

## 字符串

### 字符串方法
（用于处理字符串）


### 转义字符
无人在意的角落里：

|`\'`|`\"`|`\\`|
|---|---|---|
|'|"|`\`|

