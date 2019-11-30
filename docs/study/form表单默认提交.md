# Form表单默认提交行为
</br>
</br>
当form 表单中有type为submit的按钮时，会触发表单的默认提交行为。
</br>
</br>
若form表单有action，默认提交地址为action中的地址，并跳转至该页面。
</br>
</br>
若form表单action为空，默认提交地址为本页面，并刷新网页。
</br>
</br>
不需要为submit按钮添加点击事件，点击时会自动触发form表单的submit事件。
</br>
</br>
在input输入框内按回车键也会触发submit事件(如果有submit按钮)。
</br>
</br>
若不阻止form表单的默认提交行为，会自动刷新网页。
</br>
</br>
阻止表单默认行为只是阻止了submit事件触发时自动刷新网页。
</br>
</br>
vue中阻止表单默认提交行为：

`在form表单的submit事件后添加事件修饰符prevent`
```js
<form @submit="formSubmit">
```

常规阻止表单默认提交行为：
` e.preventDefault()`