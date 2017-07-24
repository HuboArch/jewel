#### this小结

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
