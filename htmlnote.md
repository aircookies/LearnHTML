# HTML5学习笔记

## 第一个 HTML

每个网页都会有一个基本的结构标签(也称为骨架标签),页面内容也是在这些基本标签上书写.

| 标签名 | 定义 | 说明 |
| --- | --- | --- |
| `<html>` `</html>` | HTML的标签 | 页面中最大的标签,我们称为根标签 |
| `<title>` `</title>` | 文档的标题 | 让页面拥有一个属于自己的网页标题 |
| `<body>` `</body>` | 文档的主体 | 元素包含文档的所有内容,页面内容基本都是放在`<body>`里面的 |

---

## 文档类型声明标签

`<!DOCTYPE>` 文档类型声明,作用就是告诉浏览器使用哪种HTML版本显示网页.
> `<!DOCTYPE html>`

**这行代码的意思是:当前页面采取的是HTML5版本来显示网页.**

**注意:**

1. `<!DOCTYPE>`声明位于文档中最前面的位置,处于HTML标签之前.
2. `<!DOCTYPE>`不是一个HTML标签,它就是文档类型声明标签.

---

## 字符集

字符集(Character set)是多个字符的集合.以便计算机能够识别和存储各种文字.
在`<head>`标签内,可以通过`<meta>`标签的`<charset>`属性来规定HTML文档应该使用哪种字符编码.
> `<meta charset="UTF-8" />`

---

## HTML常用标签

### 标题标签`h1`-`h6`(重要)

为了使网页更具有语义化,我们经常会在页面中用到标题标签.HTML提供了6个等级的网页标题,即`<h1>`~`<h6>`.
> `<h1>` 我是一级标题 `</h1>`

### 段落和换行标签(重要)

在网页中,要把文字有条理地显示出来,就需要将这些文字分段显示.在HTML标签中,`<p>`标签用于定义段落,它可以将整个网页分为若干段落.
> `<p>` 我是一个段落标签 `</p>`

单词paragraph的缩写,意为段落.
标签语义:可以把HTML文档分割为若干段落.

#### 段落标签特点

1. 文本在一个段落中会根据浏览器窗口的大小自动换行.
2. 段落和段落之间会保有空隙.

在HTML中,一个段落中的文字会从左到右依次排列,直到浏览器窗口的右端,然后才自动换行.如果希望某段文本强制换行显示,就需要使用换行标签`<br />`.
> `<br />`

单词break的缩写,意为打断,换行.
标签语义:强制换行.

#### 换行标签特点

1. `<br />`是个单标签.
2. `<br />`标签只是简单地开始新的一行,跟段落不一样,段落之间会插入一些垂直的间距.

### 文本格式化标签

在网页中,有时需要为文字设置粗体,斜体或下划线等效果,这时就需要用到HTML中的文本格式化标签,使文字以特殊的方式显示.

标签语义:突出重要性,比普通文字更重要.

| 语义 | 标签 | 说明 |
| --- | --- | --- |
| 加粗 | `<strong></strong>`或者`<b></b>` | 更推荐使用`<strong>`标签,语义更强烈 |
| 倾斜 | `<em></em>`或者`<i></i>` | 更推荐使用`<em>`标签,语义更强烈 |
| 删除线 | `<del></del>`或者`<s></s>` | 更推荐使用`<del>`标签,语义更强烈 |
| 下划线 | `<ins></ins>`或者`<u></u>` | 更推荐使用`<ins>`标签,语义更强烈 |

### `<div>`和`<span>`标签

`<div>`和`<span>`是没有语义的,他们就是一个盒子,用来装内容的.

> `<div>` 这是头部 `</div>`
> `<span>` 今日价格 `</span>`

div是division的缩写,表示分割,分区.span意为跨度,跨距.

#### `<div>`和`<span>`标签特点

1. `<div>`标签用来布局,但是现在一行只能放一个`<div>`.大盒子.
2. `<span>`标签用来布局,一行上可以有多个`<span>`.小盒子.

### 图像标签和路径标签(重点)

#### 1.图像标签

在HTML标签中,`<img>`标签用于定义HTML页面中的图像.

> `<img src="图像URL" />`

单词image的缩写,意为图像.

src是`<img>`标签的必须属性,它用于指定图像文件的路径和文件名.

图像标签的其他属性:

| 属性 | 属性值 | 说明 |
| --- | --- | --- |
| src | 图片路径 | 必须属性 |
| alt | 文本 | 替换文本.图像不能显示的文字 |
| title | 文本 | 提示文本.鼠标放到图像上,显示的文字 |
| width | 像素 | 设置图像的宽度 |
| height | 像素 | 设置图像的高度 |
| border | 像素 | 设置图像的边框粗细 |

