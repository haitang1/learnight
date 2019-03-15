# MenuPlugin组件
## 概括：

**MenuPlugin**为导航菜单，内置有 **el-submenu** 组件，可以使用 *item*属性直接定义二级菜单。*item*中的属性 值'label','children'分别定义导航栏的名字和二级菜单

```html
<menu-recursion
    :item="{label='工作台',children=['选项一','选项二','选项三']}"
>
</menu-recursion>
```

## 总结：

了解更多请查看 [Element](http://element-cn.eleme.io/#/zh-CN/component/menu)

### MenuPlugin相关属性
| 参数 | 说明                       | 类型   | 可选值 | 默认值 |
| ---- | -------------------------- | ------ | ------ | ------ |
| item | 定义导航栏的名字和二级菜单 | object | | |
