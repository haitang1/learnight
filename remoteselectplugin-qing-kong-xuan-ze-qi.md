# RemoteSelectPlugin清空选择器

## 概括：

选择器中间包含清空按钮，可将其清空为原始状态。组件中集成了异步函数和后台进行数据交互，_params_属性调用后台接口

```markup
<remote-search 
    :multiple=false //是否多选
    ：disabled=false //是否禁用
    :placeholder= "请选择" //占位符
    : params="{}"
>
</remote-search>
```

## 总结

| 参数 | 说明 | 类型 | 可选值 | 默认值 |
| :--- | :--- | :--- | :--- | :--- |
| multiple | 是否添加多个选项 | boolean |  | false |
| disabled | 是否禁用选项 | Boolean |  | false |
| params | 添加选项的值 | object |  |  |
| placeholder | 设置占位符 | 'String','Array','Number' |  |  |

