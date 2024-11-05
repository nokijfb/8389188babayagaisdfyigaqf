---
date: 2023-05-21
categories:
  - Devlog
tags:
  - python
  - go
  - basic-math
  - learning
---

# lilbit-Modulus
#### with code examples

At its core, the modulus operation helps you find the remainder when you divide one number by another. It’s often denoted using the percentage sign `%`. For example, when you divide 10 by 3, the division gives you 3 with a remainder of 1.<!-- more --> This operation is written as:

10 mod 3 = 1

This means that when you divide 10 by 3, there is 1 left over after you’ve distributed the apples evenly.

### A Deep Dive into Modulus

To truly understand the modulus operation, let’s break it down step by step and use various analogies and examples.

#### Basic Concept of Division

To fully grasp modulus, let's start with the concept of division. When we divide two numbers, we are trying to see how many times the second number (the divisor) can fit into the first number (the dividend).

- **Example**: If you have 10 apples and want to divide them among 3 friends:
  - Each friend can get 3 apples (3 × 3 = 9), which means there will be 1 apple left over. So, we say that 10 divided by 3 equals 3 with a remainder of 1.

When you divide two numbers, you are essentially trying to find out how many times the divisor can fit into the dividend without exceeding it. For example:

- **10 divided by 3** gives you:
  - How many times can 3 fit into 10? 
  - The answer is 3 times (because 3 x 3 = 9).
  - What is left over? 10 - 9 = 1.
  
So, we can say that:

10 ÷ 3 = 3 (the quotient) with a remainder of 1 (the modulus)

Thus:

`10 mod 3 = 1`

### Analogies to Understand Modulus

1. **Sharing Cookies**: Imagine you have 10 cookies and want to share them with 3 friends. You give each friend 3 cookies, which uses up 9 cookies in total. You have 1 cookie left. Here, `10 mod 3 = 1` because that’s the cookie that couldn’t be shared.

2. **Sharing Candies**: Suppose you have 14 candies and you want to share them with 4 friends. Each friend gets 3 candies (which totals to 12 candies). You would have 2 candies left over. This can be expressed as:

`14 mod 4 = 2`

3. **Classroom Seats**: Picture a classroom with 20 students and 6 desks. If you arrange the students at the desks, you can fill 3 desks with 6 students each (which is 18 students total), leaving 2 students without desks. Thus, `20 mod 6 = 2`.
4. **Classroom Arrangement**: Imagine a classroom with 25 students and only 6 desks. You can fill 4 desks with 6 students each (24 students total), leaving 1 student without a desk. This means:

`25 mod 6 = 1`

5. **Boxes of Toys**: If you have 25 toys and want to pack them into boxes that can each hold 8 toys, you can fill 3 boxes (24 toys total), leaving you with 1 toy. This means (`25 mod 8 = 1`).

6. **Packing Boxes**: If you have 30 toys and each box can hold 8 toys, you can fill 3 boxes with 8 toys (which totals 24 toys). You will have 6 toys left over. Therefore:

`30 mod 8 = 6`

### Mathematical Properties of Modulus

Understanding some properties of the modulus operation can help solidify your grasp:

- **Property 1**: The result of modulus is always less than the divisor. For example, `10 mod 3 = 1`, and 1 is less than 3.
  
- **Property 2**: If the dividend is smaller than the divisor, the modulus is the dividend itself. For example, `2 mod 5 = 2`.
  
- **Property 3**: When a number is divided by itself, the modulus is 0. For instance, `5 mod 5 = 0` because there is no remainder.


### Applications of Modulus in Real Life

1. **Checking Even and Odd Numbers**: Modulus is commonly used to determine if a number is even or odd. A number is even if `number mod 2 = 0` (divisible by 2) and odd if it’s not.

   - **Example**: 
     - For 8: `8 mod 2 = 0` (even)
     - For 9: `9 mod 2 = 1` (odd)

2. **Round-Robin Scheduling**: In games or tournaments, modulus can help to alternate players or teams. If you have 4 teams and 10 rounds, you can find out which team plays in each round using modulus.

3. **Time Calculation**: Modulus is helpful for calculating time on a 12-hour clock. For instance, if it’s currently 10 AM and you add 5 hours, you can use modulus to determine the new time:

`(10 + 5) mod 12 = 3 PM`

### Modulus in Programming

Now, let's explore how modulus is used in programming languages like Python and Go. We'll provide multiple examples for clarity.

#### in-Python Examples

1. **Checking for Even or Odd**:

```python linenums="1"
# Check if a number is even or odd
number = 7

if number % 2 == 0:
    print(f"{number} is Even")
else:
    print(f"{number} is Odd")
```

**Explanation**: 
- Here, we check if 7 is even or odd. Since `7 mod 2 = 1`, it prints "7 is Odd".

2. **Finding Remainders**:

```python linenums="1"
# Find the remainder of division
dividend = 29
divisor = 5

remainder = dividend % divisor
print(f"The remainder of {dividend} divided by {divisor} is {remainder}.")
```

**Explanation**: 
- This calculates `29 mod 5`, which results in 4, so it prints "The remainder of 29 divided by 5 is 4."

3. **Cycling Through a List**:

```python linenums="1"
# Cycling through a list of colors
colors = ["Red", "Green", "Blue"]
for i in range(10):
    print(colors[i % len(colors)])
```

**Explanation**: 
- This loops through the list of colors and prints each color, cycling through them repeatedly.

#### in-Go Examples

1. **Checking for Even or Odd**:

```go linenums="1"
package main

import "fmt"

func main() {
    number := 12

    if number % 2 == 0 {
        fmt.Println(number, "is Even")
    } else {
        fmt.Println(number, "is Odd")
    }
}
```

**Explanation**: 
- Similar to the Python example, this checks if 12 is even or odd.

2. **Finding Remainders**:

```go linenums="1"
package main

import "fmt"

func main() {
    dividend := 23
    divisor := 6

    remainder := dividend % divisor
    fmt.Printf("The remainder of %d divided by %d is %d.\n", dividend, divisor, remainder)
}
```

**Explanation**: 
- This calculates `23 mod 6` and prints the result.

3. **Cycling Through a Slice**:

```go linenums="1"
package main

import "fmt"

func main() {
    colors := []string{"Red", "Green", "Blue"}

    for i := 0; i < 10; i++ {
        fmt.Println(colors[i % len(colors)])
    }
}
```

**Explanation**: 
- This prints the colors in a cycle, just like the Python example.

---

Modulus is a fundamental operation that helps us understand the concept of remainders in division. Through relatable examples, properties, and applications, we've seen how modulus is utilized in real life and programming. Understanding this operation can enhance your mathematical skills and improve your programming capabilities.

As you continue to practice and explore, try creating your own examples and applications for modulus to reinforce your understanding. Whether you’re checking if a number is even or finding patterns in data, modulus is a powerful tool at your disposal!
