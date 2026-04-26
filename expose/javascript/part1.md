# Part 1 - JavaScript Scope

## 1. What is printed by line 9? If the code returns an error, explain why.

Line 9 prints:

values added: 20

At first, `result` is set to 0 inside the if statement. Then it gets changed to `num1 + num2`, which is 10 + 10. So the value printed is 20.

## 2. What is printed by line 13? If the code returns an error, explain why.

Line 13 prints:

final result: 20

This works because `var` uses function scope. Even though `result` was made inside the if block, it can still be used later in the same function.

## 3. Why should you not use var? Explain why.

We should not use `var` when possible because it can be confusing. A variable made with `var` can still be used outside of the block where it was created, as long as it is inside the same function. This can make bugs harder to find. `let` and `const` are better because they stay inside the block where they are declared.

## 4. What is printed by line 9? If the code returns an error, explain why.

Line 9 prints:

values added: 20

This works because line 9 is still inside the same if block where `result` was declared. Since `result` is changed to 10 + 10 before the console.log, it prints 20.

## 5. What is printed by line 13? If the code returns an error, explain why.

Line 13 gives an error.

This is because `let` has block scope. `result` only exists inside the if block where it was declared. Line 13 is outside that block, so JavaScript cannot find `result`.

## 6. What is printed by line 9? If the code returns an error, explain why.

Line 9 does not print anything because the code gets an error before that.

The error happens at line 7 because the code tries to change `result`. Since `result` was declared with `const`, it cannot be reassigned after the first value is set.

## 7. What is printed by line 13? If the code returns an error, explain why.

Line 13 also does not print anything because the code already stopped from the error at line 7.

Also, `const` has block scope like `let`, so even if there was no reassignment error, `result` would still not be available outside the if block.