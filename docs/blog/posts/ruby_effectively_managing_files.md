---
date: 2023-05-18 
categories:
  - Devlog
tags:
  - ruby
  - learning
---

# Effectively Managing Files
#### In the Terminal Using Ruby

Ruby is not only popular as a programming language for application development but also quite powerful for automation tasks in the terminal (as far as I know from the book I read, like Python, you know). Here’s a little useful guide to using one-liner Ruby commands that can help us work efficiently in the terminal. <!-- more -->

### Moving Files with Similar Names Using Ruby

Suppose you have several files with similar names like `app01.rb`, `app02.rb`, and so on. You want to move all of them to a specific directory. Typically, you would use the wildcard `*` with the `mv` command in the terminal, but Ruby can also accomplish this with additional flexibility.

Here’s a one-liner Ruby command to move all files starting with "app" and ending with ".rb" to the target directory:

```bash linenums="1"
ruby -e 'Dir.glob("app*.rb") { |file| FileUtils.mv(file, "/path/to/target") }' -r fileutils
```

**Explanation:**

- `-e` allows you to provide a line of Ruby code to be executed. It enables you to run Ruby commands directly from the command line without needing to create a separate script file.
- `Dir.glob("app*.rb")` searches for all files matching the pattern "app*.rb".
- `FileUtils.mv(file, "/path/to/target")` moves the found files to the target directory (`/path/to/target`).
- `-r fileutils` imports the required `FileUtils` module for the `mv` operation.

### Replacing Text in a File Easily

Sometimes, you need to replace specific text within a file. This command allows you to perform search and replace directly in the file without opening an editor:

```bash linenums="1"
ruby -i -pe '$_.gsub!(/old/, "new")' file.txt
```

**Explanation:**

- `-i` tells Ruby to edit the file in place.
- `-p` processes each line in the file.
- `$_` is a Ruby variable that contains the current line’s content.
- `gsub!(/old/, "new")` replaces all occurrences of the text "old" with "new" in each line.

### Counting the Number of Lines in a File

Want to know how many lines are in a file without using `wc -l`? Use this Ruby command:

```bash linenums="1"
ruby -ne 'END { puts $. }' file.txt
```

**Explanation:**

- `-n` tells Ruby to read the file line by line.
- `$.` is a Ruby variable that holds the count of the lines read.

### Sorting and Removing Duplicates from Text Files

If you want to sort and remove duplicates in a single line from a file, this command can help:

```bash linenums="1"
ruby -ne 'puts $_.chomp.split.uniq.sort.join(" ")' file.txt
```

**Explanation:**

- `chomp` removes the newline character from the end of each line.
- `split` breaks the line into words.
- `uniq` removes duplicate elements, and `sort` arranges the remaining elements.
- `join(" ")` combines the processed words back into a single line.

### Finding Specific Patterns in a File (Similar to Grep)

To search for lines in a file that match a specific pattern, use this command:

```bash linenums="1"
ruby -ne 'puts $_ if /pattern/' file.txt
```

**Explanation:**

- The regex `/pattern/` looks for matches in each line.
- `puts $_` prints the matching lines.

### Displaying a List of Large Files in a Directory

If you want to find files larger than 5 MB in a specific directory, use this code:

```bash linenums="1"
ruby -e 'Dir.glob("*").each { |f| puts f if File.size(f) > 5 * 1024 * 1024 }'
```

**Explanation:**

- `Dir.glob("*")` searches for all files in the current directory.
- `File.size(f)` returns the size of the file in bytes.
- Files larger than 5 MB will be printed in the terminal.

### Counting the Number of Words in a File

To count the total number of words in a file, Ruby can do this quickly:

```bash linenums="1"
ruby -ne 'END { puts $total_words } ; $total_words = 0; $total_words += $_.split.size'
```

**Explanation:**

- `split.size` counts the number of words in each line.
- `$total_words` is an accumulator variable that adds up the total word count from each line.

---

Ruby’s versatility makes it a great choice for both simple and complex automation tasks.
