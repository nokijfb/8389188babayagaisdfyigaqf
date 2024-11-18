---
date: 2023-05-15 
categories:
  - Devlog
tags:
  - python
  - learning
---

# PythonSL
#### The Scripting Choice for My LxMachine

When it comes to scripting in the terminal, programmers generally rely on Bash, Zsh, or other shell scripts. However, since I haven’t thoroughly learned those languages yet and have only picked up a few basic commands to make my work in the terminal faster (pardon my laziness), I initially chose Perl as my main scripting language. As I started using it, I found Perl's syntax confusing and its conventions unusual. Ultimately, I realized that spending time on something that is both confusing and obsolete would only waste my time.<!-- more -->

Next, I turned to **Lua**. I really enjoyed this language; it’s ***lightweight***, ***fast***, and has a logo I find appealing. Many well-known programmers use Lua, but it isn’t versatile enough and has a relatively small community. I wanted something at least comparable to **Perl** but not **JavaScript**—I only use JavaScript for web development, so there was no way I would use it for scripting.

Eventually, I decided to turn back to Python. Despite my initial discomfort with its name and logo (I’m not a fan of reptiles), I know that Python’s versatility and the vast ecosystem available make it an excellent choice for a variety of tasks. The syntax is clean and straightforward, making it easy to read and write scripts. 

### Core Modules in Python for Terminal Scripting

Before diving into libraries, let’s explore some **core modules** in Python that provide essential functionality for automating tasks in the terminal. These modules allow us to manipulate files, run system commands, and handle time-based tasks directly without the need for external libraries.

1. **os**
   The `os` module offers a way to interact with the operating system, including running system commands and managing processes.

   ```python linenums="1"
   import os
   os.system("echo Hello from Python!")
   ```

   - **Using `os.popen()`**: Runs a command and captures the output.

   ```python linenums="1"
   output = os.popen('ls -la').read()
   print(output)
   ```

   - **Exiting the Program**: Use `os._exit()` to exit the program with a specified status code.

   ```python linenums="1"
   os._exit(1)  # Exits with a status of 1 indicating failure
   ```

2. **shutil**
   The `shutil` module simplifies file and directory operations, such as copying, moving, and deleting.

   ```python linenums="1"
   import shutil
   shutil.copy('source.txt', 'destination.txt')
   ```

3. **subprocess**
   The `subprocess` module allows you to spawn new processes, connect to their input/output/error pipes, and obtain their return codes.

   ```python linenums="1"
   import subprocess
   result = subprocess.run(['ls', '-la'], stdout=subprocess.PIPE)
   print(result.stdout.decode())
   ```

4. **time**
   The `time` module provides various time-related functions. This is useful for delays or scheduling tasks.

   ```python linenums="1"
   import time
   print("Starting task...")
   time.sleep(3)  # pauses for 3 seconds
   print("Task completed!")
   ```

5. **datetime**
   The `datetime` module is essential for working with dates and times.

   ```python linenums="1"
   from datetime import datetime
   current_time = datetime.now()
   print(f"Current time: {current_time}")
   ```

6. **sys**
   The `sys` module provides access to some variables used or maintained by the interpreter and to functions that interact with the interpreter.

   ```python linenums="1"
   import sys
   print(sys.version)  # Prints the Python version
   ```

7. **json**
   The `json` module makes it easy to work with JSON data.

   ```python linenums="1"
   import json
   data = json.loads('{"status": "ok"}')
   print(data["status"])
   ```

8. **csv**
   The `csv` module provides functionality for reading and writing CSV files.

   ```python linenums="1"
   import csv
   with open('log.csv', mode='r') as file:
       reader = csv.reader(file)
       for row in reader:
           print(row)
   ```

---

Python, for me, offers a clean syntax and a supportive ecosystem, allowing me to focus on completing automation tasks without getting bogged down in the complexities of other languages. This is the step I’ve taken to enhance my productivity and enjoy the process of learning a programming language that I genuinely like.
