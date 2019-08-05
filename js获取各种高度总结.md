话不多说，先上图
<img src="https://images2017.cnblogs.com/blog/1219513/201708/1219513-20170817141747443-425001125.png">


注：上图未标出外边距margin，CSS中的margin属性，与clientWidth、offsetWidth、clientHeight、offsetHeight等均无关

1. client 内部宽度系列
   窗口可视区域的宽度（不加border、padding、margin）：
   document.body.clientWidth || document.documentElement.clientWidth;
   窗口可视区域的高度（不加border、padding、margin）：
   document.body.clientHeight || document.documentElement.clientHeight;
2. offset 偏移的像素值系列
   可视区域的width+padding+border:
   document.body.offsetWidth;
   可视区域的height+padding+border:
   document.body.offsetHeight;
   元素(含width+padding+border)的宽度：
   obj.offsetWidth;
   元素(含width+padding+border)的高度：
   obj.offsetHeight;
   相对于父元素的上位移（在元素的包含元素不含滚动条的情况下）：
   obj.offsetTop;
   相对于父元素的左位移（在元素的包含元素不含滚动条的情况下）：
   obj.offsetLeft;
3. scroll 滚动系列
   （可以是document.body或obj等）实际内容的宽度 或 对象滚动的宽度:  offsetWidth
   （可以是document.body或obj等）实际内容的高度 或 对象滚动的高度:  offsetHeight
   滚动对象侧边卷起的宽度：scrollLeft
   滚动对象上边卷起的高度：scrollTop
   

参考：

https://www.jb51.net/article/103459.htm

https://blog.csdn.net/leileibrother/article/details/78686250

https://www.cnblogs.com/sunnywindycloudy/p/7381378.html