图像标签属性注意点:

1. 图像标签可以拥有多个属性,必须写在标签名的后面.
2. 属性之间不分先后顺序,标签名与属性,属性与属性之间均以空格分开.
3. 属性采取键值对的格式,即key="value"的格式,属性="属性值".

### 超链接标签(重点)

#### 1.连接的语法格式

> `<a href="跳转目标" target="目标窗口的弹出方式"> 文本或图像 </a>`

单词anchor的缩写,意为:锚.

两个属性作用如下:

| 属性 | 作用 |
| --- | --- |
| href | 用于链接目标的URL地址,(必须属性)当为标签应用href属性时,它就具有了超链接的功能 |
| target | 用于指定链接页面的打开方式,其中_self为默认值,_blank为在新窗口中打开方式. |

#### 2.链接分类

1. 外部链接,例如`<a href="http://www.bilibili.com"> 哔哩哔哩 </a>`.
2. 内部链接,网站内部页面之间的相互链接.直接链接内部页面名称即可,例如`<a href="index.html">` 首页 `</a>`.
3. 空链接,如果当时没有确定链接目标时,`<a href="#"> 首页 </a>`.
4. 下载链接,如果href里面的地址是一个文件或压缩包,会下载这个文件.
5. 网页元素链接,在网页中的各种网页元素,如文本,图像,表格,音频,视频等都可以添加超链接.
6. 锚点链接,点击链接,可以快速定位到页面中的某个位置.
   - 在链接文本的href属性中,设置属性值为 **#名字** 的形式,如:`<a href="#transfer"> 传送锚点 </a>`
   - 找到目标位置标签,里面添加一个 **id=刚才的名字** ,如:`<h3 id="transfer"> 目的地 </h3>`

---

## HTML中的注释和特殊字符

### 注释

如果需要在HTML文档中添加一些便于阅读和理解但又不需要显示在页面中的注释文字,就需要使用注释标签.
HTML中的注释以`<!--`开头,以`-->`结束.

### 特殊字符

在HTML页面中,一些特殊的符号很难或者不方便直接使用,此时我们就可以使用下面的字符来替代.

| 特殊字符 | 描述| 字符的代码 |
| --- | --- | --- |
| | 空格符 | `&nbsp;` |
| &quot; | 双引号 | `&quot;` |
| < | 小于号 | `&lt;` |
| > | 大于号 | `&gt;` |
| & | 和号 | `&amp;` |
| &yen; | 人民币 | `&yen;` |
| &copy; | 版权 | `&copy;` |
| &reg; | 注册商标 | `&reg;` |
| &deg; | 摄氏度 | `deg;` |
| &plusmn; | 正负号 | `&plusmn;` |
| &times; | 乘号 | `&times;` |
| &divide; | 除号 | `&divide;` |
| &sup2; | 平方 | `&sup2;` |
| &sup3; | 立方 | `&sup3;` |

---

### 表格标签

表格是实际开发中常用的标签:

#### 表格的基本语法

```   html
<table>
   <tr>
      <td> 单元格内的文字 </td>
      ...
   </tr>
   ...
</table>
```

1. `<table></table>`是用于定义表格的标签.
2. `<tr></td>`标签用于定义表格中的行,必须嵌套在`<table></table>`标签中.
3. `<td></td>`用于表示表格中的单元格,必须嵌套在`<tr></tr>`标签中.
4. 字母'td'指表格数据(table data),即单元格里的数据.

#### 表头单元格

一般表头单元格位于表格的第一行或第一列,表头单元格里面的文本内容加粗居中显示.
`<th>`标签表示HTML表格的表头部分(table head的缩写)

``` html
<table>
   <tr>
      <th> 姓名 </th>
      ...
   </tr>
   ...
</table>
```

#### 表格属性

表格属性在实际开发中不常用,后期可通过CSS来设置.

| 属性名 | 属性值 | 描述 |
| --- | --- | --- |
| align | left,center,right | 规定表格相对周围元素的对齐方式. |
| border | 1或"" | 规定表格单元是否拥有边框,默认为"",表示没有边框. |
| cellpadding | 像素值 | 规定单元边沿与其内容之间的空白,默认1像素. |
| cellspacing | 像素值 | 规定单元格之间的空白,默认2像素. |
| width | 像素值或百分比 | 规定表格的宽度 |
| hight | 像素值或百分比 | 规定表格的高度 |

#### 表格结构标签

使用场景:因为表格可能很长,为了更好的表示表格的语义,可以将表格分割成表格头部和表格主体两部分.
在表格标签中,分别用`<thead>`标签表格的头部区域,`<tbody>`标签表格的主体区域.这样更好的分清表格结构.

