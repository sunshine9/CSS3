## css 浮动布局

##### css 右边固定 左边自适应
```html
    <div class="slide">slide</div>
    <div class="content">content</div>
```
```css
.content{
	background: red;
	margin-right:200px;
}
.slide{
	width:200px;
	float:right;
	background: green;
}
```

--

##### css 左边固定 右边自适应
```html
<div class="slide">slide</div>
    <div class="content">content</div>
```

```css
.slide {
        float: left;
        width: 220px;
        background-color: green;
    }
    
    .content {
        background-color: orange;
        margin-left: 220px;
        /*==等于左边栏宽度==*/
    }
```
