# 学习了v-model,v-for,v-on三个命令：

- v-model 为Vue里面可以双向绑定的变量定义指令；在标签上定义为：v-model = "content" ，其中content表示一个双向绑定的变量。注意这里不需要用双层大括号；
在Vue里面就是data里面的一个变量即可。 

- v-for 表示一个for循环的指令；

- v-on 表示绑定一个页面控件事件的指令 如，单击事件绑定为； v-on:click="functaoinName" 即可、
*注: v-on:click可以写成@click 表示在当前控件中添加click事件*

今天 完成到这里， 明天继续...

jquery里面实现一个类的继承的写法：
先定义一个常用的类函数
function Page(){

}

$.extend(Page.prototype,{
    init: function(){
        this.bindleEvents();
    },
    bindleEvents:function(){
        var btn = $("#btn”);
        btn.on('click', $.proxy(this.handleBtnClick, this))
    },
    bandleBtnClick: function(){

        var inputObj = $("inputValue");
        var ulEm = $("$ulEm");
        ulEm.append('<li>'+ inputObj.val() +'</li>')
        inputObj.val('')
    }
})

var _page = new Page();
_page.init();


# 第2-4课

学习了什么时MVVM开发模式； 
M 表示model数据层
v 表示view表现层
vm 表示Vue里面的数据操作；

这种开发模式， 简化了页面dom的操作， 更多的时间在处理数据业务； 

# 如何创建一个页面的全局组件
Vuec.component(组件的名字， {组件的内容})
如下：
Vue.component("UlItem",{
    template:"<li>UlItem one</li>"
}
)
*注： 在定义组件的名称时， 依据驼峰命名法则， 在使用时用-连接，*
如下：
UlItem ->   ul-item
TodoItem ->  todo-item

定义组件后， 需要将数据传递给相应组件， 可以采用指令，v-bind来实现
v-bind 动态地绑定一个或多个特性，或一个组件 prop 到表达式

*注： v-bind可以简写成为:content*
如： v-bind:content="item"  表示将item的值绑定给content这个变量中，在组里面采用props里面的数组奕量content接收
可简写为 :content = "item" 即可。

# $watch函数
 用来监听vm里数据的变化；