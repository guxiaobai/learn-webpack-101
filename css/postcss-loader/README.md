# postcss-loader

|本期版本|上期版本
|:---:|:---:
`Sat May 21 09:34:58 CST 2022` | -


* `postcss-loader` 执行顺序必须保证在 `css-loader` 之前，建议还是放在 `less` 或者 `sass` 等预处理器之后更好。
* 即 `loader` 顺序： `less-loader` -> `postcss-loader` -> `css-loader` -> `style-loader` 或者 `MiniCssExtractPlugin.loader`

## Ref

* [https://webpack.js.org/loaders/postcss-loader/](https://webpack.js.org/loaders/postcss-loader/)
* [https://time.geekbang.org/course/detail/100028901-99020](https://time.geekbang.org/course/detail/100028901-99020)