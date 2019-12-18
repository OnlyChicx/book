# vue移动端适配

*（适用vue/cli3）*

新建项目，并在项目中新建vue.config.js

安装`postcss-pxtorem`，对px进行转换

> yarn add postcss-pxtorem -D 或 npm install postcss-pxtorem -D

将如下代码写入文件

```js
module.exports = {
  lintOnSave: true,
  css: {
      loaderOptions: {
          postcss: {
              plugins: [
                  require('postcss-pxtorem')({
                      rootValue: 75, // 换算的基数
                      selectorBlackList: ['weui','mu'], // 忽略转换正则匹配项
                      propList: ['*'],
                  }),
              ]
          }
      }
  },
}
```

还需要安装`amfe-flexible`，使屏幕变化时通过js控制页面html字体的大小

安装完成后直接在`main.js`中引用即可