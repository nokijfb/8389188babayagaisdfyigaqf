---
date: 2023-05-14 
categories:
  - Devlog
tags:
  - perl
  - learning
---

# Variabel Scope
#### THE CASE of THE MASKED `$count`

As usual, I’m conducting experiments with Perl. This time, I’m focusing on how variables declared with `my` behave when used in different contexts. During this experimentation, I encountered an interesting warning when trying to redeclare a variable with the same name. This raised the question: *Will redeclaring a variable give me an error?, and what impact does it have on my code?*<!-- more -->

### Foreach Loop with `say`

I started with a simple experiment to print a list of numbers using a `foreach` loop and the `say` feature. In the context of Perl, `use feature 'say';` is used to enable the `say` feature, which is a function for printing output that automatically appends a newline (`\n`) at the end, making it simpler than `print`. **`feature`** is a module in Perl that allows users to access new and experimental features of the language. There’s a subtle difference between `say` and `print` in Perl. Both are used for outputting values, but `say` automatically adds a newline at the end of its output, while `print` does not, so we need to manually add a newline if we’re using `print`. Additionally, there’s also `printf`, which is used for printing values in a formatted way, but in this experiment, I focused on `say` and `foreach` due to their ease of use in outputting values in a cleaner manner.

Here’s the initial snippet of code I created:

```perl
#!/usr/bin/env perl
use strict;
use warnings;
use feature 'say';

my @numbers = (1,2,3,4,5);
foreach my $count(@numbers){
    say $count;
}
say "-----------------------------";

my @numbers_2 = (1,2,3,4,5);
foreach my $count(@numbers_2){
    say $count;
}
```

Everything worked perfectly here. I declared two arrays, `@numbers` and `@numbers_2`, and printed their contents using `foreach`. What’s interesting is that even though the variable `$count` was used in both loops, there were no issues. This is because `my $count` is scoped only to the loop it resides in, so the two `$count` declarations remain separate and do not conflict with each other.

### Masking or Overriding Declarations?

After trying out a few things with `foreach`, I wanted to perform an additional experiment by declaring the variable `$count` after both loops. I was curious to see what would happen if I redeclared the same variable using `my`:

```perl
my $count = 12;
my $count = 13;
```

When this code was executed, I received the following warning:

```
"my" variable $count masks earlier declaration in same scope at app01.pl line 19
```

This was intriguing! It turned out that the second declaration of `$count` on line 19 masked the first declaration on line 18. Perl alerted me that, although both variables were in the same scope, the newer declaration obscured the older one, meaning that the value of `$count = 12` on line 18 could no longer be accessed after line 19.

### What Does This Warning Mean?

The warning **"my" variable $count masks earlier declaration in same scope** indicates that the second declaration of the variable `$count` is 'masking' the first one. Both variables are in the same scope, which is the global level of the program, so after the second declaration, the `$count` variable from the first declaration (with value `12`) is no longer accessible because it has been overridden by the second declaration (with value `13`).

Despite this warning, the program continued to run since it was only a warning and not a fatal error. The code preceding line 18 still executed without issues, including the `foreach` loops that utilized `$count` earlier.

### Are the Variables on Lines 18 and 19 Different?

Technically, the variables on lines 18 and 19 refer to the same variable within the same scope. However, when we redeclare a variable with `my`, the new declaration effectively overrides the previous one, making the variable with value `12` on line 18 inaccessible after the declaration on line 19.

### Does the Code Before Line 18 Still Run?

Yes, the code before line 18 runs as expected. The `foreach` loops at the beginning of the program print the numbers from the `@numbers` and `@numbers_2` arrays without any issues. This warning only affects the declaration of the `$count` variable in the global context after the loops.

---
In this experiment, I discovered that redeclaring a variable with `my` in the same scope is unnecessary and can lead to a "masking" warning. While the program continues to function, redeclaring a variable will obscure the previous declaration, making the code less clear. This warning serves as a reminder that it’s better to avoid redeclaring variables in the same scope, especially if we only want to change their values. 

In contrast to some other programming languages, where redeclaring a variable can lead to an error or even cause the program to terminate (for example like in Javascript, Go, and others), Perl allows this but still raises a warning, To me, this feels weirder than it is flexible.
