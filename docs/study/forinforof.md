# for in 和 for of

<br>

## for in
    for in 遍历数组获取的是数组的下标以及数组原型方法及属性

    for in 遍历对象获取的是对象的key，也可以获取对象原型上的方法和属性，可以通过``object.hasOwnPropery()``判断循环是否属于对象本身

## for of
    for of 遍历数组获取的是数组的每一项
    for of 无法遍历不是类数组的对象

>   一般循环数组使用for of
>   循环对象使用for in



