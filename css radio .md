## 样式化checkbox/radio/select/input[type=file]等


####　样式化 checkbox
```html
<div class="checkbox">
  <input id="exampleCheckbox" type="checkbox">
  <label for="exampleCheckbox"></label>
</div>
```
```css
.checkbox {
  min-height: 24px;
  padding-left: 24px;
  position: relative;
}
input[type="checkbox"] {
  box-sizing: border-box;
  left: 4px;
  margin: 0;
  padding: 0;
  position: absolute;
  top: 3px;
}
input[type="checkbox"] + label:before {
  background: #fff url(i/blue.png);
  content: " ";
  height: 22px;
  left: 0;
  position: absolute;
  width: 22px;
}
input[type="checkbox"]:focus + label:before,
input[type="checkbox"] + label:hover:before {
  background-position: -24px 0;
}

input[type="checkbox"]:checked + label:before {
  background-position: -48px 0;
}

input[type="checkbox"][disabled] + label:before {
  background-position: -72px 0;
}

input[type="checkbox"][disabled]:checked + label:before {
  background-position: -96px 0;
}
```

--

#### 样式化 input[type=file]
```html
<a href="javascript:;" class="file">
     <input type="file" name="" id="">
</a>
```
```css
.file {
    position: relative;
    display: inline-block;
    background: url(../images/upload-file.png) no-repeat;
    height:88px;
    width:88px;
    background-size: 88px auto;
    overflow: hidden;
    text-decoration: none;
    line-height: 20px;
}
.file input {
    position: absolute;
    font-size: 100px;
    right: 0;
    top: 0;
    opacity: 0;
}
```

#### 样式化 radio
```html
<div class="radio-list">
                <div class="radio-label-container">
                    <div class="radio-container radio-on">
                        <input id="woman" name="sex" value="1" checked="checked" type="radio">
                    </div>
                    <label for="woman">女士</label>
                </div>
                <div class="radio-label-container">
                    <div class="radio-container">
                        <input id="man" name="sex" value="1" type="radio">
                    </div>
                    <label for="man">先生</label>
                </div>
            </div>
```

```css
/*radio 美化*/
.radio-label-container {
    float: left;
    cursor: pointer;
    margin-right: 15px;
}

.radio-label-container label {
    display: inline-block;
    margin-left: 2px;
    line-height: 14px;
}

.radio-container {
    width: 13px;
    height: 13px;
    float: left;
    cursor: pointer;
    text-align: center;
    background: url(../images/public/radio.png) no-repeat;
    margin-right: 2px;
    background-size: 13px 13px;
}

.radio-on {
    background: url(../images/public/radio-on.png) no-repeat;
    background-size: 13px 13px;
}

.radio-container input[type="radio"] {
    opacity: 0;
    cursor: pointer;
    -ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";
    filter: alpha(opacity=0);
}

/*radio 样式美化*/
```

```javascript
// radio 样式美化 -------------------------------------
(function () {
    var radioBeautify = function () {
        var radioName = $(this).children('input[type="radio"]').attr('name');
        $('input[type="radio"]').each(function (i, obj) {
            if ($(this).attr('name') == radioName) {
                $(this).removeAttr('checked')
                $(this).parents('.radio-container').removeClass('radio-on');
            }
        });
        $(this).addClass("radio-on");
        $(this).children('input[type="radio"]').attr("checked", "checked");
    }
    $('body').on('click', '.radio-container', radioBeautify);
})();
```
