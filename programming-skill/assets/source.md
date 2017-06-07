- 获取函数参数

```JavaScript
let total = 30;
let msg = passthru `The total is ${total} (${total * 1.05} with tax)`;

function passthru (literals) {
    let result = '';
    let i = 0;

    while (i < literals.length) {
        result += literals[i++];
        if (i < arguments.length) {
            result += arguments[i];
        }
    }

    return result;
}

console.log(msg);  // 'The total is 30 (31.5 with tax)'
```
