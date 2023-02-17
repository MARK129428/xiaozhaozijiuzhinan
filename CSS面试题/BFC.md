## BFC

### 什么是BFC
块级格式化上下文,是Web页面的可视CSS渲染的一部分，是块级盒子布局过程的区域，也是浮动元素与其他元素交互的区域。

### 创建BFC的方式
- `display: table-cell`
- `display: flex`
- `display: inline-block`
- `overflow: hidden`
- `position: absolute`
- `position: fixed`

### BFC解决了什么问题

- float高度塌陷
- margin重叠
