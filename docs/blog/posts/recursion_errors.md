---
date: 2023-05-12 
categories:
  - Devlog
tags:
  - python
  - go
  - perl
  - learning
---

# Recursion Errors
##### DIVING-IN

Do you remember the **recursion error** that occurred in the previous article? I wanted to dig deeper into this phenomenon once again. A quick recap: a **recursion error** happens when a function continually calls itself without a clear stopping condition, leading to excessive memory usage and eventually throwing an error when the memory stack is exceeded.<!-- more --> In other words, if a function can't complete its call and keeps invoking itself, you will encounter **infinite recursion**, which results in a recursion error.

In this experiment, I will explore how **recursion errors** arise in **Python**, **Go**, and **Perl**.

#### Testing in Python

I started with **Python**. The code I wrote was:

```python linenums="1"
def is_even(x):
    return not is_odd(x)

def is_odd(x):
    return not is_even(x)
```

When I ran this function with an argument, for example, `is_even(2)`, it resulted in a **recursion error**. The **is_even** function calls **is_odd**, which in turn calls **is_even** again, and so on, without any stopping condition. 

Next, I tried adding an additional argument to the function:

```python linenums="1"
print(is_even(2, 3))  # Adding a second argument
```

I received the following error:

```
TypeError: is_even() takes 1 positional argument but 2 were given
```

This error indicates that the **is_even** function wasn't designed to accept more than one argument. This isn't a recursion error, but rather an issue with the number of arguments being passed.

#### Switching to Go

After trying Python, I moved on to **Go**. The code I wrote was similar to the one in Python:

```go linenums="1"
func isEven(x int) bool {
    return !isOdd(x)
}

func isOdd(x int) bool {
    return !isEven(x)
}
```

When I ran this function with a single argument, like `isEven(2)`, I also encountered a **recursion error**. This happens because the **isEven** function calls **isOdd**, and so on, with no clear stopping condition.

However, when I tried to pass two arguments:

```go linenums="1"
fmt.Println(isEven(2, 3))
```

I encountered this error:

```
cannot use 2 (type int) as type []int in argument to isEven
```

This error shows that the **isEven** function doesn't accept two arguments at once. There's no recursion here because the code can't be invoked at all with an incorrect number of arguments.

#### Exploring Perl

Finally, I turned to **Perl** to see how it handles a similar situation. The code I wrote was:

```perl linenums="1"
sub is_even {
    return !is_odd($_[0]);
}

sub is_odd {
    return !is_even($_[0]);
}
```

I tried running this function with a single argument:

```perl linenums="1"
print is_even(2);
```

Here, I also encountered a **recursion error**, because these functions call each other endlessly. However, when I passed two arguments:

```perl linenums="1"
print is_even(2, 3);
```

I got the following error message:

```
Deep recursion on subroutine "main::is_even" at script.pl line xx.
```

In the code above, I used `$_[0]` to capture the first argument passed to the function. Using `$_[0]` is a common way to capture arguments in Perl. If I wanted to accept more than one argument, I would use **`@_`**. As I wrote the code, I wondered what would happen if I used **`@_`**. So, I modified my code to:

```perl linenums="1"
sub is_even {
    return !is_odd(@_);
}

sub is_odd {
    return !is_even(@_);
}
```

By using **`@_`**, I allowed the function to accept all arguments passed to it. So when I called **is_even(2, 3)**, both arguments **2** and **3** were passed to **is_odd**, which in turn called **is_even** with the same arguments. Without any limit or stopping condition, the two functions continue to call each other endlessly, causing the program to run out of stack space and throw an error.

#### Solutions to Avoid Recursion Errors

After conducting a series of experiments, I began to wonder *"how I could prevent this `recursion error` from occurring in the first place"*. So, here are some solutions I tried for each language:

#### Python
In Python, I realized that adding type checks can be very helpful. For example, I decided to ensure that the argument passed is an integer before proceeding:

```python linenums="1"
def is_even(x):
    if isinstance(x, int):  # Check if x is an integer
        return not is_odd(x)
    return None  # Return None if x is not an integer

def is_odd(x):
    if isinstance(x, int):  # Check if x is an integer
        return not is_even(x)
    return None  # Return None if x is not an integer
```

This can prevent unnecessary recursion when an invalid argument is passed.

#### Go
In Go, I also tried adding a simple validation function. This helps ensure that only one argument is accepted before calling the recursive function:

```go linenums="1"
func isEven(x int) bool {
    return !isOdd(x)
}

func isOdd(x int) bool {
    return !isEven(x)
}

// Function to validate the argument
func isValid(n int) bool {
    return n >= 0  // For example, only accept non-negative integers
}
```

By adding this validation function, I felt safer calling the recursive function, knowing that the argument passed meets certain criteria.

#### Perl
Lastly, for Perl, I thought about using logic to check the number of arguments received. I wrote code that only proceeds if exactly one argument is passed:

```perl linenums="1"
sub is_even {
    return !is_odd($_[0]) if @_ == 1;  # Check for one argument
    return undef;  # Return undef if more than one argument is passed
}

sub is_odd {
    return !is_even($_[0]) if @_ == 1;  # Check for one argument
    return undef;  # Return undef if more than one argument is passed
}
```

To avoid **recursion errors** in Perl, I also thought about adding a type check, similar to the approach in Python. For example, I could add code to check if the argument is an integer:

```perl linenums="1"
sub is_even {
    return undef unless defined $_[0] && $_[0] =~ /^\d+$/;  # Check if the argument is an integer
    return !is_odd($_[0]) if @_ == 1;  # Check for one argument
    return undef;  # Return undef if more than one argument is passed
}

sub is_odd {
    return undef unless defined $_[0] && $_[0] =~ /^\d+$/;  # Check if the argument is an integer
    return !is_even($_[0]) if @_ == 1;  # Check for one argument
    return undef;  # Return undef if more than one argument is passed
}
``` 
This line is present in both is_even and is_odd functions.

- defined `$_[0]`: Checks if the first argument (input) is defined (not `undef`).
- `$_[0] =~ /^\d+$/`: Uses a [regular expression](https://perldoc.perl.org/perlre#Regular-Expressions) to ensure that the input is a valid integer (a `string` of `digits`).

This input validation step ensures that both functions only process valid integers. If the input is invalid (either not provided or not an integer), the function returns `undef`. This prevents potential errors and ensures the functions operate correctly.

This ensures that only valid integer arguments are processed, helping avoid potential recursion issues.<br>
Just a disclaimer, all the solutions I’ve written above are purely based on my own experiments, so they aren’t definitive or entirely accurate ways to resolve recursion errors. I’m sure there are simpler and more effective methods out there to address this issue.

---
><h3>In computing, recursion is a fundamental method for specifying an algorithm, it allows a problem to be broken down into simpler instances of the same problem.</h3>
>
>*Niklaus Wirth*<br>
>*Computer scientist and programming languages inventor ~ 1934/2024*
