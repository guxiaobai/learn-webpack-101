# webpack-dev-server

|本期版本|上期版本
|:---:|:---:
`Wed Jun  8 14:05:58 CST 2022` | -


v5|v4 | 备注
:---:|:---:|:---:
`static` | `contentBase`
`hot` | `hot` | 开启HMR, 即不要刷新页面
`-` | 	`hotOnly` | 即使HMR失效，也不要自动刷新浏览器

## Proxy

* [`http-proxy`](https://github.com/nodejitsu/node-http-proxy)
* [`http-proxy-middleware`](https://github.com/chimurai/http-proxy-middleware)
* [关于webpack-dev-server代理的哪些事儿](https://github.com/iuap-design/blog/issues/260)

## HotModuleReplacementPlugin

> Since webpack-dev-server v4, HMR is enabled by default. It automatically applies `webpack.HotModuleReplacementPlugin` which is required to enable HMR


```js
const webpack = require('webpack');

new webpack.HotModuleReplacementPlugin({
  // Options...
});
```


```js
if(module.hot) {
  // 如果 number 文件发生了变化执行后面的函数
  module.hot.accept('./number', ()=>{
    console.log('ss')
  })
}
```

## Ref

* [https://webpack.js.org/configuration/dev-server/](https://webpack.js.org/configuration/dev-server/)