# 组件的使用方法

- 可以使用is属性来关联一下子组件的显示。

如下代码：
```
  table
    tbody
        tr is=row
```
- 采用is属性进行标签显示的合规限制；
如下场景：
ul
    li

select 
    option

ol
    li
等等....


# 注意， 在子组件里定义data属性时，不是一个对象， 而是一个函数。
Vue.template('row',{
    data: function (){
        return 'this is a data';
    },//这里必须要是一个函数，而不是一个对象； 
    template: 'afasdfasdf'
})