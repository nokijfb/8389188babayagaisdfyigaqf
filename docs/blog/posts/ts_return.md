---
date: 2023-04-25
categories:
  - Devlog
tags:
  - typescript
  - learning
---

# `return` Statement

The `return` statement is essential in function design. This article will clarify the purpose of `return` and its importance.

<!-- more -->

#### What is `return`?

The `return` statement is used in functions to specify the value that should be returned to the calling context. It effectively ends the function's execution and sends a value back.

#### Why is `return` Important?

1. **Data Handling**: Functions without `return` cannot provide results to the rest of the program.
2. **Type Consistency**: Using `return` ensures that the function provides a value that aligns with the expected data type, especially in languages with type checking.
3. **Clarity**: Using `return` makes it clear that the function is meant to produce and deliver a value.
4. **Reduced Ambiguity**: Without an explicit `return`, it may not be clear how values are generated and returned.

#### Example of `return` in TypeScript

Here’s an example demonstrating the use of `return` in a TypeScript function that sums two numbers:

```typescript linenums="1"
function add(a: number, b: number): number {
    return a + b;  // Returns the sum
}

const result = add(3, 4);
console.log(`The sum is: ${result}`);  // Prints 7
```

In this example, the `add` function returns the result of adding two numbers, with the return type explicitly defined as `number`.

#### Using `return` vs. Not Using `return`

##### 1. Using `return`

When `return` is explicitly used, the output of the function is clear. The reader understands that the function is intended to return a value.

```typescript linenums="1"
function add(a: number, b: number): number {
    return a + b;  // Returns the sum
}
```

This ensures that the result is returned for further use.

##### 2. Not Using `return`

If `return` is omitted, the last evaluated expression is returned implicitly, which can lead to confusion.

```typescript linenums="1"
function add(a: number, b: number): number {
    a + b;  // Implicitly returns the sum
}

const result = add(3, 4);
console.log(`The sum is: ${result}`);  // Prints 7
```

While the output remains the same, the lack of an explicit return statement can make the code less clear.

#### Why is Using `return` Recommended?

1. **Purpose Clarity**: The function's goal is evident.
2. **Reusability**: Functions using `return` can be reused across the program.
3. **Execution Control**: Execution stops upon reaching the `return`, preventing unintended behavior.
4. **Type Safety**: TypeScript ensures that the returned value matches the declared return type.

---
In conclusion, it is beneficial to use `return` in TypeScript functions designed to process data. This practice improves code clarity, promotes reuse, and provides better control over function outputs. Understanding how to effectively use `return` can lead to more efficient and maintainable code.
