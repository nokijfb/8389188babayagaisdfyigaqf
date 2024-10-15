---
date: 2023-05-03
categories:
  - Devlog
tags:
  - perl
  - learning
---

# Primitive Data Type or Perl Wierdo-Data type Design?
#### EXPLORING DATA TYPE and `scalar` REFERENCES IN PERL

In Perl, data types are fundamental concepts that determine how data is stored and manipulated. Perl has several built-in data types, including scalars, arrays, hashes, and references. Among these, the three primitive data types are *scalars*, *arrays*, and *hashes*.<!-- more --> Understanding these types is essential for writing efficient and effective Perl code.

#### Scalar Variables
Scalar variables hold single values, such as strings or numbers. They are denoted with a dollar sign ($). Scalars can store different types of data, including:

**String**: A sequence of characters.
**Number**: An integer or floating-point number.
**Boolean**: Represents truth values, true or false.

```perl linenums="1"
my $scalar_string = "Hello, World!";  # String
my $scalar_number = 42;                 # Integer
my $scalar_float = 3.14;                # Floating-point number
```

#### Array Variables
Arrays are ordered lists of scalars. Each element in an array can be accessed using its index, which starts at zero. Arrays are denoted with the @ symbol.

```perl linenums="1"
my @array = ("apple", "banana", "cherry");
print $array[0];  # Outputs "apple"
```

#### Hash Variables
Hashes are unordered collections of key-value pairs. Each key must be unique, and they are denoted with the % symbol. Hashes allow for efficient data retrieval using keys.

```perl linenums="1"
Copy code
my %hash = (
    "name" => "John",
    "age" => 30,
    "city" => "New York"
);
print $hash{"name"};  # Outputs "John"
```

#### What Are References?

References in Perl are **special variables** that allow you to create more complex data structures by pointing to other variables, such as scalars, arrays, or hashes. Think of a reference as a way to "link" to another variable instead of holding its actual value. This is useful when you want to manipulate or organize your data in a flexible way.

#### Creating References

To create a reference to a variable, you use the backslash operator (`\`). This operator allows you to obtain the memory address of the variable you want to reference. For example:

```perl linenums="1"
my $value = "Hello";      # A scalar variable
my $ref = \$value;       # Creating a reference to $value
```

In this case, `$ref` is not storing the string "Hello" directly; instead, it holds a reference to the location in memory where `$value` is stored. This means you can change the value of `$value` through `$ref`.

#### Dereferencing

To access or modify the value that a reference points to, you need to "dereference" it using the double dollar sign (`$$`). This allows you to interact with the original variable directly.
Here's how you can change the value of `$value` using `$ref`:

```perl linenums="1"
print "Before: $$ref\n";  # Outputs "Hello"

$$ref = "World";          # Change the value of $value through the reference

print "After: $value\n";  # Now $value is "World"; the original variable has been changed, not a copy or shadow. 
```

#### Nested References

Nested references in Perl allow you to create a reference to another reference, enabling even more complex data structures. This can be particularly useful when dealing with multi-dimensional arrays or hashes that require layers of indirection. Understanding nested references can enhance your ability to manage and manipulate complex data.

#### Creating Nested References

To create a nested reference, you simply take the reference you already have and apply the backslash operator (`\`) to it. This process creates a reference that points to the first reference. For instance:

```perl linenums="1"
my $value = "Hello";            # Initial scalar variable
my $ref = \$value;             # Reference to $value
my $ref_to_ref = \$ref;        # Creating a reference to the reference
```

In this example, `$ref_to_ref` holds a reference to `$ref`, which means it indirectly points to the original scalar variable `$value`.

#### Dereferencing Nested References

To access or modify the value of the original variable through a nested reference, you need to dereference it multiple times. Each level of indirection requires an additional dollar sign (`$`). Here’s how it works:

```perl linenums="1"
print "Before: $$$ref_to_ref\n";  # Outputs "Hello"
```

In this line, `$$$ref_to_ref` first dereferences `$ref_to_ref` to get `$ref`, and then dereferences `$ref` to get the value of `$value`. Therefore, the output will be "Hello".

#### Modifying Values Through Nested References

You can also modify the original variable using nested references. This is done by dereferencing the nested reference and assigning a new value:

```perl linenums="1"
$$$ref_to_ref = "Nested World";   # Change the value of $value
```

This line assigns "Nested World" to `$value` through the nested reference. 

#### Example of Nested References in Action

Here’s a complete example demonstrating the creation and manipulation of nested references:

```perl linenums="1"
my $value = "Hello";              # Initial scalar variable
my $ref = \$value;               # Reference to $value
my $ref_to_ref = \$ref;          # Creating a reference to the reference

print "Before: $$$ref_to_ref\n";  # Outputs "Hello"

$$$ref_to_ref = "Nested World";    # Change the value of $value

print "After: $value\n";            # Now $value is "Nested World"
```

In this example:
1. We start with a scalar variable `$value`.
2. We create a reference `$ref` to `$value`.
3. We then create a nested reference `$ref_to_ref` to `$ref`.
4. Finally, we modify the original `$value` through `$ref_to_ref`, demonstrating how nested references provide powerful capabilities for data manipulation.

#### Practical Uses of References

References, including nested references, are often used in more advanced Perl programming scenarios, such as:

1. **Complex Data Structures**: You can use references to create arrays of arrays or hashes of hashes, allowing you to store related data together efficiently.
   
   ```perl linenums="1"
   my @array_of_arrays = (
       [1, 2, 3],
       [4, 5, 6],
       [7, 8, 9]
   );
   ```

2. **Memory Efficiency**: References enable you to pass large data structures around without copying all the data, saving memory and improving performance.

3. **Manipulating Values**: If you want to change multiple values through references, you can loop through an array of references easily.

4. **Managing Configurations**: References can help in managing configurations where settings may refer to other settings, creating a clear and organized structure.

#### Example of Modifying Values Through References

```perl linenums="1"
my $bandung = "kota";
my $jakarta = "ibukota";  
my @ref = (\$bandung, \$jakarta);  # Array of references

# Change all values through references
foreach my $r (@ref) {
    $$r = "desa";  # Dereference and change the value
}

# Print results
print "$bandung & $jakarta\n";  # Outputs "desa & desa"
```

---
Perl are allows to deep levels of dereferencing, it's essential to keep your code clear and readable. When dealing with complex data structures, consider restructuring your code for better clarity.

This exploration of data types and references in Perl provides a foundation for writing robust scripts and managing data effectively.