1. `<thead></thead>`用于定义表格的头部.`<thead>`内部必须拥有`<tr>`标签.一般位于第一行.
2. `<tbody></tbody>`用于定义表格的主体,主要用于放数据本体.

#### 合并单元格

##### 合并单元格方式

- 跨行合并:rowspan="合并的单元格个数"
- 跨列合并:colspan="合并的单元格个数"

##### 目标单元格(写合并代码)

- 跨行:最上侧单元格为目标单元格,写合并代码
- 跨列:最左侧单元格为目标单元格,写合并代码

---

#### 列表标签

表格是用来显示数据的,那么列表就是用来布局的.
列表最大的特点就是整齐,整洁,有序,它作为布局会更加自由方便.

根据使用场景不同,列表可以分为三大类:无序列表,有序列表和自定义列表.

##### 无序列表(重点)

`<ul>`标签表示HTML页面中项目的无序列表,一般会以项目符号呈现列表项,而列表项使用`<li>`标签定义.

无序列表的基本语法格式如下:

``` html
<ul>
   <li>列表项1</li>
   <li>列表项2</li>
   <li>列表项3</li>
   ...
</ul>
```

ul是unordered list(无序列表)的缩写.
li是list(列表)的缩写.

1. 无序列表的各个列表项之间是没有顺序级别之分的,是并列的.
2. `<ul></ul>`中只能嵌套`<li></li>`,直接在`<ul></ul>`输入其他标签或者文字是不被允许的.
3. `<li>`与`<li/>`之间相当于一个容器,可以容纳所有元素.
4. 无序列表会带有自己的样式属性,但在实际使用时,我们会用CSS来设置.

##### 有序列表(理解)

有序列表即有排序的列表,其各个表项会按照一定顺序排列.

在HTML标签中,`<ol>`标签用于定义有序列表,列表排序用数字来显示,并且使用`<li>`标签来定义列表项.

有序列表的基本语法如下:

``` html
<ol>
   <li>列表项1</li>
   <li>列表项2</li>
   <li>列表项3</li>
   ...
</ol>
```

ol是ordered list(有序列表)的缩写.
li是list item的缩写.

1. `<ol></ol>`中只能嵌套`<li></li>`,直接在`<ol></ol>`标签中输入其他标签或者文字的做法是不允许的.
2. `<li>`与`</li>`之间相当于一个容器,可以容纳所有元素.
3. 有序列表会带有自己的样式属性,但在实际使用时,我们会使用CSS来设置.

##### 自定义列表(重点)

自定义列表的使用场景:
自定义列表常用于对术语或名词进行解释和描述,定义列表的列表项前没有任何项目符号.

在HTML标签中,`<dl>`标签用于定义描述列表(或定义列表),该标签会与`<dt>`(定义项目/名字)和`<dd>`(描述每一个项目/名字)一起使用.

其基本语法如下:

``` html
<dl>
   <dt>名词</dt>
   <dd>解释1</dd>
   <dd>解释2</dd>
</dl>
```

dl是describe list(描述列表)的缩写.

1. `<dl></dl>`中只能包含`<dt>`和`<dd>`.
2. `<dt>`和`<dd>`没有个数限制,经常是一个`<dt>`对应多个`<dd>`.

##### 列表总结

| 标签名 | 定义 | 说明 |
| --- | --- | --- |
| `<ul></ul>` | 无序标签 | 里面只能包含`<li>`,没有顺序,使用较多.`<li>`里面可以包含任何标签. |
| `<ol></ol>` | 有序标签 | 里面只能包含`<li>`,有顺序,使用相对较少.`<li>`里面可以包含任何标签. |
| `<dl></dl>` | 自定义标签 | 里面只能包含`<dt>`和`<dd>`.`<dt>`和`<dd>`里面可以放任何标签. |

---

#### 表单标签

使用表单的目的是为了收集用户信息.

##### 表单的组成

在HTML中,一个完整的表单通常由**表单域**,**表单控件(也称为表单元素)**和**提示信息**3个部分组成.

##### 表单域

**表单域**是一个**包含表单元素的区域**.

在HTML标签中,`<form>`标签用于定义表单域,以实现用户信息的收集和传递.

**`<form>`**会把它范围内的表单元素交给服务器.

```   html
<form action="url地址 method="提交方式" name="表单域名称">
   各种表单元素控件
</form>
```

常用属性

| 属性 | 属性值 | 作用 |
| --- | --- | --- |
| action | url地址 | 用于指定接收并处理表单数据服务器程序的url地址. |
| method | get/post | 用于设置表单数据的提交方式,取值为get或post. |
| name | 名称 | 用于指定表单域的名称,以区分同一个页面中的多个表单域. |

