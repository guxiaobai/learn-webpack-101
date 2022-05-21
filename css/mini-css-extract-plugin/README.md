# MiniCssExtractPlugin

|本期版本|上期版本
|:---:|:---:
`Sat May 21 09:31:41 CST 2022` |  -


```js
const isProductionMode = process.env.NODE_ENV === "production";

const MiniCssExtractPlugin = require('mini-css-extract-plugin');

module:{
  rules: [
    {
      test: /\.css$/,
      use: [
        isProductionMode ? MiniCssExtractPlugin.loader : "style-loader",
        "css-loader"
      ]
    }
  ]
},
plugins: [
  new MiniCssExtractPlugin({
    filename: isProductionMode ? "[name].[contenthash].css" : "[name].css",
  })
],
```


## Ref

* [https://webpack.js.org/plugins/mini-css-extract-plugin/](https://webpack.js.org/plugins/mini-css-extract-plugin/)