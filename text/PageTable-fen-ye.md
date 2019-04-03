# pageTable组件

## 概括：  
**pageTable**内置了 **el-pagination**组件，可以使用 'page-table'设置分页。其中有 *props* 、*pageSizes*属性， *props*属性值'currentPage'当前所在的页数、'pageSize'当前页码的总数、'itemCount'总的页数

```html
<page-table
    :props="page"
    :pageSizes="[20,40,60,80]"
    @goto="paging"
>
</page-table>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    return{
        currentPage:1,
        pageSize:20,
        itemCount:0,
        isLoad:false
    }
})

methods{
    paging(param:{currentPage:number,pageSize:number}){
      this.page.pageSize = param.pageSize;
      //this.trigger.query(param.currentPage);
    },
}
</script>
```
其中 *props*属性中的值 'currentPage'为初始当前页数，'pageSize'为初始每页显示的条目数， 'itemCount'为总的条目数。  
*pageSizes*属性定义每页显示个数选择器的选项设置。  
通过 *@goto*方法可以调节当前页出现的最大条目数，能够跳转到指定的页码中

## 总结：

了解更多查看 [Element](http://element-cn.eleme.io/#/zh-CN/component/pagination#pagination-fen-ye)

| 参数     | 说明                             | 类型   | 可选值 | 默认值                                  |
| -------- | -------------------------------- | ------ | ------ | --------------------------------------- |
| props    | 设置分页结构                     | object |        | { currentPage:1,pageSize:20,itemCount:} |
| pageSize | 定义每页显示个数选择器的选项设置 | Array  |        | [20,30,50,100]                          |
### 相关方法  
| 方法名称 | 说明                                           |
| -------- | ---------------------------------------------- |
| @goto    | 调节当前页出现的最大条目数，跳转到指定的页码中 |

