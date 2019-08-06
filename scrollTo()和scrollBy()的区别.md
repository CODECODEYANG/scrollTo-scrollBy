## scrollTo()和scrollBy()的区别
**首先看一下W3C上scrollTo()和scrollBy()的介绍**

>scrollTo() 方法可把内容滚动到指定的**坐标**。

```
scrollTo(xpos,ypos)
```
| 参数 | 描述 | 
| --- | --- |
| xpos | 必需。要在窗口文档显示区左上角显示的文档的 x 坐标。| 
| ypos | 必需。要在窗口文档显示区左上角显示的文档的 y 坐标。| 

>scrollBy() 方法可把内容滚动到指定的**像素数**。

```
scrollBy(xnum,ynum)
```
| 参数 | 描述 | 
| --- | --- |
| xnum | 必需。把文档向右滚动的像素数。| 
| ynum | 必需。把文档向下滚动的像素数。| 

---
***
### 分别解释一下scrollTo()和scrollBy()
* scrollTo(xpos,ypos) 是滚动到某个绝对位置，即滚动到坐标为xpos,ypos的位置。
* scrollBy(xnum,ynum) 则是从当前位置滚动到某个相对位置，从当前位置起向右和向下滚动多少像素。
### 举个例子 在浏览器中运行下面的测试页面。按F12，在console控制台分别多次输入下面scrollBy和scrollTo，就可以很清楚的发现2者的区别：每一次执行scrollBy是当前的滚动条位置向下滚动10px，而执行scrollTo都是将元素滚动到指定位置，即和第一次是一样的位置。
* window.scrollBy(0,10)和window.scrollTo(0,10)

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>scroll</title>
</head>
<body>
<p>滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 </p>

<p>滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 </p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p>滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 </p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p>滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 </p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p>滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 </p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p>滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 </p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p>滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 </p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p>滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 </p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p>滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 滚动 </p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

</body>
</html>
```