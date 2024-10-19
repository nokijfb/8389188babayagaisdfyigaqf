---
date: 2023-05-11 
categories:
  - Devlog
tags:
  - python
  - learning
---

# Fibonacci Sequence 
#### AND THE IMPORTANCE of BASE CASE IN RECURSION

I came across a funny meme on YouTube featuring the code like this:

```python linenums="1"
def fibo(n): 
	return fibo(n - 1) + fibo(n - 2).
```

In the meme, A guy was dancing while pointing down and making copies of himself, who kept calling their clones without end, just like the recursive function.<!-- more --> This got me curious: could it really work like that? So, I decided to dive in and see if I could implement it in Python.

#### Implementing Fibonacci with Recursion

Back to meme, I was decided to implement this sequence using a recursive function like this:

```python linenums="1"
def fibo(n):
    return fibo(n - 1) + fibo(n - 2)

if __name__ == "__main__":
    fibo(1)
```

And that's what I predicted, error..., I encountered a **RecursionError**:

```bash linenums="1"
Traceback (most recent call last):
  File "/path/to/file.py", line 5, in <module>
    fibo(1)
    ~~~~^^^
  File "/path/to/file.py", line 2, in fibo
    return fibo(n - 1) + fibo(n - 2)
           ~~~~^^^^^^^
  File "/path/to/file.py", line 2, in fibo
    return fibo(n - 1) + fibo(n - 2)
           ~~~~^^^^^^^
  File "/path/to/file.py", line 2, in fibo
    return fibo(n - 1) + fibo(n - 2)
           ~~~~^^^^^^^
  [Previous line repeated 996 more times]
RecursionError: maximum recursion depth exceeded
```

#### What Is the Fibonacci Sequence and why it's error?

So, that’s from what I know (sorry if I’m wrong). the Fibonacci sequence starts with `0` and `1`, and each subsequent number is the sum of the two preceding ones. The sequence looks like this:

- **0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...**

Each number can be represented as:
- `fibo(0) = 0`
- `fibo(1) = 1`
- `fibo(2) = fibo(1) + fibo(0) = 1`
- `fibo(3) = fibo(2) + fibo(1) = 2`
- `fibo(4) = fibo(3) + fibo(2) = 3`
- And so on...

The **ErrorMessage above** tells us that the maximum recursion depth has been exceeded. This means that my function kept calling itself repeatedly without stopping. Here’s how to read the message:

- `Traceback (most recent call last)`: This indicates where the error originated from.
- `File "/path/to/file.py", line X`: This shows the file and line number where the error occurred.
- `fibo(1)`: This line indicates that the function `fibo(1)` was called.
- `return fibo(n - 1) + fibo(n - 2):` This line shows the recursive call that leads to the next level of recursion.

The repetition of lines shows that `fibo(n - 1)` and `fibo(n - 2)` were called recursively, but since there was no base case defined, the function kept calling itself endlessly.

#### The Solution: Adding Base Case

Without a **base case**, the function will keep calling itself indefinitely. A base case is a condition that stops the recursion. So, I needed to define conditions to stop the recursion. Here’s the corrected version of the code:

```python linenums="1"
def fibo(n):
    if n == 0:  # Base case
        return 0  # Return 0 if n is 0
    elif n == 1:  # Base case
        return 1  # Return 1 if n is 1
    else:
        return fibo(n - 1) + fibo(n - 2)  # Recursive call

if __name__ == "__main__":
    print(fibo(1))  # Output: 1
    print(fibo(2))  # Output: 1
    print(fibo(3))  # Output: 2
    print(fibo(4))  # Output: 3
```

### How Base Case Works

In this implementation, the base cases are:
- If `n` equals `0`, the function returns `0`.
- If `n` equals `1`, the function returns `1`.

Now, when I call `fibo(1)`, the function recognizes that it matches the base case and returns `1`. Similarly, calling `fibo(0)` will return `0`. For other values of `n`, the function will continue to break down the problem until it reaches one of the base cases.

---
The Fibonacci sequence is a classic example of how recursion can elegantly solve problems, but it also highlights the necessity of a well-defined base case. Without it, you risk infinite recursion and program crashes.
