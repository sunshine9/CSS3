# CSS3 新元素

#### input 边框线性渐变
```css
        input{
            width:250px;
            height:40px;
            -webkit-border-image: -webkit-linear-gradient(left, #ffd502, #ff01e9, #ffd502, #ff01e9) round;
            -moz-border-image:-moz-linear-gradient(left, #ffd502, #ff01e9, #ffd502, #ff01e9) round;
            -o-border-image:-o-linear-gradient(left, #ffd502, #ff01e9, #ffd502, #ff01e9) round;
            -ms-border-image:-ms-linear-gradient(left, #ffd502, #ff01e9, #ffd502, #ff01e9) round;
            border-image:linear-gradient(left, #ffd502, #ff01e9, #ffd502, #ff01e9) round;
            border-image-slice: 1;
        }
```
