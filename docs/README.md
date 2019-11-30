* * *
# [BFC](study/BFC.md)

> An awesome project.

This is my first project.

* * *
# [content的值](study/content值.md)

> An awesome project.

* * *
# 657567

> An awesome project.

# Vue 介绍

`v-for` 的用法

```html
<ul>
  <li v-for="i in 10">{{ i }}</li>
</ul>
``

<ul>
  <li v-for="i in 10">{{ i }}</li>
</ul>

# Vue 的基本用法

<!-- <div>hello {{ msg }}</div> -->

<!-- <script>
  new Vue({
    el: '#main',
    data: { msg: `v
    u
    e` }
  })
</script> -->

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
  <template>
    <div>Hello, {{ name }}!</div>
  </template>

  <script>
    module.exports = {
      data: function () {
        return { name: 'Vue' }
      }
    }
  </script>
</script>
