# Vue中如何添加样式：

- 采用在控件上写如下代码表达式：
```
    :class = "{actived: isActived}"
```
然后通过修改isActived来调整是否显示actived的样式表来达到目的； 

- 采用如下代码表达式：
```
    :class = "[actived]"
```
中括号里面的是一个JS表达式变量， 要通过调整actived的字符串的字面值来达到显示的目的；

# Vue.set('对象名‘， key, value)

# vm.$set('对象名’， key, value)