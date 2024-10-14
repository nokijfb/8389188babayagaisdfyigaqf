---
date: 2023-04-26
categories:
  - Devlog
tags:
  - perl
  - learning
---

# Ways to Call `sub` in perl
#### HANDLING ARGUMENTS IN PERL `sub`

In Perl, subroutines are a fundamental part of code organization. Understanding how to handle arguments correctly is essential to learn.<!-- more --> This article will specifically address the use of the `&` symbol when calling subroutines and how it affects argument handling.

## Declaring a Subroutine

To declare a subroutine, use the `sub` keyword. Here’s an example of a simple subroutine that adds two numbers:

```perl linenums="1"
sub add_numbers {
    my ($num1, $num2) = @_;  # Capture arguments into variables
    return $num1 + $num2;    # Return the sum
}
```

### Calling the Subroutine

You can call a subroutine simply by using its name followed by parentheses:

```perl linenums="1"
my $result = add_numbers(5, 10);  # Outputs: 15
print "Result without &: $result\n";  # Outputs: 15
```

## The Role of the `&` Symbol

In Perl, you can also call subroutines using the `&` symbol. Here’s how it looks:

```perl linenums="1"
my $result_with_ampersand = &add_numbers(5, 10);
print "Result with &: $result_with_ampersand\n";  # Outputs: 15
```

### Differ in Behavior

1. **Without `&`**:
   - When you call a subroutine without using the `&`, Perl automatically prepares the argument list and populates the special array `@_`. This is the recommended approach as it keeps the code clean and straightforward.

2. **With `&`**:
   - Using the `&` symbol prevents Perl from altering the argument list. The arguments will not be automatically passed to `@_`, and you can pass a different list of arguments if desired. This can be useful in specific scenarios, but it may lead to confusion if not handled carefully.

### Example Comparison

Let’s illustrate the difference between calling a subroutine with and without the `&` symbol.

```perl linenums="1"
sub show_values {
    my ($first, $second) = @_;  # Capture the arguments
    return "First: $first, Second: $second";
}

# Calling without &
my $output1 = show_values(1, 2);  # Output: First: 1, Second: 2

# Calling with &
my $output2 = &show_values(3, 4);  # Output: First: 3, Second: 4

print $output1;  # Outputs: First: 1, Second: 2
print $output2;  # Outputs: First: 3, Second: 4
```

### Key Takeaways

- **Use Standard Calls**: It's generally best to call subroutines without the `&` symbol to maintain clarity and ensure that the argument list is handled properly.

- **Explicit Argument Passing**: When using the `&` symbol, be aware that you're bypassing the automatic argument handling, which can lead to unexpected behavior. Here are two examples to illustrate this:

  - **Example 1 - Missing Arguments**:
    ```perl linenums="1"
    sub calculate_product {
        my ($a, $b) = @_;  # Capture arguments
        return $a * $b;    # Return product
    }

    my $result1 = calculate_product(3);          # Outputs: 0 (since $b is undefined)
    my $result2 = &calculate_product(3);         # Outputs: 0 (still, since $b is undefined)

    print "Result without &: $result1\n";        # Outputs: 0
    print "Result with &: $result2\n";           # Outputs: 0
    ```
    In this case, both calls produce the same unexpected result because the second argument is missing, leading to `undefined` behavior.

  - **Example 2 - Altered Arguments**:
    ```perl linenums="1"
    sub greet {
        my ($name) = @_;  # Capture argument
        return "Hello, $name!";
    }

    my $greeting1 = greet("Alice");              # Outputs: Hello, Alice!
    my $greeting2 = &greet("Bob");                # Outputs: Hello, Bob!

    # Now, let's modify and call it with different arguments
    my $greeting3 = &greet("Charlie", "Diana");  # Outputs: Hello, Charlie! (only the first is used)

    print $greeting1;  # Outputs: Hello, Alice!
    print $greeting2;  # Outputs: Hello, Bob!
    print $greeting3;  # Outputs: Hello, Charlie! (the second argument is ignored)
    ```
    Here, the last call illustrates how extra arguments passed with `&` are ignored, which can lead to confusion if the developer expects all arguments to be processed.

---
The conclusion is, `&` symbol can be useful in specific contexts, it’s important to use it judiciously to avoid confusion.
