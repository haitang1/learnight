# Layout组件

## 概括  
**layout** 设计一个拥有左栏、上栏的整体布局，左栏为树形控件,上栏为查询的表单。其中 *top*、*left*属性分别定义上栏高度和下栏的宽度，在容器标签中可以通过 *slot*属性值 'top'、'left'来确定容器上栏和下栏的位置。  

```html
<layout
    :top='70'
    :left='200'
>
    <div slot="left">
        左栏宽为200px的容器
    </div>
    <div slot="top">
        上栏高为70px的容器
    </div>
</layout>
```
### 设置各部分的外边距  
*right*属性定义左栏的右外边距默认值为'4'，*leftTop*属性定义左栏的上外边距，*topLeft*属性定义上栏左外边距，默认为外边距与左栏宽度保持一致
```html
<layout
    :left='200' :top='70' 
    :right="10"     <!-- 左栏右外边距为10px -->
    :leftTop="50"   <!-- 左栏上外边距为50px -->
    :topLeft="300"  <!-- 上栏左外边距为300px -->
>
    <div slot="left">
        左栏宽为200px的容器
    </div>
    <div slot="top">
        上栏高为70px的容器
    </div>
</layout>
```  
## 总结  
**layout**组件统一了平台中各分支的整体页面布局，更加便捷的添加新的内容  
| 参数    | 说明         | 类型   | 可选值         | 默认值 |
| ------- | ------------ | ------ | -------------- | ------ |
| top     | 上栏的高度   | Numble |                | 0      |
| left    | 左栏的高度   | Numble |                | 0      |
| slot    | 确定位置     | String | 'left','right' ||
| right   | 左栏右外边距 | Numble |                | 4      |
| leftTop | 左栏上外边距 | Numble |                | 0      |
| topLeft | 上栏左边距   | Numble |                | null   |