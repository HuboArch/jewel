#### this小结

`this`是 javascript 中的一个关键字，它调用的方式多种多样，但本质上 this 总是指向函数据以执行的环境对象.

1. 作为函数参数

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
