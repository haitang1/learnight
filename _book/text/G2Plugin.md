# G2 图形组件

## 概括  
使用 **g2** 标签给图形设置一个容器，通过 *data* 属性为容器添加数据，*width*，*height* 分别定义容器的宽度和高度，*type* 为几何标识属性决定创建图表的类型，*position('x \* y')* 方法是将数值映射到图形上，其中 x , y 代表两个维度的变量，*color* 方法是将数值映射到图形的颜色上，*value* : string只接受一个数据类型，
*padding* 设置容器的边距

实例：
```html
<g2 :data="data"
    :height="staticsHeight"
    :width="700"
    :padding="[10,15,30,50]"
    position="X*Y"
    color="name"
    type="line"
    :handle="line"
    >
</g2>
```

## 使用方法  
使用 **G2** 创建好容器后可以使用 *handle* 属性绑定当前的容器为其进行自定义设置，*p*参数返回的值是刚开始容器初始值，*chart*参数可以在容器中绘制出新的图表  

```javascript
new Vue({
    return{
        line({chart,p}:{chart:G2Chart,p:any}){
            p.color('name').size('2').shape('smooth') //自定义图表样式
            chart.interval().position('x*y').color('name') //在容器中绘制出另一个图表
        }
    }
})
```

## 总结  
以上介绍的是 **G2** 组件中封装的属性和方法，有关其更多的属性和方法可以参考官方的API文档  

### Chart 图表相关属性  
| 参数      | 说明                                  | 类型         | 可选值 | 默认值 |
| --------- | ------------------------------------- | ------------ | ------ | ------ |
| container | 传入DOM的id或者直接传入容器的HTML对象 | string       |        |        |
| width     | 指定宽度，单位 'px'                   | string       |        |        |
| height    | 指定高度，单位 'px'                   | string       |        |        |
| padding   | 设置图表的内边距                      | array        |        |        |
| forceFit  | 图表宽度自适应                        | boolean      |        | false  |
| data      | 图标的数据源                          | abject,array |        |        |

### 图表的相关方法  
| 参数     | 说明                       | 类型   | 可选值                           | 默认值 |
| -------- | -------------------------- | ------ | -------------------------------- | ------ |
| position | 将数据映射到图形的相应位置 | string | position('x*y')                  |        |
| color    | 将数据值映射到图形的颜色上 | string | color(value),color(field,colors) |        |
| shape    | 将数据映射到图形的形状上   | string |                                  |        |
| size     | 将数值映射到图形的大小上   | string |                                  |        |
