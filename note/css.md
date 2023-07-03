# css
## 1.什么是CSS？
CSS（层叠样式表）是一种用于描述网页上元素样式的语言。它可以控制文档的布局、颜色、字体、大小等外观，使得网页具有更好的可读性和视觉效果。

## 2. 选择器
在CSS中，选择器用于选择要应用样式的HTML元素。常见的选择器有：

##### 2.1 标签选择器
标签选择器是指用HTML标记名称作为选择器，按标记名称分类，为页面中某一类标签指定统一的CSS样式。
基本语法格式：标签名{ 属性1：属性值1；属性2：属性值2；}
所有的HTML标记名都可以作为标签选择器，例如a、body、p、h1等等.
```
p{ font-size: 12px; color: #666; font-family:"微软雅黑"; }
```

##### 2.2 类选择器：
类选择器使用**‘.’**(英文点号)进行标识，后面紧跟类名。
基本语法格式：.类名{ 属性1：属性值1；属性2：属性值2；}
该语法中，类名即为HTML元素的class属性值，大多数HTML元素都可以定义class属性。
```html
1 <!DOCTYPE html>
2 <html lang="en">
3 <head>
4 <meta charset="UTF-8">
5 <title>类选择器</title>
6 <style type="text/css">
7  .red{color: red;}
8  .green{color:green;}
9  .font22{font-size:22px;}
10 p{ text-decoration:underline; font- family:"微软雅黑"; }
11 </style>
12 </head>
13 <body>
14 <h2 class="red">二级标题文本</h2>
15 <p class-"green font22">段落文本内容</p>
16 <p class="red font22">段落二文本内容</p>
17 <p>段落三文本内容</p>
18 </body>
19 </html>
```

##### 2.3 ID选择器：
id选择器使用**‘#’**进行标识，后面紧跟id名。
基本语法格式：#id名{ 属性1：属性值1；属性2：属性值2；}
该语法中，id名即为HTML元素的id属性值，大多数HTML元素都可以定义id属性，元素的id值是唯一的，只能对应于文档中某一个具体的元素。
```html
1 <!DOCTYPE html>
2 <html lang="en">
3 <head>
4 <meta charset="UTF-8">
5 <title>id选择器</title>
6 <style type="text/css">
7 #bold{font -weight:bold; }
8 #font24 {font-size:24px; }
9 </style>
10 </head>
11 <body>
12 <pidf"bold">段落1: id="bold",设置粗体文字。</p>
13 <p id="font24">段落2: id="font24", 设置字号为24px。</p>
14 <p id="font24">段落3: id="font24", 设置字号为24px。</p>
15 <pid="bold font24">段落4: id="bold font24",同时设置粗体和字号24px。</p>
16 </body>
17 </html>
```
## 3. 属性和值
CSS样式由属性和对应的值组成。常见的属性包括：

### 3.1 color：设置文本颜色。
color: red
### 3.2font-size：设置字体大小。
font-size: 40px
### 3.3background-color：设置背景颜色。
background-color: red
### 3.4width：设置元素宽度。
width: 100px
### 3.5height：设置元素高度。
height: 100px
## 4. 盒模型
在CSS中，每个HTML元素都被看作一个矩形框，称为盒子。盒模型由内容区、内边距、边框和外边距组成。

### 内容区：显示元素的实际内容。
### 内边距：位于内容区与边框之间，可以设置背景色和边距。
### 边框：包围内容和内边距，可以设置边框样式、宽度和颜色。
### 外边距：位于边框与其他元素之间，可以控制元素之间的间距。
### 边框 

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8"> 
        <title>边框</title> 
        <style>
            p.none {border-style:none;}
            p.dotted {border-style:dotted;}
            p.dashed {border-style:dashed;}
            p.solid {border-style:solid;}
            p.double {border-style:double;}
            p.groove {border-style:groove;}
            p.ridge {border-style:ridge;}
            p.inset {border-style:inset;}
            p.outset {border-style:outset;}
            p.hidden {border-style:hidden;}
            p.mix {border-style: dotted dashed solid double;}
        </style>
    </head>
    <body>
        <p class="none">无边框。</p>
        <p class="dotted">虚线边框。</p>
        <p class="dashed">虚线边框。</p>
        <p class="solid">实线边框。</p>
        <p class="double">双边框。</p>
        <p class="groove"> 凹槽边框。</p>
        <p class="ridge">垄状边框。</p>
        <p class="inset">嵌入边框。</p>
        <p class="outset">外凸边框。</p>
        <p class="hidden">隐藏边框。</p>
        <p class="mix">混合边框</p>
    </body>
</html>
```

### 轮廓 

outline	在一个声明中设置所有的轮廓属性  
* outline-color
* outline-style
* outline-width
* inherit

outline-color	设置轮廓的颜色	color-name  
* hex-number
* rgb-number
* invert
* inherit

outline-style	设置轮廓的样式	none  
* dotted
* dashed
* solid
* double
* groove
* ridge
* inset
* outset
* inherit

outline-width	设置轮廓的宽度	thin  
* medium
* thick
* length
* inherit

### 外边距 

```css
margin-top:100px;
margin-bottom:100px;
margin-right:1.5em;
margin-left:1.75em;
```
### 内边距
```css
padding-top:100px
padding-right:100px
padding-bottom:100px
paing-left:100px
```