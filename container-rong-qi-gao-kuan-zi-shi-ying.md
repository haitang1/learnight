# Container容器高度自适应

## 概括

**container**定义一个可以自适应父元素宽度和高度的容器，通过 _width_, _height_属性可以自定义容器的初始宽度和高度，是一个固定的值。_out-width_, _out-height_属性可以定义容器的外边的宽度和高度，并能够自适应父元素的高度和宽度。_scroll_属性值是一个 'boolean'可以通过"true" 或 "false" 分别定义样式_overflow_的 'auto' , 'hidden'值。

实例：

```markup
<container
    :height="100"
    :out-width="200"
    @onresize="resize"
    :scroll="false"
    >

</container>
```

其中_@onresize="resize"_方法为寻找父节点适应其高宽。  
_width_, _height_属性固定容器的大小，_out-width_, _out-height_属性定义容器外边距并自适应高宽，其值与容器大小成反比

## 总结

### 相关属性

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
| :--- | :--- | :--- | :--- | :--- |
| height | 固定容器的高度 | Number |  |  |
| width | 固定容器的宽度 | Number |  |  |
| out-height | 定义容器外边高度并自适应 | Number |  | 0 |
| out-width | 定义容器外边宽度并自适应 | Number |  | 0 |
| scroll | 定义 _overflow_属性值 | boolean |  | true |

### 相关方法

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
| :--- | :--- | :--- | :--- | :--- |
| @onresize | 寻找父节点适应其高宽 | Object | resize |  |
