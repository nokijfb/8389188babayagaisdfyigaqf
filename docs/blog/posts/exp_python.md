---
date: 2023-05-16 
categories:
  - Devlog
tags:
  - python
  - learning
---

# Again... Experimenting with `return` but-in Python

#### Examples

As usual, let's dive into a bit of experimentation to better understand `return`, but this time with Python. (I felt uncomfortable with Perl as I mentioned in the previous post.) Anyway, back to Python! In Python, the `return` keyword is used to stop a function’s execution and give back a value from that function. But there are a few things worth understanding about how it works.<!-- more --> For example, here’s a function where we want to add two numbers and print the result:

```python linenums="1"
def main(a, b):
    c = a + b
    return c
    print(c)  # This line won't execute

main(19, 18)
```

In this function, `main` takes in two parameters, `a` and `b`, adds them together, then returns the result with `return c`. After the `return`, there’s a `print(c)`, which should print out `c`. But when we run this, it **doesn’t print anything**. Why?

### **Why `print` Doesn’t Work After `return`**

When Python hits `return`, it immediately stops the function’s execution. So anything that comes after `return` (in this case, `print(c)`) never runs. If we want `c` to print, we need to move `print(c)` before `return`. Here’s how it looks fixed:

```python linenums="1"
def main(a, b):
    c = a + b
    print(c)  # Print the value before returning it
    return c

main(19, 18)
```

With this order, `print(c)` gets executed, so the value of `c` (37) prints before the function returns it.

### **Alternative: Printing the Function’s Return Value**

There’s another way to print the result without changing the position of `return`. Instead of using `print` inside the function, we can print the return value of `main` directly:

```python linenums="1"
def main(a, b):
    c = a + b
    return c

print(main(19, 18))  # Print the result of the function call
```

With this approach, `main` just returns the value of `c`, while the `print` outside of it takes care of printing it.

### **Using `print` and `return` Together in One Line**

Alternatively, we can write `print` along with `return` in a single line, like this:

```python linenums="1"
def main(a, b):
    c = a + b
    return print(c)  # Note: This returns None

main(19, 18)
```

In this example, `print(c)` will print when the function runs. But there’s a catch: in Python, `print` always returns `None`. So, even though this code works for printing the result, the value returned by `main` isn’t `c`—it’s `None`.

### **Best Practice Recommendation**

If you want the function to both print and return the value of `c`, use code like this:

```python linenums="1"
def main(a, b):
    c = a + b
    print(c)
    return c

main(19, 18)
```

Or, even simpler, you can skip `return` entirely since Python automatically returns the last evaluated expression:

```python linenums="1"
def main(a, b):
    c = a + b
    print(c)

main(19, 18)
```
