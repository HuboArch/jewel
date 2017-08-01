#### this小结

红宝书里对 this 的定义是，函数据以执行的环境对象

1. 函数参数中的 `this`

```javascript
let fruit = {
    name: 'apple',
    log (p) {
        console.log(p)
    }
}

let basket = {
    name: 'orange',
    putIn () {
        fruit.log(this.name) // this = basket
    }
}

basket.putIn() // 'orange'

```
