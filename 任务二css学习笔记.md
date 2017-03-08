1. **如何利用CSS代码使图片和文字在同一行显示且对齐** 
  * 这个任务百度图标我用的是图片，而链接和图片出现在同一行或者同一个div里面的时候，在浏览器中运行出来的显示效果却是在不同的行，跑到别的div里了。
  * 先写的链接再写的图片，然后设置各种高度解决了，不知道是不是偶然情况。
  * nav标签
> Nav是与导航相关的，所以一般用于网站导航布局。同时完全就像使用div标签、span标签一样来使用<nav>标签可添加id或class，而与div标签又有不同处是，此标签一般只用于导航相关地方使用，所以在一个html网页布局中可能就使用在导航条处，或与导航条相关的地方布局使用。
  * 列表横行排列 `float:right;` 以及去掉点`list-style-type:none;`       	
  * 使用` vertical-align:middle;`好像没有用  
2. **行内元素 块级元素 内联元素**
     * 块级元素占一行，不论内容多少只要是有2个这样的元素就会换行，行内元素内容少时不会换行  
      [行内元素和块级元素](http://www.cnblogs.com/greenal/archive/2013/01/05/2845513.html)
        [html 行级元素和块级元素标签列表分别有哪些](https://zhidao.baidu.com/question/1988012763773636867.html)  

3. **边距 padding 与 margin** 
   * padding内边距 magin外边距
   * 顶部右边底部左边 ，距离为顺时针方向排列，可简写，如下
   `padding-top: 40px;
    padding-right: 20px;
    padding-bottom: 20px;
    padding-left: 40px;`  
				
	`padding: 40px 20px 20px 40px;`
	   * （用px定位方式给图片和文字外面加了框之后，偶然间缩小浏览器，框变小了没有包裹住，原来是相对定位绝对位置）
4. **绝对定位 相对定位？？**
    * position:relative;(相对定位)
    * position:absolute;(绝对定位)
    * position:static;(静态)
    * position:fixed;（固定定位）这里所固定的参照对像是可视窗口而并非是body或是父级元素。
       * 用相对位置relative终于将图片与文字外面的框弄好了呢，还学到了一个方法——用qq截图看图片大小
     `.box{
width:432px;
height: 432px;
margin:15px;
border:1px solid #333;
padding:20px;
position:relative;
top: 15px;
left: 15px;
}`
5. **边框上加文字**
   `<!DOCTYPE HTML>
    <html>  
   <body>  
   <form>  
   <fieldset>
    <legend>在边框上的字</legend>
    可以输入内容：<input type="text" />
    随便输入内容：<input type="text" />
   </fieldset>
   </form>
   </body>
   </html>`  
	      <legend>标签需要在<fieldset>标签里面才能正常使用
6. 通过css改变图片大小
      * 直接设置图片宽高   
      .`img{
    width: 100px;
    height: 80px;
    }`  
		
**问题：图片以及各种内容如何随着网页大小的改变而改变？**
