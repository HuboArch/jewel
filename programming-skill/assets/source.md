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

**思路分析**：msg是一个标签模板，函数调用的一种形式。其返回值就是 passthru 函数处理模板字符串后的返回值。passthru 函数的第一个参数(即literals)是一个数组，成员是模板字符串中没有被变量替换的部分 `[ 'The total is ', ' (', ' width tax)' ]`, passthru 函数的其他参数都是模板字符串中各个变量被替换后的值。由于数组参数的`length`始终是大于模板字符串中变量的个数的，所以 passthru 函数通过 `while` 遍历函数参数的方式实现了对模板字符串的拼接。**这里对函数参数的遍历方式值得学习**。
