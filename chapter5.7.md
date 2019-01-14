# CSS浏览器前缀


## 浏览器样式前缀

为了让CSS3样式兼容，需要将某些样式加上浏览器前缀：

-ms- 兼容IE浏览器

-moz- 兼容firefox

-o- 兼容opera

-webkit- 兼容chrome 和 safari

比如：

```

div
{    
    -ms-transform: rotate(30deg);        
    -webkit-transform: rotate(30deg);    
    -o-transform: rotate(30deg);        
    -moz-transform: rotate(30deg);    
    transform: rotate(30deg);
}
```


## 自动添加浏览器前缀
目前的状况是，有些CSS3属性需要加前缀，有些不需要加，有些只需要加一部分，这些加前缀的工作可以交给插件来完成，比如安装： autoprefixer

Sublime text 中安装 autoprefixer 执行 preferences/key Bindings-Users 设置快捷键 { "keys": ["ctrl+alt+x"], "command": "autoprefixer" } 通过此工具可以按照最新的前缀使用情况给样式自动加前缀。