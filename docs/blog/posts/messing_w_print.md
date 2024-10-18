---
date: 2023-05-06
categories:
  - Devlog
tags:
  - perl
  - learning
---

# Messing w/ `print`
#### DEBUGGING AND LEARNING

Sometimes I mess around with Perl like this:

```perl linenums="1"
#!/usr/bin/env perl
use strict;
use warnings;

sub post {
    my ($a, $b) = @_;
    return $a + $b;
}

my throw_up = post(22, 33);
print(throw_up);
```
Just trying to write a simple script to sum two numbers and print the result.<!-- more --> Here’s what I started with ᕕ( ᐛ )ᕗ
When I ran that random script, I got this error:

```
No such class throw_up at app.pl line 11, near "my $throw_up"
syntax error at app.pl line 11, near "my $throw_up ="
Execution of app.pl aborted due to compilation errors.
```

I was a bit confused, So I looked carefully at the message, and turns out. The error was due to forgetting the dollar sign (`$`) in front of my variable haha.. I forget that in Perl, variables need that `$` to show they’re scalars. So I fixed my code like this:

```perl linenums="1"
my $throw_up = post(22, 33);
print $throw_up;
```

That fixed the error, but I still had some questions in my mind, what if:

```perl linenums="1"
my $throw_up = 5;
print ($throw_up) + 2;
```

I got some warnings that made me scratch my head 🙆:

```
Useless use of addition (+) in void context at app.pl line 12.
```

The result is just `5`, I didn’t understand why the `+ 2` didn’t seem to change anything. I thought maybe printing `$throw_up` again would show that the addition somehow affected its value. So I ran this code:

```perl linenums="1"
print($throw_up, "\n") + 2;
print $throw_up, "\n";
```

The output still showed `5`, not `7`. It became clear that the addition was ignored, even after printing `$throw_up` again. Such a stupidity ଘ( ᐛ ) ଓ

To simplify things, I rewrote the code:

```perl linenums="1"
my $result = $throw_up + 2;
print $result, "\n";
```
And like this:

```perl linenums="1"
print $throw_up + 2, "\n";
```

And also like this:

```perl linenums="1"
print($throw_up + 2, "\n");
```

All of these work.

---
Remember about context, context, context...<br>
It's made clearer and easier to understand this wierdo language in my opinion ╮ (. ❛ ᴗ ❛.) ╭
