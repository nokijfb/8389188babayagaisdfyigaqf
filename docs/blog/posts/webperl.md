---
date: 2023-04-23
categories:
  - Devlog
tags:
  - perl
  - learning
---

# Perl Webdev
#### BUILD A WEBAPPS with `Perl`, `Dancer2`, AND `Carton`

In the Perl ecosystem, **Dancer2** is one of the most popular frameworks for building web applications due to its simplicity and flexibility. Coupled with **Carton**, which manages dependencies in an isolated environment, you can create scalable and organized web apps.<!-- more --> This article walks you through the process, ensuring your project structure is correct and maintainable

### Why Choose Dancer2?
Dancer2 stands out for several reasons:
1. **Minimal Configuration**: It's easy to set up and start developing immediately, letting you focus on building rather than configuring.
2. **Built-in Support for REST**: Building APIs or interacting with external systems is straightforward.
3. **Rich Plugin Ecosystem**: There’s an abundance of plugins to extend your app without extra complexity.

### Project Setup: Step-by-Step

#### 1. Create Your Project Directory
First, create a new directory for your project and move into it:
```bash linenums="1"
mkdir MyWebApp
cd MyWebApp
```

#### 2. Install Carton
Install Carton if it’s not already installed:
```bash linenums="1"
cpanm Carton
```

#### 3. Create a `cpanfile`
Within your project folder, create a file called `cpanfile` to define the dependencies for your app:
```perl linenums="1"
requires 'Dancer2';
```

This file will help Carton handle dependency management for your project.

#### 4. Install Dependencies
After setting up the `cpanfile`, install the defined dependencies with Carton:
```bash linenums="1"
carton install
```
This will install **Dancer2** and any related modules into the local project environment.

#### 5. Initialize Your Dancer2 Application
Now that Dancer2 is available locally, use it to initialize the project structure:
```bash linenums="1"
carton exec dancer2 -a MyWebApp
```
This command will generate a scaffold for your web application with directories such as:

- `bin/` contains the script to run your app.
- `lib/` your application logic.
- `views/` templates for rendering HTML.

#### 6. Basic Application Example
In the `bin/app.pl` file, you'll find a basic starter code. You can modify it like this to create a simple greeting app:
```perl linenums="1"
#!/usr/bin/env perl
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
This simple app provides two routes:
- `/` returns "Hello, World!"
- `/greet/:name` returns a personalized greeting.

#### 7. Run the Application
You can now run the app with Carton:
```bash linenums="1"
carton exec perl bin/app.pl
```
The app will run at `http://localhost:3000`. To test it, open a browser and visit:
- `http://localhost:3000/` for "Hello, World!"
- `http://localhost:3000/greet/YourName` for a personalized greeting.

### Managing Dependencies with Carton
Carton ensures that all dependencies are stored locally within the project. This prevents conflicts between different projects or system-level packages, keeping your environment clean. Each time you want to run or modify the app, use `carton exec` to ensure it uses the locally installed modules.

---
You can easily build well-organized and isolated web applications. Properly managing dependencies in application development provides a solid foundation for building more complex web applications in the future (from what I've learned so far). This is just a part of my practical implementation of learning the Perl language.
