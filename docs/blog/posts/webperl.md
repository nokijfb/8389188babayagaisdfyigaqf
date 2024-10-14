---
date: 2023-04-23
categories:
  - Devlog
tags:
  - perl
  - learning
---

# Perl Webdev

There are various frameworks that help developers create web applications. One popular framework among Perl developers is Dancer2. This framework offers a clean and easy-to-understand syntax, along with a comprehensive set of features to quickly and efficiently build web applications.<!-- more -->
 This article aims to discuss the steps involved in building a simple web application using Dancer2 and setting up an isolated environment using Carton, a dependency management tool for Perl.

###Why Choose Dancer2?
Dancer2 is an excellent choice for Perl developers looking to create web applications for several reasons:
1. **Simplicity and Lightness**: Dancer2 has a minimalist design that allows developers to focus on application logic without getting bogged down in complex configurations.
2. **REST Support**: This framework makes it easy to create RESTful APIs, which are crucial in modern application development.
3. **Strong Ecosystem**: Dancer2 has numerous plugins and modules available for enhancing application functionality.

###Environment Setup
Before diving into application development, make sure you have Perl installed. Me personally use asdf to manage Perl versions, which makes it easy to switch between different programming languages. We'll also be using Carton to handle our project's dependencies.

###Installing Carton
To install Carton, you can use the following command:

```bash linenums="1"
cpanm Carton
```

Make sure you have `cpanm` installed beforehand. Carton will help us manage local project dependencies without interfering with global installations on the system.

###Creating a Web Application
Once Carton is installed, we are ready to create a simple web application. In this example, we will build an application that greets users with a given name.

###1. Creating a `cpanfile`
Create a file named `cpanfile` in your project directory and add the required dependencies:

```perl linenums="1"
requires 'Dancer2';
```

The `cpanfile` serves to define all the dependencies required by your project. Using Carton, we can install all dependencies defined in this file.

###2. Creating the Application File
Create a file named `app.pl` with the following content:

```perl linenums="1"
#!/usr/bin/env perl

use strict;
use warnings;
use Dancer2;

get '/' => sub {
    return 'Hello, World!';
};

get '/greet/:name' => sub {
    my $name = param('name');
    return "Hello, $name!";
};

start;
```

A brief explanation of the code above:
- **Shebang Line**: `#!/usr/bin/env perl` allows the script to be run using the Perl interpreter installed on the system.
- **Strict and Warnings**: These modules help catch errors in the code.
- **Routing**: Using `get` to define the routes that the application will handle. Here, we define two routes: one for the homepage (`/`) and one for greeting users based on the provided name (`/greet/:name`).

###3. Installing Dependencies
After creating the `cpanfile`, we need to install all the listed dependencies. Run the following command in the terminal:

```bash linenums="1"
carton install
```

This command will read the `cpanfile` and install all necessary modules into the local project folder.

###4. Running the Application
To run the application, use the following command:

```bash linenums="1"
carton exec perl app.pl
```

The application will run and can be accessed at `http://localhost:3000/`. If you access `http://localhost:3000/greet/name`, you will see the response "Hello, name!".

###Setting Up an Isolated Environment with Carton
One of the advantages of using Carton is its ability to manage project dependencies without interfering with global installations. This is particularly useful when working on multiple projects with different dependencies. With Cart

on, all required dependencies will be stored within the project folder, keeping the development environment clean and organized.

###Steps to Create an Isolated Environment
1. **Create a `cpanfile`**: Add all the required dependencies to the `cpanfile`.
2. **Install Dependencies**: Run the command `carton install` to install all listed dependencies.
3. **Run the Application with Carton**: Use `carton exec perl app.pl` to ensure that all installed dependencies are used when running the application.

---
You can easily build well-organized and isolated web applications. Properly managing dependencies in application development provides a solid foundation for building more complex web applications in the future (from what I've learned so far). This is just a part of my practical implementation of learning the Perl language.
