---
date: 2023-04-22
categories:
  - Devlog
tags:
  - python
  - javascript
  - perl
  - PL/I
  - pascal
  - learning
---

#Subroutines nor Functions
#### UNDERSTANDING `SUBROUTINES` AND `FUNCTIONS` IN PROGRAMMING

In programming, **subroutines** and **functions** are essential concepts that help organize code, promote reusability, and improve readability. While these terms are often used interchangeably, they can have different meanings depending on the programming language and context.<!-- more --> In this article, we will explore what subroutines and functions are, how they differ, and provide examples from various programming languages to illustrate these concepts.

#### What Are Subroutines?

A **subroutine** is a block of code that performs a specific task and can be called upon whenever needed throughout a program. Subroutines can take inputs (known as parameters or arguments) and may or may not return a value. They help avoid repetition by allowing programmers to write a piece of code once and reuse it multiple times.

#### What Are Functions?

A **function** is a type of subroutine that is specifically designed to return a value. Functions take input, perform operations, and return a result. Every function can be seen as a subroutine, but not every subroutine is a function. Functions are a fundamental part of many programming languages and are crucial for calculations and data processing.

#### Differences Between Functions and Subroutines

- **Return Value**: The most significant difference is that functions always return a value, while subroutines may not.
- **Usage**: Functions are often used when a specific result is needed, while subroutines can be used for actions that do not require a return value.

### Examples in Different Programming Languages

Let’s look at how different programming languages implement subroutines and functions.

#### 1. Python

In Python, functions are the primary means of creating reusable code blocks. Here’s an example of a simple function:

```python linenums="1"
def add_numbers(a, b):  # This is a function
    return a + b  # It returns the sum of a and b

result = add_numbers(5, 3)
print("The sum is:", result)  # Output: The sum is: 8
```

In this example, `add_numbers` is a function that takes two parameters, `a` and `b`, and returns their sum.

#### 2. JavaScript

JavaScript uses functions extensively, similar to Python. Here’s how you can define a function:

```javascript linenums="1"
function greet(name) {  // This is a function
    return "Hello, " + name;  // It returns a greeting message
}

let message = greet("Alice");
console.log(message);  // Output: Hello, Alice
```

The `greet` function takes one parameter, `name`, and returns a greeting string.

#### 3. Perl

In Perl, the term **subroutine** is commonly used. Here’s an example:

```perl linenums="1"
sub multiply {  # This is a subroutine
    my ($x, $y) = @_;  # Getting parameters
    return $x * $y;  # Returning the product
}

my $result = multiply(4, 5);
print "The product is: $result\n";  # Output: The product is: 20
```

In this example, `multiply` is a subroutine that takes two parameters and returns their product.

#### 4. PL/I 

PL/I specifically uses the term **subroutine** as well. Here's an example of defining a subroutine:

```pascal linenums="1"
DCL multiply ENTRY(FIXED DECIMAL(5,2), FIXED DECIMAL(5,2)) RETURNS(FIXED DECIMAL(5,2));  // Subroutine declaration

multiply: PROCEDURE(x, y) 
    DCL x FIXED DECIMAL(5,2);
    DCL y FIXED DECIMAL(5,2);
    RETURN x * y;  // Returning the product
END multiply;

DCL result FIXED DECIMAL(5,2);
result = multiply(4.5, 2.0);  // Calling the subroutine
PUT DATA('The product is: ', result);  // Output: The product is: 9.00
```

Here, the `multiply` subroutine calculates the product of two numbers.

#### 5. Pascal

In Pascal, there are two types of subroutines: procedures and functions. Here’s how you can define both:

```pascal linenums="1"
function add(a, b: Integer): Integer;  // Function declaration
begin
    add := a + b;  // Returning the sum
end;

procedure greet(name: string);  // Procedure declaration
begin
    WriteLn('Hello, ', name);  // Printing a greeting
end;

var
    sum: Integer;
begin
    sum := add(5, 3);  // Calling the function
    WriteLn('The sum is: ', sum);  // Output: The sum is: 8
    greet('Alice');  // Calling the procedure
end.
```

In this example, `add` is a function that returns a value, while `greet` is a procedure that does not return a value.

---
Two of them provide a way to break down complex problems into smaller, manageable parts, promoting code reuse and organization. While the terminology may vary across different programming languages, the underlying concepts remain similar and consistent.
