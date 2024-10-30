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

When it comes to scripting in the terminal, programmers generally rely on `Bash`, `Zsh`, or other `shell-scripts`. However, since I haven’t thoroughly learned those languages yet, and just a few basic commands would make my work in the terminal faster (pardon my laziness), I decided to use **Python** as my main scripting language. Initially, **Python** seemed like a solid choice for me. The syntax is flexible, and it has a rich ecosystem. But as time passed, I started to feel uncomfortable scripting with **Python**. Not because of the syntax or the ecosystem, but for some *ridiculous* reasons—like the name and the logo of the snake just didn’t sit well with me. As you know, ***“I’m not a fan of reptiles.”*** Perhaps that’s what made me uncomfortable; it feels like I’m scripting with a serpent, and I feel like I’m in the jungle being chased by a monster! Haha!<!-- more -->

After some reflection, I decided to search for another scripting language to replace **Python**. Do you remember when I said that **Perl** might be good for scripting? Then I tried using it as my main scripting language. As you know, in my previous posts, I used **Perl** as the main subject because I was indeed learning it, right? However, as I delved deeper into its documentation, I realized that the language has complicated and unusual conventions. Moreover, **Perl** is outdated and hasn’t evolved much these days. I learned the basics, but I felt that spending more time on something that isn’t widely used today would only waste my time. Ultimately, I thought it would be better to go back and dive deeper into **Python** rather than invest time in **Perl**.

Next, I turned to **Lua**. I really enjoyed this language; it’s ***lightweight***, ***fast***, and has a logo I find appealing. Many *well-known programmers* use Lua, but it isn’t versatile enough and has a relatively small community. I wanted something at least comparable to **Python** but not **JavaScript**, I only use **JavaScript** for web development—no way I’m using it for everything else, especially not for automating tasks in my Lx-Local Machine.

Then **Ruby** appeared as the answer. Its syntax is very easy to read, and the community is substantial—especially with the popularity of **Ruby on Rails**. Plus, I love the name and its logo. **Ruby** felt like the perfect combination to meet my scripting needs.

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
**Ruby** for me, offers a clean syntax and a supportive ecosystem, allowing me to focus on completing automation tasks without getting bogged down in the complexities of other languages. This is the step I’ve taken to enhance my productivity and enjoy the process of learning a programming language that I genuinely like.
