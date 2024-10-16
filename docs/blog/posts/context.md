---
date: 2023-05-04
categories:
  - Devlog
tags:
  - perl
  - learning
---

# Context and Arguments gave me a headache for a while.
#### DEBUGGING a PERL `sub`

While learning on a simple Perl subroutine, I encountered an issue that left me puzzled. It seemed straightforward: I was trying to pass two numbers into a subroutine, add them, and print the result. However, instead of getting what I expected, I received a strange output.<!-- more --> This experience led me to discover the concept of **context** in Perl, which is crucial (in my opinion) for understanding how Perl evaluates expressions.

#### The Initial Confusion

Here's the code that initially confused me:

```perl linenums="1"
#!/usr/bin/env perl
use strict;
use warnings;

sub result {
    my $a = @_;
    my $b = @_;
    return $a + $b;
}

sub main {
    print result(13, 15), "\n";  # Expected output: 28
}

main;
```

In this code, I expected the output to be `28` because I passed `13` and `15` into the `result` subroutine. The subroutine was supposed to add them and return the result. But instead, I got `4`. This result made me stop and question, <i>"***bruh, what was happening behind the scenes..?***"</i>

#### Breaking Down the Problem

The line that puzzled me was this one inside the `result` subroutine:

```perl linenums="1"
my $a = @_;  # Why is $a 2?
my $b = @_;  # Why is $b also 2?
```

I had assumed that `$a` and `$b` would each get the values `13` and `15`, but that clearly wasn’t happening. Instead, both `$a` and `$b` were somehow assigned the value `2`. This led me to ask: why was Perl giving me `2` instead of `13` and `15`?

#### Discovering Scalar Context

It turns out that when I wrote `my $a = @_;`, I was putting `@_`—which holds the subroutine arguments—into **scalar context**. In scalar context, an array does not return its elements; instead, it returns the number of elements it contains (*how many indexes are there*). In this case, since I passed two arguments (`13` and `15`), `@_` returned `2`. Therefore, both `$a` and `$b` were assigned the value `2`, leading to the output of `4` because the subroutine returned `2 + 2`.

#### Unpacking Arguments

To access the arguments I passed into the subroutine correctly, I needed to unpack them from `@_` properly. Here’s the change I made:

```perl linenums="1"
sub result {
    my ($a, $b) = @_;  # Unpack the arguments into $a and $b
    return $a + $b;    # Now returns 28 as expected
}
```

With this modification, when I called `result(13, 15)`, `$a` was assigned the value `13`, and `$b` was assigned the value `15`. The subroutine now added them correctly, resulting in `28`, which was what I originally expected.

Here's an expanded version of the section on **Understanding List Context** to provide more context and explanation:

---

#### Understanding List Context

So, what changed here? Why did the behavior differ just because I added parentheses around `$a` and `$b`? The answer lies in something called **list context** (*TBH: I got this term from Google... lol*). 

In Perl, context matters a lot when it comes to evaluating expressions. The context determines how variables, subroutine arguments, and array elements are treated by the interpreter. 

When I wrote:

```perl
my ($a, $b) = @_;  # List context
```

I instructed Perl to evaluate `@_` in **list context**. This means that instead of treating the entire array as a single scalar value, Perl looks at each individual element within the array. In this case, it would return the elements `13` and `15`, assigning those values directly to `$a` and `$b`. 

On the other hand, when I wrote:

```perl
my $a = @_;
my $b = @_;
```

I didn't use parentheses, and as a result, Perl evaluated `@_` in **scalar context**. In this context, Perl interprets the expression differently: instead of pulling out individual elements, it returns the number of elements in the array, which is `2`. Thus, both `$a` and `$b` were assigned the value of `2`.

For me, this distinction is crucial for understanding how Perl operates, because it influences how data is assigned and manipulated within the program. Whether I working with single values or lists, it can change the outcome of calculations significantly.

#### Exploring Other Contexts

As I worked through this issue, I began to wonder if there were other contexts in Perl that influenced behavior. Here are several key contexts, along with detailed examples:

 **Scalar Context**:
 
   - In scalar context, an array or a list will evaluate to a single value, typically the count of elements.
   **Example**:
     ```perl linenums="1"
     my @array = (1, 2, 3, 4);
     my $count = @array;  # $count holds the number of elements in @array
     # If @array has 4 elements, $count will be 4.
     ```
     
   - When you use `@array` in a context expecting a scalar (like an assignment to a scalar variable), it evaluates to the number of elements.

 **List Context**:
 
   - In list context, expressions can return multiple values, which can be assigned to an array or unpacked into individual scalars.
   
   **Example**:
     ```perl linenums="1"
     my @array = (1, 2, 3);
     my ($first, $second) = @array;  # $first is 1, $second is 2
     ```
     
   - Here, the values from `@array` are unpacked into `$first` and `$second`, retrieving the first two elements.

 **Void Context**:
 
   - Void context is when a function's return value is ignored. This often happens when you call a subroutine but don't assign its result.
   
   **Example**:
     ```perl linenums="1"
     sub do_nothing {
         return 1;  # This value is ignored
     }
     do_nothing();  # The return value from do_nothing() is discarded.
     ```
     
   - Here, the return value from `do_nothing()` is ignored entirely.

 **Numeric Context**:
 
   - In numeric context, strings can be treated as numbers, and Perl will automatically convert them when needed.
   **Example**:
     ```perl linenums="1"
     my $sum = "5" + "10";  # Numeric context converts strings to numbers
     # Here, "5" and "10" are treated as numbers, so $sum becomes 15.
     ```
     
   - Perl performs implicit conversion, treating the string values as numbers for arithmetic operations.

 **String Context**:
 
   - In string context, values are treated as strings, allowing string operations like concatenation.

   **Example**:
     ```perl linenums="1"
     my $text = "Hello, " . "world!";  # Strings are concatenated
     # This concatenation results in $text being "Hello, world!".
     ```
     
   - In this case, the `.` operator is used to concatenate the two strings.

#### Scalar vs. List Context

This is taught me an essential lesson about how Perl (in a weird way) handles data: **context matters**. Perl evaluates expressions differently depending on whether it expects a single value (scalar context) or multiple values (list context). 

I had run into this without realizing it, and by making a small change to how I wrote the code, I was able to achieve the behavior I wanted. 

---
It was both confusing and enlightening, but I learned that by paying attention to context, I could avoid pitfalls in my code and ensure that my subroutines worked as intended. This awareness will undoubtedly save me a lot of headaches.
