# HTML_Study  
  
  
### 作者：冰红茶  
### 参考书籍：《HTML5权威指南》
------  

  HTML，Hypertext Makeup Language超文本标记语言。其实当初在学javascript权威指南第二部分的时候，就觉得应该补一下html和css权威指南方面的知识，才能更好地进行第二部分的学习^_ ^
  
## 目录

## [一、初探HTML](#1)
### [1.1 元素](#1.1)
### [1.2 创建HTML文档](#1.2) 
### [1.3 HTML5元素背景知识](#1.3)
## [二、构建HTML元素](#2)
### [2.1 文档结构元素](#2.1)
### [2.2 文本元素](#2.2) 
### [2.3 组织内容元素](#2.3)
------  

    
<h2 id='1'> 一、初探HTML </h2>
<h3 id='1.1'> 1.1元素</h3>  

#### 1) 元素格式  
>> 其实HTML其实HTML的职责应该被限定于说明文档内容的结构和含义，而并非内容呈现的形式，内容呈现形式的责任应该由CSS承担。  
>>>>>> ![图1-1 元素格式](https://github.com/hblvsjtu/HTML_Study/blob/5f7ba08d23b8f4de45599032c5b7445e4de8da87/picture/%E5%9B%BE1-1%20%E5%85%83%E7%B4%A0%E6%A0%BC%E5%BC%8F.png?raw=true)   

#### 2)	空元素
>> 空元素的表示内容为空的标签，如`<code></code>`；  
>> 或者你可以使用自闭合的标签，如`<code/>`,直接在第一个标签的最后加上“/”；  

#### 3)	虚元素
>> 本身规定就不允许带有内容的元素，如`<hr>`,是一种段落组织元素，一条长横线，不过更倾向于类似空元素的写法，在末尾加上一个“/”，形如`<hr/>`  

			I like apples; <hr/> I like pears;
			
#### 4) 元素属性
- 属性只能用于开始标签或者单个标签；
- 属性又分为全局属性和局部属性；
>>>>>> ![图1-2 元素属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/%E5%9B%BE1-2%20%E5%85%83%E7%B4%A0%E5%B1%9E%E6%80%A7.png?raw=true) 
- 布尔属性
>> 其属性值为空字符串==属性名字符串；或者直接赋予“true”或者“false”；
- 自定义属性
>> 用户自己定义的，以`data-`打头的,添加这样的前缀是为了避免与未来版本可能增加的属性名称冲突；可以跟CSS和JS结合起来；

#### 5) 元素的分类
- 父元素
- 子元素 关系最近的后代元素
- 后代元素
- 兄弟元素

#### 6) 元素的类型
- 元数据类型 构建html文档的基本结构，以及就如何处理文档向浏览器提供信息和指示；
- 流元素 流元素是短语元素的超集 ？不明所以
- 短语元素 ？不明所以
- 其他元素，如`<li>` ？不明所以

<h3 id='1.2'>1.2 创建HTML文档</h3>  

#### 1) 用户代理user agent
>> 用于处理HTML文档的软件有一个共同的软件——用户代理user agent，浏览器是最流行的用户代理，但不是唯一的一种；

#### 2) 外层结构
>> 外层结构由两个元素决定: DOCTYPE和html;  

			<!DOCTYPE HTML>
				<html>
					<!-- type your text -->
				</html>

#### 3) 元数据
>> 放在`<head>内容</head>`中间的内容；

#### 4) HTML实体
>> 特殊字符的编码，避免该特殊字符被当作HTML元素处理，而当作普通显示字符处理；
>>>>>> ![图1-3 常用HTML实体](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/%E5%9B%BE1-2%20%E5%85%83%E7%B4%A0%E5%B1%9E%E6%80%A7.png?raw=true) 

#### 5) 全局属性
- accesskey 快捷键 在Windows系统上是“Alt” + accesskey的值；
- class 给元素归类用的；
- contenteditable 赋予用户可修改的文字的权限，它的值是一个布尔值，“true”或者“false”；
- contextmenu 用来为元素设置快捷菜单，即右键会弹出菜单，然而，暂时还没有支持该特性的浏览器；
- dir 文字向左靠边还是向右靠边，“ltr” | “rtl”；
- draggable 表示元素是否可被拖放；
- dropzone 与draggable搭配使用；
- hidden 是否隐藏该元素，可以直接使用，后面不加值，或者说他本身就是键值同体；
- id 元素的唯一标识符，在CSS中是用“#”+id作为分类器。还可以利用id值导肮到文档中的特定位置，如URL=文档名+“#”+id，“#”+id称为URL的片段标识符；
- lang 语言选项，“en”“fr”“es”;
- spellcheck 拼写检查，只有在哪些用户可编辑的元素上才有意义，如：`<textarea>`它的值是一个布尔值，“true”或者“false”。不过有一个问题是，该属性会忽略之前的lang属性，原因是spellcheck属性基于用户操作系统或浏览器的语言设置;
- style 直接定义CSS样式用的；
- tabindex 键盘焦点的切换，一般用“tab”键，键值为1的会被首先选中，-1的不会被选中；
- title 提供元素的额外信息，一般是一些提示，即你用光标移过去之后会出现提示；  

<h3 id='1.3'> 1.3 HTML5元素背景知识 </h3> 

#### 1) 语义与呈现分离  
#### 2) 元素选用原则  
>> 这里说的很含糊，其实并没有什么具体的可操作选用原则；  
------  

<h2 id='2'> 二、构建HTML文档 </h2>  
<h3 id='2.1'> 2.1 文档元素</h3>   

>>>>>> ![图2-1 文档和元数据元素](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.1%20%E6%9E%84%E7%AD%91%E5%9F%BA%E6%9C%AC%E7%9A%84%E6%96%87%E6%A1%A3%E7%BB%93%E6%9E%84.png?raw=true)  

>>>>>> 元素|元素类型|内容|元素结束方式|是否HTML5新增
>>>>>> -|-|-|-|-
>>>>>> a|短语/流|短语内容/流内容|开始标签和结束标签|否
>>>>>> b|短语|短语内容|开始标签和结束标签|否
>>>>>> em|短语|短语内容|开始标签和结束标签|否
>>>>>> i|短语|短语内容|开始标签和结束标签|否
>>>>>> s|短语|短语内容|开始标签和结束标签|否
>>>>>> strong|短语|短语内容|开始标签和结束标签|否
>>>>>> small|短语|短语内容|开始标签和结束标签|否
>>>>>> sup|短语|短语内容|开始标签和结束标签|否
>>>>>> sub|短语|短语内容|开始标签和结束标签|否
>>>>>> br|短语|无|虚元素|否
>>>>>> wbr|短语|无|虚元素|是
>>>>>> code|短语|短语内容|开始标签和结束标签|否
>>>>>> var|短语|短语内容|开始标签和结束标签|否
>>>>>> samp|短语|短语内容|开始标签和结束标签|否
>>>>>> kbd|短语|短语内容|开始标签和结束标签|否
>>>>>> abbr|短语|短语内容|开始标签和结束标签|否
>>>>>> dfn|短语|短语内容|开始标签和结束标签|否
>>>>>> q|短语|短语内容|开始标签和结束标签|否
>>>>>> ruby|短语|短语内容/rt/rp|开始标签和结束标签|是
>>>>>> bdo|短语|短语内容|开始标签和结束标签|否
>>>>>> bdi|短语|短语内容|开始标签和结束标签|是
>>>>>> span|短语|短语内容|开始标签和结束标签|否
>>>>>> mark|短语|短语内容|开始标签和结束标签|是
>>>>>> ins|短语/流|短语内容/流内容|开始标签和结束标签|否
>>>>>> del|短语/流|短语内容/流内容|开始标签和结束标签|否
>>>>>> time|短语|短语内容|开始标签和结束标签|是

#### 1) DOCTYPE元素  
>> 他告诉浏览器两件事：它处理的是HTML文档；用来标记文档内容HTML所属的版本；  
#### 2) html元素 开始标签和结束标签    
>> 有一个更加恰当的名字*根元素*；  
#### 3) head元素 开始标签和结束标签    
>> 包含着文档的元数据和文档信息，元数据向浏览器提供有关文档内容和标记的信息，还包括CSS和JS的文档的引用；
- title 标签页名字
- base 虚元素的形式，有两个属性
> - href 基准地址，如  	
> - target 告诉浏览器如何打开URL
- meta 虚元素的形式  
> - name 使用“name”和“content”作为键值对；  
> - content；  
> - charset 声明字符编码
> - http-equiv 模拟HTTP标头字段，字段值由content表示  

>>>>>> ![2.2 meta元素http-equiv属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.2%20meta%E5%85%83%E7%B4%A0http-equiv%E5%B1%9E%E6%80%A7.png?raw=true)  

- style 开始标签和结束标签  
> - text 定义CSS样式
> - scoped html5新增的，可以设置属性scoped已规定作用域，如果不设置的话就作用于整个文档
> - media 规定设备值,可以  采用“AND”“NOT”和表示“OR”的逗号表示  
>>>>>> ![2.3 style元素media属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.3%20style%E5%85%83%E7%B4%A0media%E5%B1%9E%E6%80%A7.png?raw=true)  

>>>>>> ![2.4 style元素media属性规定的设备值](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.4%20style%E5%85%83%E7%B4%A0media%E5%B1%9E%E6%80%A7%E8%A7%84%E5%AE%9A%E7%9A%84%E8%AE%BE%E5%A4%87%E5%80%BC.png?raw=true)  

- link 开始标签和结束标签   
> - 虚元素的形式，指定外部资源，在HTML5中新增“size”的属性，去掉“charset”“rev”“target”的属性；
> - rel的值除了我们常见的“stylesheet”载入CSS文档，还有“icon”，表示为网站载入图标,还有预获取功能“prefetch”； 
> - type的值可以是“text/css”，还可以是“image/x-icon”
> - 预获取功能“prefetch”,在用户点击某链接进入某个页面的前就已经进行预先加载。  
>>>>>> ![2.5 link元素属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.5%20link%E5%85%83%E7%B4%A0%E5%B1%9E%E6%80%A7.png?raw=true)  

		<!DOCTYPE html>
		<html>
			<head>
				<title>欢迎页面</title>
				<base href="http://"/>
				<meta name="author" content="LvHongbin"/>
				<meta name="description" content="A simple example"/>
				<meta charset="utf-8"/>
				<meta http-equiv="refresh" content="5"/>
				<style type="text/css" scoped="">>
					a{
						background-color: grey;
						color: white;
						padding: 0.5em;
					}
				</style>
			</head>
			<body>
				<a href="www.baidu.com">登陆页面</a> 
			</body>
		</html>  

- script  开始标签和结束标签，用于定义脚本并控制其执行方式，具有的属性包括；
> - type 不使用该属性的时候，默认是js类型
> - src 载入外部文件，设置了该属性的script元素只能是空白元素，不能既有src属性，又有内嵌内容。*另外，如果是引用外部的文件，则必须使用结束标签，不能采用自闭合标签，否则浏览器会忽略该外部文件的加载*；
> - defer 一般来讲，浏览器是按顺序解析html文本和JS文档，但是有时候需要将JS文档放在最后执行，此时除了将该JS脚本放在html文档的末尾之外，还有一种方法，就是使用defer，该属性没有值，直接放进去就可以了。需要注意的是，该属性只能用于外部JS文档的引用，如果使用内嵌式的JS脚本则不起作用；
> - async 异步执行脚本，该属性没有值，直接放进去就可以了
> - charset 
- noscript 
>> 假如用户的浏览器不支持JS或者用户选择禁用JS的功能是，使用noscript给用户显示一些简短信息；  

<h3 id='2.2'> 2.2 文本元素</h3>  

>> >> 一个主要特点是元素内容是短语元素，组织形式是行内；
>>>>>> ![2.6 文本元素1](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.6%20%E6%96%87%E6%9C%AC%E5%85%83%E7%B4%A01.png?raw=true)  
>>>>>> ![2.6 文本元素2](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.6%20%E6%96%87%E6%9C%AC%E5%85%83%E7%B4%A02.png?raw=true)  
#### 1) 超链接a 开始标签和结束标签    
>> href 指向外部的超链接；  
>> href 指向内部的超链接，herf="# + id名称"，如果找不到这样的id，那么浏览器会尝试寻找name值等于该id值的元素；  
>> target 设定浏览环境，其实就是决定新窗口在哪里打开的问题  
>>>>>> ![2.7 a元素的target属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.7%20a%E5%85%83%E7%B4%A0%E7%9A%84target%E5%B1%9E%E6%80%A7.png?raw=true)  

#### 2) 用于设置文字格式的元素
> - b元素 开始标签和结束标签，用于内容加粗；    
> - em元素 开始标签和结束标签，用于内容强调，感觉就是做一个斜体；    
> - i元素 开始标签和结束标签，用于外文词语或者科技术语；  
> - s元素 开始标签和结束标签，用于不正确或者纠正，其实就是加一个删除线；  
> - strong元素 开始标签和结束标签，用于一段重要的文字，其实就是把字体放大一号；  
> - u元素 开始标签和结束标签，用于加下划线；  
> - small元素 开始标签和结束标签，用于小一号字；  
> - sup元素和sub 开始标签和结束标签，用于上标和下标；
#### 3) 换行
> - br元素 虚元素，用于强制换行；  
> - wbr元素 虚元素，当一行装不下那么多的文字的时候自动换行；  
#### 4) 输入和输出
>> 包括code,car,samp,kbd，不过基本上用不到；  
#### 5) 标题引用，引文，定义和缩写
>> 基本上用不到； 
#### 6) 使用语言元素
> - ruby,rt和rp，HTML5新增的，开始标签和结束标签，这个还有些用，主要用来注音的，即在文字的上方加拼音；
> - bdo 开始标签和结束标签，文字阅读的方向，跟dir属性一起使用；  
> - bdi HTML5新增的，开始标签和结束标签，保证文字方向
#### 7) 其他文本元素
> - span元素 开始标签和结束标签，内容是短语元素，本身并没有什么特别的含义，它可以把一些全局属性用到一段内容上；
> - mark元素 HTML5新增的，开始标签和结束标签，把文字变成黄底黑字；
> - del/ins元素 开始标签和结束标签，删除或者添加；
> - time元素 HTML5新增的，开始标签和结束标签，其实并不是很懂这个元素的用法；  

<h3 id='2.3'> 2.3 组织内容元素</h3>

>> 一个主要特点是内容元素是流，组织形式是块；
>>>>>> ![2.8 内容分组元素](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.8%20%E5%86%85%E5%AE%B9%E5%88%86%E7%BB%84%E5%85%83%E7%B4%A0.png?raw=true)  

>>>>>> 元素|元素类型|内容|元素结束方式|是否HTML5新增
>>>>>> -|-|-|-|-
>>>>>> p|流|短语内容|开始标签和结束标签|否
>>>>>> div|流|流内容|开始标签和结束标签|否
>>>>>> pre|流|短语内容|开始标签和结束标签|否
>>>>>> blockquote|流|流内容|开始标签和结束标签|否
>>>>>> hr|流|无|虚元素|否
>>>>>> ol|流|li元素|开始标签和结束标签|否
>>>>>> ul|流|li元素|开始标签和结束标签|否
>>>>>> li|无|流内容|开始标签和结束标签|否
>>>>>> dl dt dd|||开始标签和结束标签|否
>>>>>> figure|流|流内容,figcaption元素|开始标签和结束标签|是
>>>>>> figcaption|无|流内容|开始标签和结束标签|是

#### 1) 建立段落p
> - p元素 开始标签和结束标签
#### 2) 万能div
> - div元素 开始标签和结束标签，相当于文本元素的span元素，知识div元素应用于块形式；
> - 万不得已的时候不要使用div元素，因为它是万金油，如果有其他更加具体的元素应首先使用他们，这也会是选用元素的原则；
#### 3) 预先编排好的pre
> - pre元素 开始标签和结束标签，阻止浏览器合并连续空格，保留文本的源格式；
> - 尤其是与code元素搭配起来使用时特别有用；
#### 4) figure和figcaption
> - HTML5是这样定义figure：一个独立的内容单元，可带标题。通常作为一个整体被文档的主体引用，把它从文档主体中删除也不会影响文档的意思；
> - figcaption定义插图figure的标题；


























