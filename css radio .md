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
