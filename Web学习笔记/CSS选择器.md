一、基础选择器

1.	&#42;	 --通用元素选择器，匹配任何元素
2.	E	 --标签选择器，匹配所有使用E标签的元素
3.	.info	 --class选择器，匹配所有class属性中<b>包含</b>info的元素
4.	#footer	 --id选择器，匹配所有id属性<b>等于</b>footer的元素

实例：</br>
&#42; { margin:0; padding:0; }</br>
p { font-size:2em; }</br>
.box { background:#eee; }</br>
#title { color:red; }

二、结构选择器

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
