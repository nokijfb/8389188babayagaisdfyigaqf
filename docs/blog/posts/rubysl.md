---
date: 2023-05-15 
categories:
  - Devlog
tags:
  - ruby
  - learning
---

# RubySL
#### The Scripting Choice for my LxMachine

When it comes to scripting in the terminal, programmers generally rely on `Bash`, `Zsh`, or other `shell-scripts`. However, since I haven’t thoroughly learned those languages yet, and just a few basic commands I've Learned to make my work in the terminal faster (pardon my laziness), I decided to use **Python** as my main scripting language. Initially, **Python** seemed like a solid choice for me. The syntax is flexible, and it has a rich ecosystem. But as time passed, I started to feel uncomfortable scripting with **Python**. Not because of the syntax or the ecosystem, but for some *ridiculous* reasons—like the name and the logo of the snake just didn’t sit well with me. As you know, ***“I’m not a fan of reptiles.”*** Perhaps that’s what made me uncomfortable; it feels like I’m scripting with a serpent, and I feel like I’m in the jungle being chased by a monster! Haha!<!-- more -->

After some reflection, I decided to search for another scripting language to replace **Python**. Do you remember when I said that **Perl** might be good for scripting? Then I tried using it as my main scripting language. As you know, in my previous posts, I used **Perl** as the main subject because I was indeed learning it, right? However, as I delved deeper into its documentation, I realized that the language has complicated and unusual conventions. Moreover, **Perl** is outdated and hasn’t evolved much these days. I learned the basics, but I felt that spending more time on something that isn’t widely used today would only waste my time. Ultimately, I thought it would be better to go back and dive deeper into **Python** rather than invest time in **Perl**.

Next, I turned to **Lua**. I really enjoyed this language; it’s ***lightweight***, ***fast***, and has a logo I find appealing. Many *well-known programmers* use Lua, but it isn’t versatile enough and has a relatively small community. I wanted something at least comparable to **Python** but not **JavaScript**, I only use **JavaScript** for web development—no way I’m using it for everything else, especially not for automating tasks in my Lx-Local Machine.

Then **Ruby** appeared as the answer. Its syntax is very easy to read, and the community is substantial—especially with the popularity of **Ruby on Rails**. Plus, I love the name and its logo. **Ruby** felt like the perfect combination to meet my scripting needs.

Baik, berikut adalah penambahan detail untuk setiap modul inti yang akan memberikan pembaca gambaran lengkap tentang penggunaannya untuk scripting di terminal.


### Core Modules in Ruby for Terminal Scripting

Before jumping into libraries, let’s explore some **core modules** in Ruby that provide essential functionality for automating tasks in the terminal. These modules allow us to manipulate files, run system commands, and handle time-based tasks directly without the need for external libraries.

1. **Kernel**  
   The `Kernel` module offers crucial built-in methods for system operations, process management, and general-purpose functions used frequently in scripting. Here are the most relevant commands:

   - **`system`**: Runs a system command directly from Ruby, displaying the output in real-time.
     ```ruby linenums="1"
     system("echo Hello from Ruby!")
     ```

   - **Backticks (\`\` `)**: Runs a command and captures the output as a string, often useful for storing or processing the result.

     ```ruby linenums="1"
     output = `ls -la`
     puts output
     ```

   - **`exec`**: Executes a command and completely replaces the Ruby process with the new one. This is used for cases when no further Ruby code should run after the command.
     ```ruby linenums="1"
     exec("echo This replaces the Ruby process")
     ```

   - **`sleep`**: Pauses execution for a specified amount of time, commonly used in scripting for delays or timing control.
     ```ruby linenums="1"
     puts "Starting task..."
     sleep(3) # pauses for 3 seconds
     puts "Task completed!"
     ```

   - **`exit`**: Exits the program with a specified status code, commonly used in shell scripts for signaling success (0) or failure (non-zero).
     ```ruby linenums="1"
     exit(1) # Exits with a status of 1 indicating failure
     ```
     
2. **File**  
   The `File` module is fundamental for handling file operations, such as reading, writing, or modifying files in the system, making it ideal for automation scripts that need file manipulation.

   - **Reading and Writing Files**:
     ```ruby linenums="1"
     File.write("example.txt", "Hello, File!") # Writes content to a file
     content = File.read("example.txt") # Reads the file's content
     puts content
     ```

   - **Appending to a File**: Adds new content to the end of an existing file.
     ```ruby linenums="1"
     File.open("example.txt", "a") { |file| file.puts("More content") }
     ```

   - **Checking File Existence**: Ensures actions only occur if the file is present.
     ```ruby linenums="1"
     if File.exist?("example.txt")
       puts "File exists!"
     end
     ```

