---
date: 2023-05-10 
categories:
  - Devlog
tags:
  - perl
  - learning
---

# Loop Experiment
#### INFINITE LOOP AND SILENT CODE

I was experimenting with Perl again, as usual, filled with tons of "why" questions! This time, I stumbled upon a situation where I was just trying to print the elements of an array one by one, but somehow I got stuck in an infinite loop.<!-- more --> 

### The First Experiment: The Infinite Loop

Here's what I wrote initially:
```perl linenums="1"
my @numbers = (1,2,3,4,5,7,8,9);

while (my @count = shift @numbers){
    print "array @count";
}
```

At first, I thought, "Why is this running forever? What did I miss here?" Turns out, the issue came from how I used `shift`. I assumed that `shift` would pull one element from the array and assign it to `@count`, but Perl doesn't exactly work like that. 

#### Why Does This Happen?

`shift @numbers` pulls out **one element** from the array, not an array itself. It’s just a single scalar value, but I mistakenly stored it into `@count`, which is an array. The interesting thing is, when you treat a single scalar as an array, Perl doesn’t throw an error; it just kind of rolls with it. But this leads to a subtle problem. The array `@count` always exists, and in Perl, an array—even if it’s empty—is considered "true" in a logical sense. So the loop never gets a "false" signal to stop. Endless loop—boom! 

I was fascinated and kept wondering, "Why doesn’t Perl treat an empty array as false?" The more I dug into Perl’s logic, the more I realized that the language is quirky this way—it likes to keep things "true" until explicitly told otherwise.

### The Second Experiment: The Silent Code

So, after fixing that infinite loop, I ran into another curious case. This time, I wanted to see how the loop behaves when I include `0` in the array. Here’s what I did:

```perl linenums="1"
my @numbers = (0,1,2,3,4,5,6,7,8,9);

while (my $count = shift @numbers) {
    print "array $count\n";
    $count++;
}
```

Guess what? Nothing printed! Not a single "array 0" or anything else. And, of course, I had to ask myself again, **"Why is nothing showing up?**"

Turns out, in Perl, `0` is considered **false** in a boolean context. So, when `shift @numbers` pulls out that first `0`, the loop checks if `$count` is true. But since `0` is false, it breaks the loop right then and there! It didn’t even give the code a chance to print anything.

I started to ask myself, "Why does `0` have to be false? Why doesn’t Perl treat it like a valid number, regardless of its truthiness?" This led me to learn about how Perl (and many other languages) treats certain values (`0`, `undef`, etc.) as "falsy," which makes sense in most logical situations but can surprise you when you’re handling numbers directly.

### Postfix Increment Mystery

Finally, the third experiment involved something even more mysterious. I added a `postfix increment` (`$count++`) to the loop, expecting it to modify my numbers. But nothing seemed to change.

Here’s what I wrote:
```perl linenums="1"
my @numbers = (0,1,2,3,4,5,6,7,8,9);

while (defined(my $count = shift @numbers)) {
    print "array $count\n";
    $count++;
}
```

This time, the output started to work as expected, but I still wondered, **"Why doesn’t `$count++` seem to have any effect?**"

After some digging, I realized that the `postfix increment` increments `$count`, but only **after** it’s been used. So, even though I was adding 1, the value was already printed before the increment happened. To make it even more confusing, on the next iteration, `$count` would be overwritten by the next element from the array due to `shift`. The increment had no lasting impact because each loop just overwrote `$count` with the next array value! 

At this point, I started to understand why handling variables inside loops with these nuances can be tricky. Perl just kept giving me more "whys" to think about.


---
In the end, this whole experiment made me appreciate Perl’s quirky nature even more. It's a language where things like infinite loops, truthy/falsy values, and postfix increments can really make you stop and think. Every little behavior led me to ask more "why" questions, and that’s what keeps me hooked. Why does Perl handle arrays like this? Why does `0` stop the loop? Why didn’t `$count++` change my result?

It’s fun that with programming, the deeper you go, the more curious you become!
