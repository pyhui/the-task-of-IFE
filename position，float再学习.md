## position，float再学习
*  **当盒子宽度都规定好时，可以用float进行多栏布局**
*     **特殊的三栏布局左右两栏宽度规定好，中间一栏自适应时，应该采取position的绝对定位**
       * 例如本题中，采用左右浮动，每栏会被上一栏挤下去，采用绝对定位方式，如下  
          * 最左栏添加样式   `position: absolute; left: 40px;top: 30px;`  
          *	最右一栏添加样式   `position: absolute;right: 40px;	top: 30px;`
          *	中间一栏添加边界值  `margin:0px 145px 0 220px;`
          *	*但是当规定了中间一栏bottom值后，会发现最右一栏比中间栏长时会溢出，怎样才能使最大的包裹的盒子高度为三个小盒子的高度最大值呢？粗暴地增加了中间栏文字，使之高度最高*

* **清除浮动**（清除浮动带来的影响）
  * 方法一:clear--(仍与外部接触） 
     * 1.浮动元素底部加<div>插入`clear：both`样式  
     * 2.css :after伪元素（IE6/IE7不兼容）
        
  * 方法二:BFC（IE8+）/haslayout（IE6/IE7）--(包裹起来，形成封闭结构，不对外部产生影响)
     * 浮动元素父元素添加`overflow:hidden`样式  
     `.clearfix:after{content:'';display:table;clear:both;}   (IE8)
       .clearfix{*zoom:1;}   (IE6/IE7)
       clearfix应用在包含浮动子元素的父元素上`
