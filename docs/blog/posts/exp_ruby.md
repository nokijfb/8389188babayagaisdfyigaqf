---
date: 2023-05-16 
categories:
  - Devlog
tags:
  - ruby
  - learning
---

# Again... Experimenting with `return` but-in Ruby

#### Exampless

As usual, let's dive into a bit of experimentation to better understand `return` but nowon with Ruby. (I felt uncomfortable with Perl as I mentioned in the previous post) Anyway, back to Ruby! In Ruby, the `return` keyword is used to stop a function’s execution and give back a value from that function.<!-- more --> But there are a few things worth understanding about how it works. For example, here’s a function where we want to add two numbers and print the result:

```ruby linenums="1"
def main(a, b)
  c = a + b
  return c
  puts c
end

main(19, 18)
```

In this function, `main` takes in two parameters, `a` and `b`, adds them together, then returns the result with `return c`. After the `return`, there’s a `puts c`, which should print out `c`. But when we run this, it **doesn’t print anything**. Why?

### **Why `puts` Doesn’t Print After `return`**

When Ruby hits `return`, it immediately stops the function’s execution. So anything that comes after `return` (in this case, `puts c`) never runs. If we want `c` to print, we need to move `puts c` before `return`. Here’s how it looks fixed:

```ruby linenums="1"
def main(a, b)
  c = a + b
  puts c    # Print the value before returning it
  return c
end

main(19, 18)
```

With this order, `puts c` gets executed, so the value of `c` (37) prints before the function returns it.

### **Alternative: Printing the Function’s Return Value**

There’s another way to print the result without changing the position of `return`. Instead of using `puts` inside the function, we can print the return value of `main` directly:

```ruby linenums="1"
def main(a, b)
  c = a + b
  return c
end

puts main(19, 18)  # Print the result of the function call
```

With this approach, `main` just returns the value of `c`, while the `puts` outside of it takes care of printing it.

### **Using `puts` and `return` Together in One Line**

Alternatively, we can write `puts` along with `return` in a single line, like this:

```ruby linenums="1"
def main(a, b)
  c = a + b
  return puts(c)
end

main(19, 18)
```

In this example, `puts(c)` will print when the function runs. But there’s a catch: in Ruby, `puts` always returns `nil`. So, even though this code works for printing the result, the value returned by `main` isn’t `c`—it’s `nil`.

### **Best Practice Recommendation**

If you want the function to both print and return the value of `c`, use code like this:

```ruby linenums="1"
def main(a, b)
  c = a + b
  puts c
  return c
end

main(19, 18)
```

Or, even simpler, you can skip `return` entirely since Ruby automatically returns the last evaluated expression:

```ruby linenums="1"
def main(a, b)
  c = a + b
  puts c
end

main(19, 18)
```
