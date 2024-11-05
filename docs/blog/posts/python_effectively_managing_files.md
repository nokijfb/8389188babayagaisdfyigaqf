---
date: 2023-05-18 
categories:
  - Devlog
tags:
  - python
  - learning
---

# Effectively Managing Files
#### In the Terminal Using Python

Python is not only popular as a programming language for application development but also quite powerful for automation tasks in the terminal. Here’s a little useful guide to using one-liner Python commands that can help us work efficiently in the terminal.<!-- more -->

### Moving Files with Similar Names Using Python

Suppose you have several files with similar names like `app01.py`, `app02.py`, and so on. You want to move all of them to a specific directory. Typically, you would use the wildcard `*` with the `mv` command in the terminal, but Python can also accomplish this with additional flexibility.

Here’s a one-liner Python command to move all files starting with "app" and ending with ".py" to the target directory:

```bash linenums="1"
python -c 'import glob, shutil; [shutil.move(f, "/path/to/target") for f in glob.glob("app*.py")]'
```

**Explanation:**

- `-c` allows you to provide a line of Python code to be executed. It enables you to run Python commands directly from the command line without needing to create a separate script file.
- `glob.glob("app*.py")` searches for all files matching the pattern "app*.py".
- `shutil.move(f, "/path/to/target")` moves the found files to the target directory (`/path/to/target`).

### Replacing Text in a File Easily

Sometimes, you need to replace specific text within a file. This command allows you to perform search and replace directly in the file without opening an editor:

```bash linenums="1"
python -c 'import fileinput; [line.replace("old", "new") for line in fileinput.input("file.txt", inplace=True)]'
```

**Explanation:**

- `fileinput.input("file.txt", inplace=True)` reads the file and allows in-place editing.
- `line.replace("old", "new")` replaces all occurrences of the text "old" with "new" in each line.

### Counting the Number of Lines in a File

Want to know how many lines are in a file without using `wc -l`? Use this Python command:

```bash linenums="1"
python -c 'print(sum(1 for _ in open("file.txt")))'
```

**Explanation:**

- `sum(1 for _ in open("file.txt"))` counts the number of lines in the file.

### Sorting and Removing Duplicates from Text Files

If you want to sort and remove duplicates in a single line from a file, this command can help:

```bash linenums="1"
python -c 'print(" ".join(sorted(set(line.strip().split()) for line in open("file.txt"))))'
```

**Explanation:**

- `line.strip().split()` breaks the line into words and removes leading/trailing whitespace.
- `set()` removes duplicate elements, and `sorted()` arranges the remaining elements.
- `" ".join(...)` combines the processed words back into a single line.

### Finding Specific Patterns in a File (Similar to Grep)

To search for lines in a file that match a specific pattern, use this command:

```bash linenums="1"
python -c 'import sys; [print(line) for line in open("file.txt") if "pattern" in line]'
```

**Explanation:**

- The condition `if "pattern" in line` checks for matches in each line.
- `print(line)` prints the matching lines.

### Displaying a List of Large Files in a Directory

If you want to find files larger than 5 MB in a specific directory, use this code:

```bash linenums="1"
python -c 'import os; [print(f) for f in os.listdir() if os.path.isfile(f) and os.path.getsize(f) > 5 * 1024 * 1024]'
```

**Explanation:**

- `os.listdir()` searches for all files in the current directory.
- `os.path.getsize(f)` returns the size of the file in bytes.
- Files larger than 5 MB will be printed in the terminal.

### Counting the Number of Words in a File

To count the total number of words in a file, Python can do this quickly:

```bash linenums="1"
python -c 'print(sum(len(line.split()) for line in open("file.txt")))'
```

**Explanation:**

- `len(line.split())` counts the number of words in each line.
- The outer `sum(...)` adds up the total word count from each line.

---

Python’s versatility makes it a great choice for both simple and complex automation tasks.
