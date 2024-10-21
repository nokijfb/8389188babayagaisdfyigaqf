---
date: 2023-05-13 
categories:
  - Devlog
tags:
  - perl
  - learning
---

# Looping Scheme
#### HOW DOES LOOPING ACTUALLY WORK IN PERL?

Let’s talk about looping one more time. I began wondering how exactly looping works in Perl. This language provides several useful types of loops for repeating code blocks: `while`, `until`, `for`, and `foreach`.<!-- more --> At first, I thought the concepts were similar to other languages I’ve tried, but after digging deeper, I found some eccentric details worth exploring further.

### Explanation and Simple Examples for Each Loop

#### While Loop

This loop continues as long as its condition is true. For instance, if we want to print numbers from 1 to 5:

```perl
my $i = 1;
while ($i <= 5) {
    print "$i\n";
    $i++;
}
```

Here, as long as `$i` is less than or equal to 5, the loop will run, and `$i` increases with each iteration.

---
Let's summing numbers from 1 to 10.
###### This may be redundant, but it shows how it works sequentially.

```perl
my $sum = 0;
my $i = 1;
while ($i <= 10) {
    $sum += $i;
    $i++;
}
print "Total sum: $sum\n";
```

#### Until Loop

This is the opposite of `while`. The loop will continue until its condition becomes true. A simple example:

```perl
my $i = 1;
until ($i > 5) {
    print "$i\n";
    $i++;
}
```

Here, the loop keeps running until `$i` is greater than 5. In other words, the loop stops when the condition is true.

#### For Loop

If you’ve used other programming languages, this loop may look familiar. We can print numbers from 1 to 5 like this:

```perl
for (my $i = 1; $i <= 5; $i++) {
    print "$i\n";
}
```

This loop has three parts: initialization (`$i = 1`), condition (`$i <= 5`), and the action after each iteration (`$i++`).

#### Foreach Loop

The `foreach` loop is typically used to iterate over lists or arrays. For example, if we have a list of names:

```perl
my @names = ('Alice', 'Bob', 'Charlie');
foreach my $name (@names) {
    print "$name\n";
}
```

This will print each element of the `@names` array.

---
Printing values from an array with a suffix.

```perl
my @scores = (90, 80, 70);
foreach my $score (@scores) {
    print "Score: $score\n";
}
```

### Operators in the Until Loop

Many people assume that conditions in an `until` loop can only use `==`, but there are many other logical operators you can use to control when the loop stops. Here are some options:

#### Equality Operators: `==` and `!=`

- `==`: Compares two numbers for equality.
- `!=`: Compares two numbers for inequality.

**Example:**

```perl
my $i = 1;
until ($i == 5) {
    print "$i\n";
    $i++;
}
```

This loop will stop when `$i` equals 5.

```perl
my $i = 1;
until ($i != 5) {
    print "$i\n";
    $i++;
}
```

This loop will continue as long as `$i` is not equal to 5.

#### Comparison Operators: `<`, `>`, `<=`, `>=`

- `<`: True if the left value is less than the right value.
- `>`: True if the left value is greater than the right value.
- `<=`: True if the left value is less than or equal to the right value.
- `>=`: True if the left value is greater than or equal to the right value.

**Example:**

```perl
my $i = 10;
until ($i < 5) {
    print "$i\n";
    $i--;
}
```

The loop will continue as long as `$i` is not less than 5.

#### String Operators: `eq`, `ne`, `lt`, `gt`, `le`, `ge`

- `eq`: Equal to, for strings.
- `ne`: Not equal to, for strings.
- `lt`: Less than, for strings.
- `gt`: Greater than, for strings.
- `le`: Less than or equal to, for strings.
- `ge`: Greater than or equal to, for strings.

**Example:**

```perl
my $name = 'Alice';
until ($name eq 'Charlie') {
    print "$name\n";
    $name = 'Charlie';
}
```

The loop will stop when `$name` equals 'Charlie'.

#### Other Operators: `&&`, `||`

You can also use logical operators:

- `&&`: True if both conditions are true.
- `||`: True if either condition is true.

**Example:**

```perl
my $i = 1;
until ($i > 5 && $i < 10) {
    print "$i\n";
    $i++;
}
```

This loop will stop when `$i` is greater than 5 and less than 10.

It seems like the explanations in each section are indeed concise, and adding more detail could enhance understanding. Here’s an expanded version that clarifies the differences between `while`, `for`, and `foreach` loops with a bit more explanation.

---

