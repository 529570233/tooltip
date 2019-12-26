# tooltip
tooltip提示工具


# Usage
**1.引入tooltip.js和style.css文件**
```html
<link rel="stylesheet" href="style.css">
<script src="tooltip.js"></script>
```

**2.DOM结构中**
```html
<li class="item" tip="Tooltip-top" direction="top">top</li>
<li class="item" tip="Tooltip-right" direction="right">right</li>
<li class="item" tip="Tooltip-bottom" direction="bottom">bottom</li>
<li class="item" tip="Tooltip-left" direction="left">left</li>
```
属性：
- tip：tooltip提示框中的文本内容；
- direction：tooltip提示框的位置，可选值为top/right/bottom/left

**3.JS中**
```js
tooltip('.item');
tooltip('.item', null, enterCallback, outCallback);
tooltip('.item', ｛transition: true｝, enterCallback, outCallback);tooltip('.item', ｛transition: true, time: 200｝, enterCallback, outCallback);
```
参数：
- '.item'：需要添加tooltip提示的目标元素，必填项；若只给一个元素添加tooltip，可以使用id     
- ｛transition: true[, time: 1000]｝: 过度效果，transition：是否添加过度效果，true为添加，false为不添加，默认为false，time：过度效果的持续时间（单位为毫秒，默认为200毫秒）     
- enterCallback：tooltip显示时的回调函数     
- outCallback：tooltip消失时的回调函数 
