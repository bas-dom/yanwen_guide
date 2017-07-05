## 更好的编码
1．	面向对象思想编程。
2．	请实现响应式页面，优先保证1366px、1920px宽度下显示。
3．	CSS书写位置。CSS请放到对应HTML文件的开头，公共样式请放到Content目录下。
4．	共用方法请放到common.js中。对common.js的修改，请务必通知到全组成员。
5．	请使用绝对路径。如“/static/scripts/lib/Chart.min.js”。
6．	适量的ID。仅在必要时为HTML标签添加ID属性，如动态数据容器等。
7．	优先采用div布局。布局时，能不使用“position: absolute”，则不使用。
8．	所有的HTML标签应该正确闭合。无论是否为自闭和标签，请确保每个标签都有对应的”/”。 
9．	私有在前，标准在后。先写带有浏览器私有标志的，后写W3C标准的。
```
.m-box {
-webkit-box-shadow:0 0 0 #000;
-moz-box-shadow:0 0 0 #000;
box-shadow:0 0 0 #000;
}
```
10．	减少标签的数量。编写 HTML 代码时，尽量避免多余的父元素，保持简洁。
11．	预防元素显示失败、显示不明确。如为<img>添加alt属性，为canvas添加加载失败提示，适当的添加title属性等。
12．	优先使用CSS。如果CSS可以做到，就不要使用JS，减轻JS开发量：
•	用CSS控制交互或视觉的变化，JS只需要更改className。
•	利用CSS一次性更改多个节点样式，避免多次渲染，提高渲染效率。
•	简单动画实现请用CSS。
13．	总是使用var。变量如果声明时没有加var会使该变量成为全局变量。避免污染全局命名空间。
14．	缓存jQuery查询。
// bad
```
function setSidebar() {
  $('.sidebar').hide();
  // ...stuff...
  $('.sidebar').css({
    'background-color': 'pink'
  });
}
```
// good
```
function setSidebar() {
  var $sidebar = $('.sidebar');
  $sidebar.hide();
  // ...stuff...
  $sidebar.css({
    'background-color': 'pink'
  });
}
```
 
# 其他参考引用
可参照学习，如有冲突部分，请以本文档为最终基准:
	JavaScript规范 https://github.com/adamlu/javascript-style-guide
	编写更好的jQuery代码 http://www.cnblogs.com/allenxing/p/3672105.html
	编码规范,编写灵活、稳定、高质量的 HTML 和 CSS 代码的规范
http://codeguide.bootcss.com/
	NEC http://nec.netease.com/
	javascript编程规范-基本格式 http://www.tw93.com/?p=1
	javascript编程规范-命名规范 
http://www.html-js.com/article/The-little-front-end-tw93-JavaScript-programming-specification--naming-conventions


