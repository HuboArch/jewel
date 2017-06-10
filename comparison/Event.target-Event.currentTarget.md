#### Event.target-Event.currentTarget

JS 的 Event 对象拥有两个属性，`Event.target` 和 `Event.currentTarget`. 这两个属性均是和事件对象相关的DOM对象引用，前者引用的是触发事件处理程序的元素，后者引用的则是被绑定了事件处理程序的元素

```html
<!-- HTML -->
<div class="outer">
    <div class="inner"></div>
</div>
```

```css
/* CSS */
.outer {
    width: 100px;
    height: 100px;
    padding: 20px;
    border: 1px solid blue;
}

.inner {
    width: 50px;
    height: 50px;
    background-color: red;
}
```

```JavaScript
let outer = document.querySelector('.outer')
let inner = document.querySelector('.inner')

outer.addEventListener('click', function (e) {
    console.log('target: ' + e.target + ' ' + 'currentTarget: ' + e.currentTarget)
}, false)
```
![img](https://github.com/hugeloveu/jewel/blob/master/comparison/assets/target-currentTarget.png)
