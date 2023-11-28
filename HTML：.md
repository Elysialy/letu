HTML：

1.标签使用说明书。

使用<>括起来，分开始标签和结束标签，结束标签比开始标签多一个/

标签之间可以嵌套，但是有先后顺序的分别。    

eg.（1）用<p>表示一个段落中的文本信息，每一段需要重新使用<p>来将这每一段分开    

（2）利用<hx>来表示标题的每个标签，例如<h1><h2>等等，数字越大表示等级越低，一般来讲<h1>最重要常常作为网站名称。

![img](https://img1.sycdn.imooc.com//528970d80001e67f01720125.jpg)

2.标签基本结构组成：

使用<!DOCTYPE>开头

使用<html>和</html>作为开头结尾标志

利用<head>和</head>包括HTML文件信息，其中可以添加如title标签等各类信息

<body>和</body>标签表示主体部分

*需要注意的是在head标签内需要首先设置<meta charset="UTF-8">来进行文件字符编码设置

3.注释文件的使用：格式<!--注释文字-->如此来添加相关的注释

4.利用<span>来自定义标签内文字格式     *利用span设置时span{ }内部应该每句话结束时增加；

5.利用<div>来为网页划分为独立的板块（section标签具有同样的作用但是更具语义化）

header标签（<hedar>与</hedar>)表示标题头部(写在主体部分内)

eg.

![img](https://img1.sycdn.imooc.com//5e946d130001b6ba25480108.jpg)

footer标签与之相应的就代表了底部标签

<aside></aside>aside标签则连同于div的作用，不过是在侧边更具语义化的区域部分。

6.文字结构设置。在HTML中的回车和空格会被自动忽略。如果真的需要换行时，我们应该使用<br />放置在句子末尾进行换行

而如果需要在文本中添加空格，则需要在文本中添加&nbsp加分号来表示空格

如果需要加图示的下划线，则需要采用<hr />标签

![img](https://img1.sycdn.imooc.com//52932bbc0001c12206620372.jpg)

如果需要列列表如图中带黑点的模式则可以采用<ul><li>列表</li><ul>（在<ul>内添加更多的<li>可以添加更多的列表）（呈现结果为无序状态）

![img](https://img1.sycdn.imooc.com//52d3851200012ec503870284.jpg)

而如果需要有序状态的列表，那么可以选择采用<ol><li>列表信息</li><ol>，结果如

![img](https://img1.sycdn.imooc.com//52d3893400019ee003830208.jpg)

7.网页图片设置。

使用<img>来插入图片格式如下：

<img src="myimage.gif"alt="my image"title="my image"/>其中src识别图像位置；alt指定图像的描述性文本，当图像不可见时（下载不成功），可看到属性指定文本；title提供图像可见时的图像描述，即鼠标滑过图片时的显示文本；图像可以是GIF,PNG,JPEG的形式

8.网页超链接设置。

使用<a>来设置网站超链接格式如下：

<a href="目标网址"title=“鼠标滑过显示的文本”>链接显示的文本</a>如下单击click here!网页链接道**http://www.imooc.com**这个网站

**eg.<a  href="http://www.imooc.com"  title="点击进入慕课网">click here!</a>**

9.新建窗口。

a标签有的target属性，代表打开网页的方式，可选择使用_(横杠)加self或者加blank分别表示在当前页面或新建窗口的方式打开页面如下

![img](https://img1.sycdn.imooc.com//5e917d9f000187c711100555.jpg)

10.使用table类为网页添加表格。

使用包括table,th,tr,td来添加在其中<table>....<table>建立整体框架，<th>...<th>表示表格表头<tr>...<tr>表示表格的一行<td>...<td>用来表示一行中的列数<boder>可以用来添加裱框，caption则表示标题标签相关用法如图：（*th默认粗体居中）

![img](https://img1.sycdn.imooc.com//5e9180d50001d1ec18461296.jpg)

*如何定义表格

<thead>(无需尾部）用来定义表格表头<tbody>.....</tbody>定义表身<tfoot>包裹表尾

这三类均为了为表格某一部分进行分组，能够使得表格更快的加载出来，不必等待表格完全下载之后再显示。

11.使用表单标签形成于用户交互的形式。

（把浏览者输入的数据传送到服务器端）

（1）建立服务器通道

形式如<form   method="传送方式"  action="服务器文件">如下：

```
<form    method="post"   action="save.php">
        <label for="username">用户名:</label>
        <input type="text" name="username" />
        <label for="pass">密码:</label>
        <input type="password" name="pass" />
</form>
```

（2）文本输入框（输入账户密码等）

形式如：

```
<form>
   <input type="text/password" name="名称" value="文本" />
</form>
```

其中如果type="text"时，输入框为文本输入框，type="password"时，输入框为密码输入框

name为文本框命名，为后台使用

values为文本框输入框设置默认值（起到提示作用）

举例：

```
<form>
  姓名：
  <input type="text" name="myName">
  <br/>
  密码：
  <input type="password" name="pass">
</form>
```

（3）提示用户输入框内容使用placeholder,形成如下效果

![img](https://img1.sycdn.imooc.com//5e918efa0001a01204260146.jpg)

类比（2）中使用，在此内容中我们使用方法如下：

![img](https://img1.sycdn.imooc.com//5e9195930001127311650493.jpg)

（4）密码输入框。

只需把<inpute type=".....">中的.....替换为numbei就行

（5）网址输入框

同理，将（4）中的......替换为url但是需要注意的是再输入网址的时候必须以http://或者https://开头，不然会报错

（6）邮箱输入框

同理，依然进行替换，不过这次替换为"email"但是注意必须包含@键且其后必须有内容

（7）创建文本域<textarea>,采用语法如下：

```
<textarea  rows="行数" cols="列数">文本
</textarea>
```

在<taxarea>标签之间可以输入默认值

举例：

```
<form  method="post" action="save.php">
        <label>联系我们</label>
        <textarea cols="50" rows="10" >在这里输入内容...</textarea>
</form>
```

11.使用label为input标签穿上衣服。

形式上如：<label for="控件id名称">但是要注意一点：

```
<form
  <label for="email">输入你的邮箱地址</label>
  <input type="email" id="email" placeholder="Enter email">
</form>
```

for中与id的属性值应该相同

12.单选框，复选框的建立

形式如：**<input   type="radio/checkbox"   value="值"    name="名称"   checked="checked"/>**

radio--->单选框checkbox-->多选框，注意同一组单选按钮name的取值应该相同。

13.创建下拉菜单（select与，option）

都是双标签，而且select里面只能放option标签，表示下拉列表的选项。

option标签放选项内容,不放置其他标签,例如：

![img](https://img1.sycdn.imooc.com//5e91a9c80001810a11210735.jpg)

14.提交按钮：

形式

```
<input   type="submit"   value="提交">
```

value代表按钮上面显示出来的文字

15.重置按钮

形式：

![img](https://img1.sycdn.imooc.com//52e618680001a6b204570101.jpg)