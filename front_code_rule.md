# 前端编码规范
## 可读性
1．	所有文档请统一采用UTF-8编码。
2．	缩进。一个Tab或四个空格。
3．	目录结构。可以自行新增文件，但请遵守已有的目录结构。
4．	代码提交。
•	提交代码前，请更新本地代码。进行简单测试，确保运行无误后，方可提交。
•	提交代码时，请填写备注，并勾选掉没用的文件。
•	精简提交次数。提交的代码应该保证逻辑上的完整、独立。确保每次提交都有价值。
5．	命名：
•	无论CSS、JS，请用采用小驼峰命名法。HTML标签、属性名请全部小写。
•	命名应简约而不失语义，建议适当的缩写。第一节反映出元素种类或所属模块，如button的样式请用btn开头、string的声明请用str开头。请参照“统一语义理解和简写”小节。
•	类名、枚举名、全局变量名首字母大写。
•	静态变量名所有字母大写。
•	JQuery对象，请用”$”开头，如:
```
var $div = $(“divName”);。
```
6．	必要、精简的注释。良好的注释可以帮助自己和他人，请尽量清晰地描述。注释中偶尔的幽默，可以让大家更愉快的编码。临时性代码请注释//TODO。
7．	换行。
•	只有一行内容，请不要换行。如:
```
.btnXXX { margin: 0; }，if(true) return;。
```
•	每对大括号，后一个换行，前一个不换行。
8．	引号。HTML标签内请用双引号，JS、CSS中优先使用单引号。
9．	属性顺序。HTML 属性应当按照class, id, style,其他的顺序依次排列。
10．	引入图片，应优先用css属性，尽量避免使用<img>标签。
11．	适当的空格。
•	“=”、”==”、”&&”、”||”、”>”、”<”前后需要跟空格
•	数组成员间的”,”和各个参数间的”,”（包括形参和实参）后面需要跟空格。

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


# 统一语义理解和简写
布局（.g-）
语义	命名	简写
文档	doc	doc
头部	head	hd
主体	body	bd
尾部	foot	ft
主栏	main	mn
主栏子容器	mainc	mnc
侧栏	side	sd
侧栏子容器	sidec	sdc
盒容器	wrap/box	wrap/box
模块（.m-）、元件（.u-）
语义	命名	简写
导航	nav	nav
子导航	subnav	snav
面包屑	crumb	crm
菜单	menu	menu
选项卡	tab	tab
标题区	head/title	hd/tt
内容区	body/content	bd/ct
列表	list	lst
表格	table	tb
表单	form	fm
热点	hot	hot
排行	top	top
登录	login	log
标志	logo	logo
广告	advertise	ad
搜索	search	sch
幻灯	slide	sld
提示	tips	tips
帮助	help	help
新闻	news	news
下载	download	dld
注册	regist	reg
投票	vote	vote
版权	copyright	cprt
结果	result	rst
标题	title	tt
按钮	button	btn
输入	input	ipt
皮肤（.s-）
语义	命名	简写
字体颜色	fontcolor	fc
背景	background	bg
背景颜色	backgroundcolor	bgc
背景图片	backgroundimage	bgi
背景定位	backgroundposition	bgp
边框颜色	bordercolor	bdc
状态（.z-）
语义	命名	简写
选中	selected	sel
当前	current	crt
显示	show	show
隐藏	hide	hide
打开	open	open
关闭	close	close
出错	error	err
不可用	disabled	dis