3. **Dir**  
   The `Dir` module provides functionality for working with directories, such as creating new directories, listing files, or setting the working directory.

   - **Creating a Directory**:
     ```ruby linenums="1"
     Dir.mkdir("new_directory") unless Dir.exist?("new_directory")
     ```

   - **Listing Files**: Shows all files and folders within a directory.
     ```ruby linenums="1"
     files = Dir.entries(".") # Current directory
     files.each { |file| puts file }
     ```

   - **Changing Directory**:
     ```ruby linenums="1"
     Dir.chdir("/path/to/directory") do
       puts Dir.pwd # Prints current working directory
     end
     ```

4. **Time**  
   The `Time` module provides capabilities for tracking and manipulating time and dates. This is useful for tasks that involve logging, scheduling, or time-based automation.

   - **Current Time and Formatting**:
     ```ruby linenums="1"
     current_time = Time.now
     puts "Current time: #{current_time}"
     puts "Formatted time: #{current_time.strftime("%Y-%m-%d %H:%M:%S")}"
     ```

   - **Time Calculations**: Adding or subtracting time, such as scheduling tasks.
     ```ruby linenums="1"
     one_hour_later = Time.now + 3600 # 3600 seconds = 1 hour
     puts "One hour later: #{one_hour_later}"
     ```

5. **ENV**  
   The `ENV` module gives access to environment variables, which are essential for passing configuration details to scripts without hardcoding them.

   - **Retrieving an Environment Variable**:
     ```ruby linenums="1"
     puts ENV["HOME"] # Outputs the home directory
     ```

   - **Setting an Environment Variable**:
     ```ruby linenums="1"
     ENV["MY_VAR"] = "my_value"
     puts ENV["MY_VAR"]
     ```

6. **Process**  
   The `Process` module enables you to work directly with system processes, spawn new ones, or retrieve their statuses, making it particularly useful for more complex task automation and process management.

   - **Starting and Managing Processes**:
     ```ruby linenums="1"
     pid = Process.spawn("sleep 5")
     Process.detach(pid) # Allows the process to run independently
     ```

   - **Process Information**: Accessing the process ID, parent process ID, or even killing processes.
     ```ruby linenums="1"
     puts Process.pid # Current Ruby process ID
     puts Process.ppid # Parent process ID
     Process.kill("TERM", pid) # Terminates a process by its ID
     ```

7. **Math**  
   The `Math` module provides basic mathematical functions, which can come in handy for scripting calculations or generating values.

   ```ruby linenums="1"
   puts Math.sqrt(16) # Calculates square root
   puts Math.sin(Math::PI / 4) # Trigonometric functions
   ```

These core modules provide powerful, built-in capabilities for writing efficient and effective terminal scripts in Ruby. This foundation equips us to handle a wide range of system tasks directly, and with these basics covered, we’re ready to move on to libraries that extend these functionalities even further.


### Key Libraries for Scripting in Ruby

After choosing **Ruby** as my scripting language, I began exploring useful libraries for automating tasks on Linux. Here are some libraries that I found incredibly helpful:

1. **FileUtils**: Simplifies file and directory management, such as copy, move, or delete, similar to basic commands in Bash.
   ```ruby linenums="1"
   require 'fileutils'
   FileUtils.cp('source.txt', 'destination.txt')
   ```

2. **Open3**: Useful for executing system commands and capturing their output and errors.
   ```ruby linenums="1"
   require 'open3'
   stdout, stderr, status = Open3.capture3('systemctl status nginx')
   ```

3. **Optparse**: Allows **Ruby** scripts to accept input from the command line, making them more interactive.
   ```ruby linenums="1"
   require 'optparse'
   options = {}
   OptionParser.new do |opts|
     opts.on("-r", "--restart", "Restart service") { |n| options[:restart] = n }
   end.parse!
   ```

4. **Net::HTTP**: For accessing APIs or making HTTP requests.
   ```ruby linenums="1"
   require 'net/http'
   uri = URI('https://example.com/status')
   response = Net::HTTP.get(uri)
   ```

5. **Logger**: Facilitates clean and consistent logging.
   ```ruby linenums="1"
   require 'logger'
   logger = Logger.new('logfile.log')
   logger.info("Service restarted successfully.")
   ```