### Differences in How While, For, and Foreach Work

Now, let’s explore the differences between `while`, `for`, and `foreach` loops in Perl. Although all three serve to repeat blocks of code, they do so in different ways, with each loop type having specific use cases depending on what you need.

#### While Loop
The `while` loop is highly flexible because it checks the condition at the start of every iteration. It’s best suited when you don’t know exactly how many times the loop should run, or when the loop needs to keep running until a condition changes.

For example, this `while` loop will keep printing numbers from 1 to 5:

```perl
my $i = 1;
while ($i <= 5) {
    print "$i\n";
    $i++;
}
```

Here, the condition `($i <= 5)` is evaluated before each iteration. If it’s true, the loop will continue. Once `$i` exceeds 5, the condition becomes false, and the loop stops.

The `while` loop is often used for scenarios where the termination condition isn’t predetermined. For instance, when waiting for user input:

```perl
my $input;
while ($input ne 'exit') {
    $input = <STDIN>;
    chomp($input);
    print "You entered: $input\n";
}
```

In this example, the loop will keep running until the user types `'exit'`.

##### Example 2: Summing Even Numbers
Here’s another case where we use `while` to sum even numbers up to 20:

```perl
my $sum = 0;
my $i = 2;
while ($i <= 20) {
    $sum += $i;
    $i += 2;
}
print "Total sum of even numbers: $sum\n";
```

In this example, the loop increments `$i` by 2 each time, ensuring only even numbers are added to `$sum`. The loop ends once `$i` exceeds 20.

#### For Loop
The `for` loop is generally used when you know beforehand how many iterations the loop should go through. This type of loop has three main parts: initialization, condition, and increment. It’s particularly useful when dealing with a fixed range or a known number of iterations.

For example, to print numbers from 1 to 5:

```perl
for (my $i = 1; $i <= 5; $i++) {
    print "$i\n";
}
```

Here, `$i` starts at 1, and the loop runs as long as `$i` is less than or equal to 5. After each iteration, `$i` is incremented by 1. This type of loop is compact and effective when you know the exact range of values.

##### Example 2: Summing Numbers from 1 to 10
This loop sums the numbers from 1 to 10:

```perl
my $total = 0;
for (my $i = 1; $i <= 10; $i++) {
    $total += $i;
}
print "Total: $total\n";
```

In this case, the loop adds each number from 1 to 10 to `$total`. Since the number of iterations is known in advance, a `for` loop is the natural choice.

##### Example 3: Printing Multiples of 3
Here’s an example where we print multiples of 3 from 3 to 30:

```perl
for (my $i = 3; $i <= 30; $i += 3) {
    print "$i\n";
}
```

The loop starts at 3 and increments `$i` by 3 with each iteration, printing the current value of `$i`. Again, since the number of iterations is fixed, the `for` loop is ideal.

#### Foreach Loop
The `foreach` loop is designed specifically for iterating over collections such as arrays or lists. It’s especially useful when you need to perform the same operation on each element of an array without worrying about the index or length of the array.

For instance, to print all names from an array:

```perl
my @names = ('Alice', 'Bob', 'Charlie');
foreach my $name (@names) {
    print "$name\n";
}
```

In this case, the loop automatically extracts each element from the `@names` array and assigns it to the `$name` variable, one at a time. This makes `foreach` a clean and easy way to work with lists.

##### Example 2: Calculating Length of Each Name
Let’s calculate the length of each name in the array:

```perl
my @names = ('Alice', 'Bob', 'Charlie');
foreach my $name (@names) {
    print "Length of $name: ", length($name), "\n";
}
```

Here, the loop iterates over each name in `@names` and prints the length of each one using Perl’s `length` function.

##### Example 3: Adding a Suffix to Array Values
Finally, let’s say we want to print scores from an array with a custom suffix:

```perl
my @scores = (90, 80, 70);
foreach my $score (@scores) {
    print "Score: $score points\n";
}
```

In this example, the `foreach` loop goes through each score in the array and prints it with the suffix "points." This loop is particularly useful when working with data collections like arrays or lists.

---

### Summary of Differences

- **While Loop:** Best used when the number of iterations isn’t known, and the loop should run until a condition changes.
  
- **For Loop:** Ideal when you know exactly how many iterations are needed, such as counting through a range of numbers.
  
- **Foreach Loop:** Tailored for iterating through arrays or lists, allowing you to easily access and manipulate each element.

By understanding the differences and use cases for each type of loop, you can choose the right one depending on the task at hand.
