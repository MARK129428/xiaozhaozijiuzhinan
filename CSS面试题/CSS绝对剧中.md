## CSS如何实现绝对剧中

### 定宽高
- 绝对定位  + 负margin值
```css
.parent {
  width: 100px;
  height: 100px;
  position: relative;
}
.box {
  position: absolute;
  width: 50px;
  height: 50px;
  position: absolute;
  left: 50%;
  top: 50%;
  margin-left: -50px;
  margin-top: -50px;
}
```
- 绝对定位  + margin auto
```css
.parent {
  width: 100px;
  height: 100px;
  position: relative;
}
.box {
  position: absolute;
  width: 50px;
  height: 50px;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: auto;
}
```

### 不定宽高
- 绝对定位  + transform
```css
.parent {
  width: 100px;
  height: 100px;
  position: relative;
}
.box {
  position: absolute;
  width: 50px;
  height: 50px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
```
- tabel-cell
```css
.parent {
  width: 100px;
  height: 100px;
  display: table-cell;
  vertical-align: middle;
  text-align: center;
}
.box {
  display: inline-block;
}
```
- flex布局
```css
.parent {
  display: flex;
  jcc
  aic
}
```