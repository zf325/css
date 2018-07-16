# 伪类选择器

## 1. 常见的四种选择器
:link :visted :hover :active

伪类能保证以上的四种选择器正常有效的效果渲染，选择器的书写应当按照上述顺序：LVHA。
通常配合 a 标签使用。

:link       未访问的连接。

:visted     已访问连接，浏览器会查询历史浏览记录。当将该页面的浏览记录全部删除，该伪类才不会实现。

:hover      鼠标移动元素上。

:active     表示已经选择的元素

```html
<div class = "box">
        <a href = "http://www.baidu.com/" target="_blank">点我一下试试</a>
</div>
<style>

    .box a:link{
        color:red;
    }
    .box a:visited{
        color:blueviolet;
    }
    .box a:hover{
        color:blanchedalmond;
    }
    .box a:active{
        color:chartreuse;
    }
</style>

```
1. :active  会被其他伪类覆盖，优先级需要最高
2. :visted 会覆盖 :hover


## 2. :checked
1. :checked 伪元素选择器，针对Input type = "checkbox|radio",select 的 option(选定) 有效。

```html
<input type="checkbox" checked/>
<input type="radio"  checked/>
<select>
    <option checked> hahah</option>
    <option>eeee</option>
</select>
<style>

:checked{
    width:50px;
    height:50px;
    color:red;
}
</style>
```

## 3. :default [css3]

1. :defalut 只能用作表单元素，针对 button,checkbox,radio 有效

    表示选择默认状态下的表单元素

```html
<input type="checkbox"  checked/>
<input type="radio" checked/>
<input type="checkbox"  />
<input type="radio"  />
<button >点我点我</button>
<button checked>click me</button>
<style>

:default{
    width:50px;
    height:50px;
    color:red;
}
</style>
```



<!-- ## 2. 伪元素（装饰器）
- ::after     [ css3 引入]

已选中元素的最后一个元素
通常用来配合行内元素的 content ,对content 进行装饰。
```html
<body>

    <div >
       <span class = "ribbon">点我一下试试 </span>
    </div>
    
</body>
<style>

    .ribbon::after{
        content:" please,come on!";
        color:"green";
    }

</style>
``` -->