1. 在写表单元素之前,应该有个表单域把他们进行包含.
2. 表单域是form标签.

##### 表单元素

1. input输入表单元素
2. seelct下拉表单元素
3. textarea文本域表单元素

###### `<input>`表单元素

在英文单词中,input是输入的意思,而在表单元素中 **`<input>`用于收集用户信息.**

在`<input>`标签中,包含一个**type**属性,根据不同的**type属性值**,输入字段拥有很多种形式(可以是文本字段,复选框,掩码后的文本控件,单选按钮,按钮等).

```   html
<input type="属性值" />
```
  
- `<input />`为单标签
- type属性设置不同的属性值用来指定不同的控件类型

**type**属性的属性值及其描述如下:

| 属性值 | 描述 |
| --- | --- |
| button | 定义可点击按钮(多数情况下,用于通过JavaScript启动脚本). |
| checkbox | 定义复选框. |
| file | 定义输入字段和"浏览"按钮,供文件上传. |
| hidden | 定义隐藏的输入字段. |
| image | 定义图像形式的提交按钮. |
| password | 定义密码字段.该字段中的字符被掩码. |
| radio | 定义单选按钮. |
| reset | 定义重置按钮.重置按钮会清除表单中的所有数据. |
| submit | 定义提交按钮.提交按钮会把表单数据发送到服务器. |
| text | 定义单行的输入字段,用户可在其中输入文本.默认宽度为20个字符. |

除type属性以外,`<input>`标签还有其他很多属性,其常用属性如下:

| 属性 | 属性值 | 描述 |
| --- | --- | --- |
| name | 由用户自定义 | 定义input元素的名称. |
| value | 由用户自定义 | 规定input元素的值. |
| checked | checked | 规定此input元素首次加载时应当被选中. |
| maxlength | 正整数 | 规定输入字段中的字符的最大长度. |

1. name和value是每个表单都有的属性值,主要给后台人员使用.
2. name表单元素的名字,要求**单选按钮和复选框要有相同的name值.**
3. **checked属性主要针对于单选按钮和复选框,** 主要作用是打开页面就可以默认选中某个表单元素.
4. maxlength是用户可以在表单元素输入的最大字符数,一般较少使用.

有些表单元素想刚打开就默认显示几个文字该怎么做?

答:可以给这些表单元素设置value属性="值"

``` html
用户名:<input type="text" value="请输入用户名" />
```

页面中的表单元素很多,如何区分不同的表单元素?

答:name属性=当前表单的名字,后台可以通过name属性找到这个表单.页面中的表单很多,name的主要作用就是用于区分不同的表单.

``` html
用户名: <input type="text" value="请输入用户名" name="username" />
```

- name 属性后面的值是自定义的.
- radio(或者checkbox)如果是一组,我们必须给他们命名相同的名字.

如果页面一打开就让某个单选按钮或者复选框是选中状态?

答:checked属性,表示默认选中状态,用于单选按钮和复选按钮.

``` html
性别:
<input type="radio" name="sex" value="男" checked="checked" />男
<input type="radio" name="sex" value="女" />女
```

如何让input表单元素展现不同的形态?比如单选按钮或者文本框.

答:type属性,type属性可以让input表单元素设置不同的形态.

###### `<lable>`标签

`<label>`标签为input元素定义标注(标签).

`<label>`标签用于绑定一个表单元素,当点击`<label>`标签内的文本时,浏览器就会自动将焦点(光标)转到或者选择对应的表单元素上,用来增加用户体验.

**语法:**

``` html
<label for="sex">男</label>
<input type="radio" name="sex" id="sex" />
```

核心:`<label>`标签的for属性应当与相关元素的id属性相同.

###### `<select>`表单元素

使用场景:在页面中,如果有多个选项让用户选择,并且想要节省页面空间时,我们可以使用`<select>`标签控件定义**下拉列表.**

**语法:**

``` html
<select>
   <option>选项1</option>
   <option>选项2</option>
   <option>选项3</option>
   ...
</select>
```

1. `<select>`中至少包含一对`<option>`.
2. 在`<option>`定义select="selected"时,当前项即为默认选中项.

---

###### `<textarea>`表单元素

使用场景:当用户输入内容较多的情况下,我们就不能使用文本框表单了,此时我们可以使用`<textarea>`标签.

在表单元素中,`<textarea>`标签是用于定义多行文本输入的控件.

**语法:**

``` html
<textarea rows="3" cols="20">
   文本内容
</textarea>
```