<html lang="en">
<head>
    <meta charset="UTF-8">
    <title></title>
</head>
<body marginheight="0"><h1>学习html的一些思考（task_1_1_1笔记）</h1>
<h2>表单相关</h2>
<h3>1.form标签的使用</h3>
<ul>
<li>到底需不需要使用form标签呢，第一个任务我没有使用，用与不用有什么区别吗，什么时候必须用form标签，什么时候可不用？ <blockquote>
<ol>
<li>所有向后台提交数据（包括原生和ajax提交）的input都建议用form包裹，如果只是用来做前台交互效果则不推荐使用form包裹  </li>
<li>form是表单，有一定的特殊的作用，一个是方便展示很多的数据，一个是为了想后台提交数据，有自己一定的标签意义，就像img和div同样都可以显示图片，只是在用的地方有写不一样，标签的意思等等。  </li>
</ol>
</blockquote>
</li>
</ul>
<h3>2.文本框内的文字如何点击即消失</h3>
<ul>
<li>怎样才能使本文框内原有（灰色）文字点击即消失，不需要使用者手工删除呢？<ul>
<li>需要在input的属性中添加onfocus="this.value=''" （<strong>方法来源网络</strong>）<pre><code>&lt;input type="text" value="这是一个文本输入框" onfocus="this.value=''"&gt;</code></pre>
</li>
<li>或者添加元素placeholder<pre><code>&lt;input type="text" placeholder="这是一个文本输入框"&gt;</code></pre>
</ul>
</li>
</ul>
<h3>3.radio默认选中一个元素后点击只选中一个元素</h3>
<ul>
<li>默认选中性别男后，再选性别女，怎么两个都选中了呢？<ul>
<li>添加name属性，使属性值相同  <pre><code>&lt;input type="radio" name="sex" checked="checked"&gt;男
&lt;input type="radio" name="sex" &gt;女</code></pre>
</li>
</ul>
</li>
</ul>
<h3>总结：简单的一些html之前都有接触过，只要多练便可熟悉，这个任务虽然简单但是里面肯定也有要改进的地方，而且第一个task我就拖了很久才来做，拖延症没救了，也不知道能坚持多久。</h3>
<p>Edit By <a href="http://mahua.jser.me">MaHua</a></p>
</body></html>
