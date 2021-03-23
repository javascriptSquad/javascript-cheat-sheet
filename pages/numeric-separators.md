# Numeric separators

- Author: [0x4bd0](https://github.com/0x4bd0)

Large numeric literals are difficult for the human eye to parse quickly, especially when there are lots of repeating digits.

## Information

Reference Material:

- [V8](https://v8.dev/features/numeric-separators)

## Examples and Explanation

When working with big numbers in javascript, you can use _ to visually seperate the digits.

```js
let firstNumber = 1_000_000_000_000;
let secondNumber = 1000000000000

console.log(firstNumber === secondNumber);  //  true
```


