# HTML

## 1.初识HTML

###	1.1 什么是HTML？

HTML是一种描述网页的语言，称为超文本标记语言，（它不是编程语言），所谓标记语言就是提供了一套标记标签

网页：网页是网站的构成的基本元素，一个网站是由一个或者多个网页组成，网页其实就是一个文件（超文本标记语言格式），该文件的后缀名：`html/htm`

- 静态网页：网站内容是预先定义好的，每个看到的网页的内容都是一样
- 动态网页：取决于用户提供的参数，例如：每个人看到的购买网站的内容都是不一样

### 	1.2 HTML的基本框架

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

</body>
</html>
```


## 2.网页基本信息

2.1  DOCTYPE:告诉浏览器，我们要使用什么规范

2.2  head标签代表网页头部

2.3  meta描述性标签，它用来描述我们网站的一些信息

2.4  title网页标题 

2.5  body标签代表网页主体

```html
<!DOCTYPE html>
<html lang="en">
<!-- head标签代表网页头部 -->
<head>
    <meta charset="UTF-8">
    <!-- title网页标题 -->
    <title>我的第一个网页</title>
</head>
<!-- body标签代表网页主体 -->
<body>
hello world!
</body>
</html>
```

## 3.网页基本标签

- 标题标签

- 段落标签

- 换行标签

- 字体样式标签

- 注释
  
  标题标签
  ```
  <h1>一级标签</h1>
  <h2>二级标签</h2>
  <h3>三级标签</h3>
  <h4>四级标签</h4>
  <h5>五级标签</h5>
  <h6>六级标签</h6>
  ```
  
  段落标签
  ```
  <p>第一段</p>
  <p>第二段</p>
  <p>第三段</p>
  <p>第四段</p>
  <p>第五段</p>
  ```
  
  换行标签
  ```
  换行1<br />
  
  换行2<br />
  ```
  
  <!-- 粗体、斜体 -->
  字体样式标签
  ```
  粗体:<strong>粗体</strong>
  斜体:<em>斜体</em>
  <br />
  ```
  注释
  ```
  <!--  这就是注释 -->
  ```

## 4.图像标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>图像标签笔记</title>
</head>
<body>
<!-- img标签笔记

src:图片地址（相对地址和绝对地址）
    ../   --上一级目录
    
alt:图片名字

title：鼠标悬停文字提示

width: 图片宽度  height：图片高度
-->
<img src="../html/ /" alt="照片" title = "悬停文字" width="200">
</body>
</html>
```

## 5.超链接

###	5.1 概念

链接，即从一个页面链接到另一个页面
###     5.2 代码展示

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>超链接学习</title>
</head>
<body>
<h2>页面间链接</h2>
<a name = "top"></a>
<!-- a标签
href: 必填，表示要跳转到哪个页面 target： 表示窗口在哪里打开
    _blank：在新标签中打开  _self: 在自己的网页中打开
-->
<a href="1.初识HTML.html" target = "_blank">点击我跳转页面</a>
<a href="https://www.baidu.com" target = "_self">点击我跳转到百度</a>
<br />
</body>
</html>
```

## 6.块元素和行内元素

### 6.1 块元素

无论内容多少，该元素独占一行，如段落标签（p）、标题标签（h1~h6）等。

### 6.2 行内标签

内容撑开宽度，左右都是在行内元素的可以再排在一行，如a、strong、em等。

## 7.列表标签

### 7.1 什么是列表

列表就是信息资源的一种展示形式。它可以使信息结构化和条理化，并以列表的形式显示出来，以便浏览者能更快捷地获取相应的信息

##### 7.2列表的分类

1. 无序列表

2. 有序列表

3. 自定义列表

   7.2.1 代码展示

   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <title>列表笔记</title>
   </head>
   <body>
       <!-- 有序列表 <ol>
        应用范围：试卷、问答……
        -->
       <ol>
           <li>Java</li>
           <li>Python</li>
           <li>C#</li>
           <li>C</li>
       </ol>
       <hr />
       <!-- 无序列表 <ul>
       应用范围：导航、侧边栏……
       -->
       <ul>
           <li>Java</li>
           <li>Python</li>
           <li>C#</li>
           <li>C</li>
       </ul>
       <!-- 自定义列表 <dl>
       dl:标签
       dt:列表名称
       dd:列表内容
       使用范围：公司网站底部
       -->
   <dl>
       <dt>学科</dt>
   
       <dd>Java</dd>
       <dd>Python</dd>
       <dd>Linux</dd>
       <dd>C</dd>
   
       <dt>位置</dt>
   
       <dd>重庆</dd>
       <dd>西安</dd>
       <dd>沈阳</dd>
       <dd>辽宁</dd>
   </dl>
   </body>
   </html>
   ```

## 8.表格标签

### 8.1为什么要使用表格

1）简单通用

2）结构稳定

##### 8.2 代码展示

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表格笔记</title>
</head>
<body>
<!--表格table
行 tr
列 td
-->
<table border="1" cellpadding="3">
  <tr>
    <!-- rowspan 跨行 -->
    <td rowspan="3" align="center">学科</td>
  </tr>
  <tr>
    <td>语文</td>
    <td >数学</td>
    <td>英语</td>
    <td>政治</td>
  </tr>
  <tr>
    <!-- colspan 跨列 -->
    <td colspan="2" align="center">位置</td>
    <td>湖北</td>
    <td>安徽</td>
  </tr>
</table>
</body>
</html>
```
