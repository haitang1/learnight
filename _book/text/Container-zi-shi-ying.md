# Container组件

## 概括 
**container**定义一个可以自适应父元素宽度和高度的容器，通过 *width*, *height*属性固定容器的长度和宽度。*out-width*, *out-height*属性定义容器与浏览器边框的距离。*scroll*属性值是一个 'boolean'可以通过"true" 或 "false" 分别定义样式*overflow*的 'auto' , 'hidden'值。

实例：
```html
<container
    :height="100"
    :out-width="200"
    @onresize="resize"
    :scroll="false"
    >

</container>
```
其中*@onresize="resize"*方法为寻找父节点适应其高宽。  
*width*, *height*属性固定容器的大小，*out-width*, *out-height*属性定义容器分别与浏览器窗口右边和下边的距离
## 总结

### 相关属性
| 参数       | 说明                     | 类型    | 可选值 | 默认值 |
| ---------- | ------------------------ | ------- | ------ | ------ |
| height     | 固定容器的高度           | Number  |        |        |
| width      | 固定容器的宽度           | Number  |        |        |
| out-height | 定义容器外边高度并自适应 | Number  |        | 0      |
| out-width  | 定义容器外边宽度并自适应 | Number  |        | 0      |
| scroll     | 定义 *overflow*属性值    | boolean |        | true   |
### 相关方法
| 参数      | 说明                 | 类型   | 可选值 | 默认值 |
| --------- | -------------------- | ------ | ------ | ------ |
| @onresize | 寻找父节点适应其高宽 | Object | resize |        |