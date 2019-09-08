### doctype的作用

DOCTYPE是html5标准网页声明，且必须声明在HTML文档的第一行。来告知浏览器的解析器用什么解析这个文档，不同的渲染的模式应该会影响到浏览器对于css代码甚至JavaScript脚本的解析。

#### 文档解析类型有：

*  BackCompat:怪异模式，浏览器使用自己的怪异模式解析渲染页面。（如果没有声明Doctype,默认是这个模式）
*  Css1Compat:标准模式，浏览器使用w3c的标准解析渲染页面。
* IE8:近乎标准的模式 （基本淘汰）


#### 三种模式的区别

* 标准模式(standars mode):页面按照HTLML和CSS的定义渲染
* 怪异模式(quirks mode):会模拟更旧的浏览器的行为
* 近乎标准(almost standars):实施一种表单元格尺寸的怪异行为


### HTML、XHTML、XML区别

* HTML(超文本标记语言):在html4.0之前html现有实现再有标准，导致html非常混乱和松散
* XML(可扩展标记语言):主要用于存储数据和结构，可以扩展，主要是轻量高效
* XHTML(可扩展超文本标记语言):基于上述两者而来，w3c为了解决html混乱问题而生，并诞生了html5，开头加入了<!Doctype html> ,如果不加就是兼容混乱的html。


### data-属性 

html的数据属性，用于将数据存储在标准的html元素中作为额外的信息，我们可以通过js访问并操作，以此达到操作数据的目的。

```
<div
  id="user"
  data-index-number="12314"
  data-parent="cars"
  data-uid="12345">
...
</div>

```
上述例子

```
var  user=document.getElementById('user');
var uid = user.getAttribute('data-uid') ; // uid = '12345'
user.setAttribute('data-index-number','158933');

```

### 前端存储数据

cookies、 localStorage 、sessionStorage、Web SQL、IndexedDB


* cookies： 在HTML5标准前本地储存的主要方式，优点是兼容性好，请求头自带cookie方便，缺点是大小只有4k，自动请求头加入cookie浪费流量，每个domain限制20个cookie，使用起来麻烦需要自行封装

* localStorage：HTML5加入的以键值对(Key-Value)为标准的方式，优点是操作方便，永久性储存（除非手动删除），大小为5M，兼容IE8+

* sessionStorage：与localStorage基本类似，区别是sessionStorage当页面关闭后会被清理，而且与cookie、localStorage不同，他不能在所有同源窗口中共享，是会话级别的储存方式

* Web SQL：2010年被W3C废弃的本地数据库数据存储方案，但是主流浏览器（火狐除外）都已经有了相关的实现，web sql类似于SQLite，是真正意义上的关系型数据库，用sql进行操作，当我们用JavaScript时要进行转换，较为繁琐。

* IndexedDB： 是被正式纳入HTML5标准的数据库储存方案，它是NoSQL数据库，用键值对进行储存，可以进行快速读取操作，非常适合web场景，同时用JavaScript进行操作会非常方便。