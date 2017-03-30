# pull-loading
移动设备任意容器实现下拉刷新，原生JavaScript实现。

# 使用示意
① 引入 JS 
```JavaScript
<script src="pull-loading.js"></script>
```

② 引入 CSS
```HTML
<link rel="stylesheet" href="pull-loading.css">
```

③ 绑定
```JavaScript
new PullLoading(document.getElementById('container'));
```

# 语法
```JavaScript
new PullLoading(ele, option);
```

其中：
* `ele`表示需要拖动的元素；
* `option`为可选参数，包括：
  * `scrollElem`表示产生滚动条的容器，默认为`body`；
  * `frontText`下拉生效前的提示语，默认为“下拉加载更多”；
  * `loadingText`正在执行回调时的提示语，默认为“正在加载中...”；
  * `endText`释放后生效的提示语，默认为“释放立即加载”；
  * `bgcolor`下拉刷新容器背景颜色，默认为`#eee`；
  * `icon`正在执行回调时的 loading 图标，采用 svg 实现，可选值：`circle`、`rect`、`rectAlpha`，默认为`rectAlpha`；
  * `callback`触发执行的回调函数，函数第一个参数为`done`函数，回调执行完毕时调用`done()`将下拉框回复到初始状态，默认值为`setTimeout`两秒后执行`done()`；
  * `timeout`回调超时值，毫秒，当超时未执行`done()`函数时自动执行，建议设置，设为`0`时表示不作超时处理，默认为`0`；
  * `timeoutCallback`当回调超时时触发的回调函数，一般用来做一些错误提示处理。

# 在线预览
点击查看[在线demo](https://gisonyeung.github.io/pull-loading/demo/example.html)
