一、基础选择器

1.	*	 --通用元素选择器，匹配任何元素
2.	E	 --标签选择器，匹配所有使用E标签的元素
3.	.info	 --class选择器，匹配所有class属性中包含info的元素
4.	#footer	 --id选择器，匹配所有id属性等于footer的元素

实例：
* { margin:0; padding:0; }
p { font-size:2em; }
.box { background:#eee; }
#title { color:red; }

二、结构选择器

5. E F --后代（包含）选择器，匹配所有属于E元素后代的F元素，E和F之间用空格分隔
6. E>F --子代选择器，匹配所有E元素的子元素F
7. E~F --全部兄弟选择器，匹配任何在E元素<b>之后</b>的同级F元素
8. 