6. **YAML and JSON**: Useful for storing and reading data in configuration formats.
   ```ruby linenums="1"
   require 'yaml'
   config = YAML.load_file('config.yml')
   require 'json'
   data = JSON.parse('{"status": "ok"}')
   ```

7. **Pathname**: Simplifies path file management.
   ```ruby linenums="1"
   require 'pathname'
   path = Pathname.new('/home/user')
   path.join('scripts', 'automation.rb')
   ```

8. **Shellwords**: Helps with parsing and sanitizing shell arguments.
   ```ruby linenums="1"
   require 'shellwords'
   args = Shellwords.split('ls -la /home/user')
   ```

9. **CSV**: Eases the management of data in CSV format.
   ```ruby linenums="1"
   require 'csv'
   CSV.foreach("log.csv") { |row| puts row }
   ```

10. **ERB**: Allows for dynamic template creation, useful for generating reports or configurations.
    ```ruby linenums="1"
    require 'erb'
    template = ERB.new("Status: <%= status %> at <%= Time.now %>")
    puts template.result(binding)
    ```

### Additional Libraries for Scripting

In addition to the libraries above, here are some extra ones that are also useful:

1. **StringIO**: Allows using strings as files.
   ```ruby linenums="1"
   require 'stringio'
   output = StringIO.new
   output.puts "Hello, World!"
   puts output.string
   ```

2. **Tempfile**: Creates temporary files that are automatically deleted after use.
   ```ruby linenums="1"
   require 'tempfile'
   Tempfile.create('my_temp_file') do |temp_file|
     temp_file.write("Hello, Tempfile!")
     puts temp_file.read
   end
   ```

3. **Popen3**: Runs shell commands and accesses stdin, stdout, and stderr.
   ```ruby linenums="1"
   require 'open3'
   Open3.popen3('ls') do |stdin, stdout, stderr, thread|
     puts stdout.read
   end
   ```

4. **Rake**: A task automation tool for organizing and running automation tasks.
   ```ruby linenums="1"
   require 'rake'
   task :hello do
     puts "Hello, Rake!"
   end
   Rake::Task[:hello].invoke
   ```

5. **Shell Executor**: Executes shell commands and manages output.
   ```ruby linenums="1"
   output = `ls -la`
   puts output
   ```

---

### Shell Executor: Advanced Examples

1a. **Piping Commands**  
   You can use piping (`|`) to pass the output of one command as input to another.

   ```ruby linenums="1"
   output = `ps aux | grep ruby`
   puts "Processes running Ruby:\n#{output}"
   ```

2b. **Redirecting Output to a File**  
   Save the output of a command to a file for later use or logging.

   ```ruby linenums="1"
   `ls -la > output.txt`
   puts "Output saved to output.txt"
   ```

3c. **Combining Commands with Conditional Execution (`&&` or `||`)**  
   Run multiple commands conditionally, such as executing the second command only if the first succeeds.

   ```ruby linenums="1"
   result = `mkdir new_folder && cd new_folder && touch example.txt`
   puts "Commands executed successfully; file created in new_folder" if $?.success?
   ```

4d. **Running Background Tasks**  
   Add `&` at the end of a command to run it in the background.

   ```ruby linenums="1"
   `sleep 5 &`
   puts "The sleep command is now running in the background"
   ```

5e. **Capturing Exit Status**  
   In addition to the output, you can capture the exit status of the last command to check if it succeeded or failed.

   ```ruby linenums="1"
   `invalid_command`
   if $?.exitstatus != 0
     puts "Command failed with status: #{$?.exitstatus}"
   else
     puts "Command executed successfully"
   end
   ```

6f. **Using Backticks with Interpolation**  
   Embed Ruby variables directly into a command.

   ```ruby linenums="1"
   directory = "/home/user"
   output = `ls -la #{directory}`
   puts "Contents of #{directory}:\n#{output}"
   ```

7g. **Storing Command Output in Arrays**  
   Split command output into an array, making it easy to iterate over and manipulate.

   ```ruby linenums="1"
   files = `ls -1`.split("\n") # -1 flag lists files line by line
   puts "Files in the directory:"
   files.each { |file| puts "- #{file}" }
   ```

---
**Ruby** for me, offers a clean syntax and a supportive ecosystem, allowing me to focus on completing automation tasks without getting bogged down in the complexities of other languages. This is the step I’ve taken to enhance my productivity and enjoy the process of learning a programming language that I genuinely like.
