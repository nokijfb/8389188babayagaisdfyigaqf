---
date:
  created: 2023-05-07 
  updated: 2023-08-25
categories:
  - Devlog
tags:
  - perl
  - rust
  - typescript
  - learning
---

# Enums
###### Post Updated: August 22, 2023
#### FROM CONFUSION TO CLARITY

So, there I was, scrolling through [*X*](https://x.com/88saiba) one lazy afternoon—just catching up on the usual memes, tech banter, and random thoughts—when I stumbled upon something oddly specific. It was a meme about `enums`. Yep, `enums`.<!-- more -->

Now, if you’ve ever watched *Tom and Jerry*, you know Tom, the cat, always finds himself in ridiculous situations. Well, this meme had two versions of *Tom: one looking like his usual clueless self*, labeled **“Enums in TypeScript”**, and *another flexing like a hero straight out of an action movie*, captioned **“Enums in Rust.”** Now, I hadn’t even heard about this comparison, but apparently, Rust’s `enums` are like a boss, and TypeScript’s, well… not so much.

That got me wondering: **What are enums from this perspective, anyway?**

#### So, What Are Enums?

**`Enums`** (short for ***enumerations***) are a way to define a set of fixed, predefined values. Sounds fancy, but let me break it down for you with a simple example.

Imagine you’re designing a traffic light system. The light can only be one of three colors: <b style="color:red">Red</b>, <b style="color:yellow">Yellow</b>, or <b style="color:green">Green</b>. There are no options for <b style="color:blue">Blue</b>, <b style="color:purple">Purple</b>, or anything else—just these three specific colors. Now, if you were to code this traffic light system, you’d need a way to ensure that only these valid colors can be used. How do you make sure no one accidentally selects <b style="color:blue">“Blue”</b> for the traffic light?

That’s where enums come in. Enums work like a menu of options, ensuring that you can only pick from the listed items. They lock in these choices so that if someone tries to use a color that doesn’t exist, like “Blue,” the code will raise an error or warning. This helps prevent mistakes and keeps the program running smoothly.

#### Let’s See It in Action (In Perl!)

Before diving into the meme-worthy battle between TypeScript and Rust, let’s first see how enums might work in Perl. Now, Perl doesn’t have enums built in, but you can use a module like `enum` to create a simple enum for our traffic light:

```perl linenums="1"
use enum qw(RED YELLOW GREEN);

my $light = RED;
if ($light == RED) {
    print "The light is red.\n";
}
```

Here, we’re defining an enum with three colors: `RED`, `YELLOW`, and `GREEN`. And then we check if the light is red. Simple, right? The enum ensures you can only use those three colors for the traffic light.

> The `qw` in Perl stands for ["quote words."](https://perldoc.perl.org/perlop#Quote-and-Quote-like-Operators) It allows you to create a list of strings without needing to individually quote each word. The words are separated by spaces, and `qw` automatically converts them into a list of quoted strings.

Enums have a wide range of applications across different programming scenarios.

Here maybe I'll give you a couple of additional examples that illustrate their versatility:

##### Order Status in an E-commerce Application

In an e-commerce application, you might want to track the status of customer orders. Using enums, you can define a set of possible order statuses, such as:

- **Pending**
- **Shipped**
- **Delivered**
- **Cancelled**

This helps ensure that the order status can only be one of the predefined values, making your code easier to read and reducing the chances of errors.

```perl linenums="1"
use strict;      # Enforces strict variable declaration rules
use warnings;    # Enables warnings to help catch potential issues
use enum qw(PENDING SHIPPED DELIVERED CANCELLED);  # Define an enum for order statuses

# Set the initial status of the order
my $order_status = PENDING;

# Check the order status and print a message accordingly
if ($order_status == SHIPPED) {
    print "Your order has been shipped.\n";  # Message if the order is shipped
} elsif ($order_status == DELIVERED) {
    print "Your order has been delivered.\n"; # Message if the order is delivered
} else {
    print "Your order is still pending.\n";    # Message if the order is still pending
}
```

##### User Roles in a Web Application

Another common use case for enums is defining user roles in a web application. This could include roles like:

- **Admin**
- **User**
- **Guest**

By using enums, you can ensure that the user role is always one of these predefined values, which helps maintain consistent access control throughout the application.

```perl linenums="1"
use strict;      # Enforces strict variable declaration rules
use warnings;    # Enables warnings to help catch potential issues
use enum qw(ADMIN USER GUEST);  # Define an enum for user roles

# Set the role of the current user
my $user_role = ADMIN;

# Check the user role and print a welcome message accordingly
if ($user_role == ADMIN) {
    print "Welcome, Admin! You have full access.\n";  # Message for admin users
} elsif ($user_role == USER) {
    print "Welcome, User! You have limited access.\n"; # Message for regular users
} else {
    print "Welcome, Guest! Please log in for more features.\n";  # Message for guests
}
```

##### Directions in a Game

In a gaming application, you might use enums to define possible movement directions for a character:

- **Up**
- **Down**
- **Left**
- **Right**

Using enums here makes the code cleaner and easier to maintain, as it restricts the possible movement options to just these four directions.

```perl linenums="1"
use strict;      # Enforces strict variable declaration rules
use warnings;    # Enables warnings to help catch potential issues
use enum qw(UP DOWN LEFT RIGHT);  # Define an enum for movement directions

# Set the movement direction
my $movement = UP;

# Check the movement direction and print a corresponding action
if ($movement == UP) {
    print "You move up!\n";    # Action for moving up
} elsif ($movement == DOWN) {
    print "You move down!\n";  # Action for moving down
} elsif ($movement == LEFT) {
    print "You move left!\n";  # Action for moving left
} else {
    print "You move right!\n"; # Action for moving right
}
```
<br>
#### Why Bother with Enums?

The cool thing about `enums` is that they make your code more reliable. Without `enums`, someone might try to set the traffic light to <b style="color: blue">“Blue”</b>, which doesn’t exist, and the system might break. With `enums`, you’re basically saying, “Hey, these are the only valid values”, and your code will warn you if you try anything else.

Now, let’s get to the fun part: how `enums` differ between **TypeScript** and **Rust**, as hinted by that ***Tom and Jerry*** meme.

#### Enums in TypeScript (Clueless Tom)

First up, TypeScript—our poor, confused Tom. TypeScript has enums, but they’re kind of basic. They get the job done, but they don’t offer much beyond the bare essentials. Here’s what an enum looks like in TypeScript for our traffic light:

```typescript linenums="1"
enum TrafficLight {
  Red = "RED",
  Yellow = "YELLOW",
  Green = "GREEN"
}

let currentLight: TrafficLight = TrafficLight.Red;
```

This code creates an enum with three possible values: `Red`, `Yellow`, and `Green`. You can assign one of these values to `currentLight`, and it works just fine. But that’s about it. TypeScript doesn’t force you to handle all possible values of the enum, so if you miss a case, well… clueless Tom strikes again.

#### Enums in Rust (Macho Tom)

Now, Rust’s enums are a whole different story—this is where Tom goes full macho mode. Rust’s enums are powerful and come with all sorts of features. Not only can you define a list of values, but you can also attach data to each value and force the code to handle every possible case.

Here’s the same traffic light example, but in Rust:

```rust linenums="1"
enum TrafficLight {
    Red,
    Yellow,
    Green,
}

let current_light = TrafficLight::Red;
```

At first glance, this might seem similar to TypeScript. But Rust’s strength shines when you have to work with these values. Rust’s enums come with a `match` statement that forces you to handle all possible values, so there’s no way to accidentally forget one (unlike TypeScript):

```rust linenums="1"
match current_light {
    TrafficLight::Red => println!("The light is red."),
    TrafficLight::Yellow => println!("The light is yellow."),
    TrafficLight::Green => println!("The light is green."),
}
```

If you leave out a case, Rust won’t even compile the code! It’s like Tom bulking up, making sure you don’t miss any important details in your code. It’s stricter, but that’s what makes Rust so reliable. The language doesn’t just let things slide like TypeScript sometimes does.

#### Why the Difference?

So, why does ***TypeScript’s*** enum feel like a confused Tom, while ***Rust’s*** is like a flexing **powerhouse**? The key difference lies in how strict and opinionated the languages are about data types and error handling.

TypeScript, being a "superset of JavaScript", was designed with flexibility in mind. It allows developers to write code quickly and iterate rapidly, which is great for prototyping and building applications in a fast-paced environment. However, this flexibility comes at a cost. TypeScript’s `enums`, while useful, don’t enforce strict rules around their usage. You can easily assign a value to an enum that isn't explicitly defined, which can lead to `unexpected behaviors` or `bugs` down the line. For example, if a developer mistakenly uses a string that doesn’t match any of the `enum` values, TypeScript won’t `throw` an `error` at compile time. Instead, it will *compile the code*, potentially causing `runtime issues` that can be ***hard to trace back to the source***.

On the other hand, Rust is designed with ***safety*** and ***precision*** at its core. It enforces `strict` type checking and ensures that all possible cases are handled explicitly in your code. When you define an `enum` in Rust, the language expects you to account for every possible variant when using that `enum`. If you fail to do so, Rust *won’t even compile* your code. This might seem `strict`, but it ultimately leads to more `robust` and `reliable` applications. The *emphasis* on `safety` means that common programming `errors—like` using an invalid `enum` value—are caught early in the development process, saving developers time and frustration later on.

Moreover, Rust’s `enums` come with additional features, such as the ability to *associate data with each variant*. This allows for more complex and expressive representations of data, making it easier to manage and reason about your code. For example, you can create an `enum` that holds not just the type of **traffic light** but also additional data like **the duration each light should stay on**. This level of detail helps developers create more powerful and flexible applications.

TypeScript’s more ***permissive approach*** makes it easier for developers to get started, but still it can lead to `subtle bugs` if *proper care* isn’t taken. Rust’s *strictness*, while potentially intimidating for newcomers, ensures a *higher level* of `reliability` and `safety` in the code. This difference in philosophy reflects the broader goals of the two languages: **TypeScript aims for ease of use and rapid development, while Rust prioritizes safety and performance**.

#### Enums in Other Languages

Just for fun, here’s how enums might look in other languages:

- **JavaScript:** No built-in enums here, but you can fake it with objects:
  ```javascript
  const TrafficLight = {
    Red: 'RED',
    Yellow: 'YELLOW',
    Green: 'GREEN'
  };

  let currentLight = TrafficLight.Red;
  ```

- **Perl:** As we saw earlier, Perl uses modules like `enum` to simulate enums:
  ```perl
  use enum qw(RED YELLOW GREEN);
  ```

#### So, Why Do Enums Matter?

At the end of the day, `enums` make your code `cleaner` and more `reliable`. They lock down which values are allowed and prevent unexpected inputs from sneaking in. Whether you’re using TypeScript’s more *relaxed* approach or Rust’s *stricter*, more powerful version, `enums` are a handy tool that makes your life easier as a programmer.

---
And next time you see a meme about enums—or find yourself coding up a traffic light—you’ll know exactly what they are and why they matter. Plus, you’ll understand why Tom’s always getting into these situations! ᕕ( ᐛ )ᕗ
