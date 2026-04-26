# Part 2 - JavaScript Practice

## 1. What will happen at line 12 and why?

Line 12 prints:

3

This happens because `i` was declared with `var`, so it has function scope. After the loop finishes, `i` is still available, and its final value is 3.

## 2. What will happen at line 13 and why?

Line 13 prints:

150

This happens because `discountedPrice` was declared with `var` inside the loop. Since `var` has function scope, it can still be used after the loop. The last discounted price is 300 * 0.5, which is 150.

## 3. What will happen at line 14 and why?

Line 14 prints:

150

`finalPrice` was declared with `var` near the top of the function, so it is available after the loop. During the last loop, the final price becomes 150.

## 4. What will this function return?

The function returns:

[50, 100, 150]

Each price gets multiplied by `1 - discount`. Since the discount is 0.5, each price is cut in half and pushed into the `discounted` array.

## 5. What will happen at line 12 and why?

Line 12 gives an error.

This happens because `i` was declared with `let` inside the for loop. `let` has block scope, so `i` only exists inside the loop. Line 12 is outside the loop, so JavaScript cannot find `i`.

## 6. What will happen at line 13 and why?

Line 13 gives an error.

`discountedPrice` was declared with `let` inside the for loop, so it only exists inside that loop block. Since line 13 is outside the loop, JavaScript cannot access it.

## 7. What will happen at line 14 and why?

Line 14 prints:

150

This works because `finalPrice` was declared outside the loop, inside the function. So even though the loop is finished, `finalPrice` can still be used. Its final value is 150.

## 8. What will this function return?

The function returns:

[50, 100, 150]

There is no error here. `discounted` is declared outside the loop, so the function can return it after all the discounted prices are added.

## 9. What will happen at line 11 and why?

Line 11 gives an error.

This happens because `i` was declared with `let` inside the for loop. It only exists inside the loop, so it cannot be used outside the loop.

## 10. What will happen at line 12 and why?

Line 12 prints:

3

This works because `length` was declared near the top of the function, not inside the loop. It stores `prices.length`, which is 3.

## 11. What will this function return?

The function returns:

[50, 100, 150]

The function creates an empty array called `discounted`, loops through the prices, calculates each discounted price, pushes it into the array, and then returns the array.

## 12. Given the object, write the notation.

A. Accessing the name property:

student.name

B. Accessing the Grad Year property:

student['Grad Year']

C. Calling the greeting function:

student.greeting()

D. Accessing the name property inside Favorite Teacher:

student['Favorite Teacher'].name

E. Accessing index zero in courseLoad:

student.courseLoad[0]

## 13. Arithmetic

A. `'3' + 2`

Output:

'32'

Because `+` with a string does string concatenation.

B. `'3' - 2`

Output:

1

Because `-` converts the string `'3'` into the number 3.

C. `3 + null`

Output:

3

Because `null` becomes 0 in this arithmetic expression.

D. `'3' + null`

Output:

'3null'

Because `+` with a string turns `null` into a string and combines them.

E. `true + 3`

Output:

4

Because `true` becomes 1.

F. `false + null`

Output:

0

Because `false` becomes 0 and `null` also becomes 0.

G. `'3' + undefined`

Output:

'3undefined'

Because `+` with a string turns `undefined` into a string.

H. `'3' - undefined`

Output:

NaN

Because `undefined` cannot be converted into a useful number for subtraction.

## 14. Comparison

A. `'2' > 1`

Output:

true

The string `'2'` gets converted to the number 2, and 2 is greater than 1.

B. `'2' < '12'`

Output:

false

Both values are strings, so JavaScript compares them like text. Since `'2'` comes after `'1'`, this is false.

C. `2 == '2'`

Output:

true

`==` allows type conversion, so `'2'` becomes 2.

D. `2 === '2'`

Output:

false

`===` checks both value and type. One is a number and one is a string.

E. `true == 2`

Output:

false

With `==`, true becomes 1. Since 1 is not equal to 2, the result is false.

F. `true === Boolean(2)`

Output:

true

`Boolean(2)` becomes true, so this compares true with true using strict equality.

## 15. Explain the difference between == and ===.

`==` compares two values but allows JavaScript to convert the types first. This can sometimes give surprising results. `===` is stricter because it checks both the value and the type. In general, `===` is safer because it does not do automatic type conversion.

## 17. What will be the result?

The result will be:

[2, 4, 6]

The function `modifyArray` loops through `[1, 2, 3]`. For each number, it calls the callback function `doSomething`. Since `doSomething` returns `num * 2`, each number gets doubled and added to the new array.

## 19. What is the output of the code?

The output is:

1
4
3
2

First, it prints 1. Then the two `setTimeout` calls are scheduled. After that, it immediately prints 4. The timeout with 0 milliseconds prints 3 next, and the timeout with 1000 milliseconds prints 2 last.