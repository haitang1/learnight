# DictPlugin组件  

## 概括  
**DictPlugin**设计一个选择器，通过 *dict* 属性来添加选择器中的选项，其属性值为Array，组件中使用 *item.itemCode*、 *item.itemName*分别定义 *key、value*和 *label*的值。*placeholder*定义占位符
```html
<dict
    :dict="[
        {itemCode:'选项1',itemName:'蛋糕'},
        {itemCode:'选项2',itemName:'鸡蛋'},
        {itemCode:'选项3',itemName:'牛奶'}
    ]"
    placeholder="请选择"
>
</dict> 
```  

### 多选功能
通过*multiple*的'true'或'false'属性值可以让选择栏中是否添加多个选项。
```html
<dict
    :dict="[
        {itemCode:'选项1',itemName:'蛋糕'},
        {itemCode:'选项2',itemName:'鸡蛋'},
        {itemCode:'选项3',itemName:'牛奶'}
    ]"
    :multiple="true"
    >
</dict>
```
## 总结
上述的属性是已经集成到组件，了解更多相关属性和用法请参考 [Element](http://element-cn.eleme.io/#/zh-CN/component/select)

**DictPlugin**属性

| 参数        | 说明             | 类型                      | 可选值 | 默认值 |
| ----------- | ---------------- | ------------------------- | ------ | ------ |
| multiple    | 是否添加多个选项 | boolean                   |        | false  |
| dict        | 添加选项的值       | Array                    | ||
| placeholder | 设置占位符       | 'String','Array','Number' |||