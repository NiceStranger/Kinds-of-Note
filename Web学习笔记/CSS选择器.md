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
19. a:link --用来定义未被点击的链接样式</br>
20. a:visited --用来定义已被点击的链接样式</br>
21. a:active --用来定义鼠标已经在其上按下，但还没有释放的超链接样式</br>
22. a:hover --用来定义鼠标悬停其上时的样式</br>
23. input:focus --用于选择获得焦点的表单元素</br>
</br>
 实例：</br>
 input[type=text]:focus { color:#000; background:#ffe; }</br>

 <h4>4.2 结构伪类选择器</h4>
 24. E:first-child --匹配父元素的第一个子元素E</br>
 25. E:last-child --匹配父元素的最后一个子元素E</br>
 26. E:nth-child(n) --匹配其父元素的第n个子元素，第一个编号为1</br>
 27. E:nth-last-child(n)	--匹配其父元素的倒数第n个子元素，第一个编号为1</br>
 28. E:nth-of-type(n)	--与:nth-child()作用类似，但是仅匹配使用同种标签的元素</br>
 29. E:nth-last-of-type(n)	--与:nth-last-child() 作用类似，但是仅匹配使用同种标签的元素</br>
 30. E:first-of-type	--匹配父元素下使用同种标签的第一个子元素，等同于E:nth-of-type(1)</br>
 31. E:last-of-type	--匹配父元素下使用同种标签的最后一个子元素，等同于E:nth-last-of-type(1)</br>
 32. E:only-child	--匹配父元素下仅有的一个子元素，等同于E:first-child E:last-child或 E:nth-child(1) E:nth-last-child(1)</br>
 33. E:only-of-type	--匹配父元素下使用同种标签的唯一一个子元素，等同于E:first-of-type E:last-of-type或 E:nth-of-type(1) E:nth-last-of-type(1)</br>
 34. E:root	--匹配文档的根元素，对于HTML文档，就是HTML元素</br>
 35. E:empty	--匹配一个不包含任何子元素的元素，注意，文本节点也被看作子元素</br>
 36. E:not(s)	--匹配不符合当前选择器的任何元素</br>
<b>注意：结构伪类选择器中，子元素的序号是从1开始的，所以，当参数n的计算结果为0 时，将不选择任何元素</b>

<h4>4.3 其他伪类选择器</h4>
37. E:target	--目标伪类选择器，匹配被相关URL指向的E元素</br>
38. E:lang(language) --语言伪类选择器，匹配指定语言的元素</br>
39. 
