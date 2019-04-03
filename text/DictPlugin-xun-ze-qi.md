# DictPlugin组件  

## 概括  
**DictPlugin**设计一个选择器，通过 *dict* 属性来添加选择器中的选项，其属性值为Array，组件中使用 *item.itemCode*、 *item.itemName*分别定义 *key、value*和 *label*的值。*placeholder*定义占位符
```html
<dict :dict="option" v-model="value" placeholder="请选择">

</dict>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    return{
        value: '',
        option: [{itemCode:'选项1',itemName:'蛋糕'},
        {itemCode:'选项2',itemName:'鸡蛋'},
        {itemCode:'选项3',itemName:'牛奶'}],
    }
})
</script>
```  

### 多选功能
通过*multiple*的'true'或'false'属性值可以让选择栏中是否添加多个选项。
```html
<dict :dict="option" v-model="value" placeholder="请选择"
    multiple= true
>

</dict>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    return{
        value: '',
        option: [{itemCode:'选项1',itemName:'蛋糕'},
        {itemCode:'选项2',itemName:'鸡蛋'},
        {itemCode:'选项3',itemName:'牛奶'}],
    }
})
</script>
```

### 禁用分组下的所有选项
通过 *disabled*设置 'false'值可以禁用选择器。其默认值为'true'
```html
<dict :dict="option" v-model="value" placeholder="请选择" 
    disabled= true>
       
</dict>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    return{
        value: '',
        option: [{itemCode:'选项1',itemName:'蛋糕'},
        {itemCode:'选项2',itemName:'鸡蛋'},
        {itemCode:'选项3',itemName:'牛奶'}],
    }
})
</script>
```  
### 选中全部的选项  
*isFilter*属性可以通过设置'true'的属性值可以添加选中全部的选项  
```html
<dict :dict="option" v-model="value" placeholder="请选择"
    isFilter= true
>
    
</dict>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    return{
        value: '',
        option: [{itemCode:'选项1',itemName:'蛋糕'},
        {itemCode:'选项2',itemName:'鸡蛋'},
        {itemCode:'选项3',itemName:'牛奶'}],
    }
})
</script>
```  
## 总结
上述的属性是已经集成到组件，了解更多相关属性和用法请参考 [Element](http://element-cn.eleme.io/#/zh-CN/component/select)

**DictPlugin**属性

| 参数        | 说明             | 类型                      | 可选值 | 默认值 |
| ----------- | ---------------- | ------------------------- | ------ | ------ |
| multiple    | 是否添加多个选项 | boolean                   |        | false  |
| dict        | 添加选项的值       | Array                    | ||
| placeholder | 设置占位符       | 'String','Array','Number' |||
|disabled|禁用选型|Boolean||true|
|isFilter|选中全部选项|Boolean||true|