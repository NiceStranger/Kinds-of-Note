<h3>一、基础选择器</h3>

1.	&#42;	 --通用元素选择器，匹配任何元素
2.	E	 --标签选择器，匹配所有使用E标签的元素
3.	.info	 --class选择器，匹配所有class属性中<b>包含</b>info的元素
4.	#footer	 --id选择器，匹配所有id属性<b>等于</b>footer的元素

实例：</br>
&#42; { margin:0; padding:0; }</br>
p { font-size:2em; }</br>
.box { background:#eee; }</br>
#title { color:red; }

<h3>二、结构选择器</h3>

5. E F --后代（包含）选择器，匹配所有属于E元素后代的F元素，E和F之间用空格分隔
6. E>F --子代选择器，匹配所有E元素的子元素F
7. E~F --同级元素通用选择器，匹配任何在E元素<b>之后</b>的同级F元素
8. E+F --毗邻元素选择器，匹配所有<B>紧随E元素之后的同级元素F</B>
9. E,F --并集（群组）选择器，同时匹配所有E元素或F元素，E和F之间用逗号分隔
10. EF --交集选择器，同时匹配E元素和F元素，E和F之间用 . 分隔

实例：</br>
div p { color:#f00; }</br>
div > strong { color:#f00; }</br>
p ~ ul { background:#ff0; }</br>
p + h2 { color:red; }</br>
p , h2 { color:#fff; }</br>
p.h2 { font-weight:bold; }

<h3>三、属性选择器</h3>

11. E[att] --属性的或运算，匹配所有具有att属性的E元素，不考虑它的值
12. E[att1][att2] --属性的与运算，匹配所有具有att1和att2属性的E元素
13. E[att="val"] --匹配所有att属性等于"val"的E元素
14. E[att~="val"] --匹配所有att属性具有多个空格分隔的值、其中一个值等于"val"的E元素
15. E[att|="val"]	--匹配所有att属性具有多个连字号 - （hyphen-separated）分隔的值、其中一个值以"val"开头的E元素，主要用于lang属性，比如"en"、"en-us"、"en-gb"等等
16. E[att^="val"]	--属性att的值以"val"开头的元素
17. E[att$="val"]	--属性att的值以"val"结尾的元素
18. E[att*="val"]	--属性att的值包含"val"字符串的元素

实例：</br>
p[title] { color:#f00; }</br>
h2[name][class] { font-weight:700; }</br>
div[class="error"] { color:#f00; }</br>
h2[class~="title"] { color:red; }</br>
p[lang|="en"] { color:#f00; }</br>
div[class^="tle"] { background:#ff0; }</br>
h2[class$="tle"] { color:red; }</br>
h2[class*="title"] { color:red; }

<h3>四、伪类选择器</h3>

<h4>4.1 动态伪类选择器</h4>
 19. a:link --用来定义未被点击的链接样式
 20. a:visited --用来定义已被点击的链接样式
 21. a:active --用来定义鼠标已经在其上按下，但还没有释放的E元素样式
 22. a:hover --用来定义鼠标悬停其上时的样式
 23. input:focus --用于选择获得焦点的表单元素

 实例：</br>
 
