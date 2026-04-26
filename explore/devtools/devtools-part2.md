# DevTools Part 2

## 1. What was the bug?

The bug was that the input values were being read as strings, not numbers. So when JavaScript used the `+` operator, it joined the values like text instead of adding them as numbers. For example, 2 and 3 became 23 instead of 5.

## 2. How would you fix it?

I would fix it by converting `num1` and `num2` into numbers before adding them.

```js
function calculateSum(num1, num2) {
    let result = Number(num1) + Number(num2);
    return result;
}
```

This makes JavaScript add the values as numbers instead of joining them as strings.