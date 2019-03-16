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
