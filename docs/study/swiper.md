##Swiper


###Swiper的安装使用

  官网下载对应的css和js，将文件引入页面
  官网地址：`https://3.swiper.com.cn/download/index.html`

  也可使用npm包管理器下载
  npm命令：`npm install swiper`

  引入文件后在js中获取swiper实例对象：
  ```js
  var mySwiper = new Swiper('参数一','参数二')
  //参数一为页面中seiper的选择器
  //参数二为需要传入的swiper的配置对象
  ```

###Swiper的配置项
  
</br>

**分页器  Pagination**

    在参数二中传入Pagination对象

```js
pagination: {
  el: '.swiper-pagination',//分页器的选择器
  type: 'custom',//分页器自定义开启
  //分页器自定义设置
  renderCustom: function(swiper, current, total) {
    var customPaginationHtml = "";
    for (var i = 0; i < total; i++) {
      //判断哪个分页器此刻应该被激活 
      if (i == (current - 1)) {
        customPaginationHtml += '<span class="swiper-pagination-customs swiper-pagination-customs-active"></span>';
      } else {
        customPaginationHtml += '<span class="swiper-pagination-customs"></span>';
      }
    }
    return customPaginationHtml;
  }
}
```
    分页器可以放在轮播图之外，注意改写样式时层级选择器的改变

</br>

**Swiper循环----loop**

    在配置项中填写配置参数    loop:true

**Swiper自动播放----autoplay**

    在配置项中填写配置参数    autoplay:true/false   开启/关闭

```js
delay: 3000ms  //设置自动切换时间，默认3000
```
```html
<div class="swiper-slide" data-swiper-autoplay="2000">
  //也可以在单独的slide设置停留时间
```

`注意：`在不为autoplay设置其他属性时，autoplay的值为true或false，若要设置其他属性，autoplay的值为一个配置对象