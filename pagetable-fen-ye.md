# PageTable分页

## 概括：

**pageTable**内置了 **el-pagination**组件，可以使用 'page-table'设置分页。

```markup
<page-table
    :props="{currentPage:1,pageSize:20,itemCount:400}"
    :pageSizes="[20,40,60,80]"
>
</page-table>
```

其中 _props_属性中的值 'currentPage'为初始当前页数，'pageSize'为初始每页显示的条目数， 'itemCount'为总的条目数。  
_pageSizes_属性定义每页显示个数选择器的选项设置。

## 总结：

了解更多查看 [Element](http://element-cn.eleme.io/#/zh-CN/component/pagination#pagination-fen-ye)

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
| :--- | :--- | :--- | :--- | :--- |
| props | 设置分页结构 | object |  | { currentPage:1,pageSize:20,itemCount:} |
| pageSize | 定义每页显示个数选择器的选项设置 | Array |  | \[20,30,50,100\] |

