## css 绘制图形

#### 三角形边框
1、margin 方法
```html
<div class="demo1">
    <em>&#9670;</em>
    <span>&#9670;</span>
</div>
```
```css
.demo1{width:300px;margin:20px auto;border:1px solid red;height:100px;}
.demo1 em,.demo1 span{display:block;width:30px;height:16px;font-size:30px;overflow:hidden;_position:relative;margin-left:10px;}
.demo1 em{margin-top:-16px;color:#e4e4e4;font-style:normal;}
.demo1 span{margin-top:-14px;color:white;}
```
2、position 方法
```html
<div class="demo2">
    <em>&#9670;</em>
    <span>&#9670;</span>
</div>
```
```css
.demo2{width:300px;border:1px solid #F00;height:100px;position:relative;margin-left:auto;margin-right:auto;}
.demo2 em,.demo2 span{font-style:normal;font-size:30px;position:absolute;left:-16px;top:40px;color:red;}
.demo2 span{left:-14px;color:white;}
```
3、可以用背景图片
