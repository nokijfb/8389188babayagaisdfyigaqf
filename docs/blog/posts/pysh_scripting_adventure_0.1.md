---
date: 2023-05-19 
categories:
  - Devlog
tags:
  - python
  - bash
  - learning
---

# Python and Bash Scripting Adventure 0.1
#### Optimizing Terminal Scripts with It

When I open the terminal, I often have to check and update the system using `sudo apt update`. I thought this process could be made more efficient, so I started considering creating a script that would automatically perform this update only once each time the terminal is opened.<!-- more -->

I planned to write the script in the `.bashrc` file. The goal was to check if the marker file `/tmp/.apt_update_done` exists. If it doesn’t, the terminal will run the update and then create the marker file. To ensure this process starts over the next time I open the terminal, the marker file must be deleted every time I exit the terminal.

### Combining the Power of Bash and Python

After formulating this idea, I began writing the code. Here’s the basic script I created:

```bash linenums="1"
if [ ! -f /tmp/.apt_update_done ]; then
    sudo apt update
    touch /tmp/.apt_update_done
fi

trap 'rm -f /tmp/.apt_update_done' EXIT
```

- **`if [ ! -f /tmp/.apt_update_done ]; then`**: This conditional statement checks if the file `/tmp/.apt_update_done` **does not exist**.
- **`sudo apt update`**: This command updates the package list on the system.
- **`touch /tmp/.apt_update_done`**: This command creates the marker file that indicates the update has been performed.
- **`trap`**: This is a command to capture a signal or event.
- **`trap 'rm -f /tmp/.apt_update_done' EXIT`**: This captures the exit event from the terminal (`EXIT`) and deletes the marker file when the terminal is closed.

> <small> <h3>When to Use `trap`</h3>
> `trap` is typically used in situations where you need to ensure that something is done before a script exits. Some common
> uses include:
> 
> 1. **Resource Cleanup**: Deleting temporary files, closing database connections, or releasing other resources.
> 2. **Error Handling**: Providing handling for situations when the script does not execute correctly.
> 3. **Signal Handling**: Capturing signals such as `SIGINT` (which is generated when you press Ctrl+C) to execute specific
> commands.</small>

<br>
However, I wanted to add a little Python touch mwehehe... This was my way of practicing Python. I modified my code to this:

```bash linenums="1"
if [ ! -f /tmp/.apt_update_done ]; then
    python3 -c 'import os; os.system("sudo apt update"); open("/tmp/.apt_update_done", "w").close()'
fi

trap 'python3 -c "import os; os.remove(\'/tmp/.apt_update_done\') if os.path.exists(\'/tmp/.apt_update_done\') else None"' EXIT
```

- **`python3 -c 'import os; os.system("sudo apt update"); open("/tmp/.apt_update_done", "w").close()'`**:
  - Here, we run the command `sudo apt update` using Python and create the marker file using `open`. Let’s break this down:
    - **`python3 -c`**: Executes the Python code written afterwards.
    - **`os.system("sudo apt update")`**: Calls the command `sudo apt update` from within Python, just like running it in the terminal. This will update the package list on the system.
    - **`;`**: Provides a separator between two statements in Python, allowing us to execute the next command after the previous one completes.
    - **`open("/tmp/.apt_update_done", "w").close()`**: Creates the marker file `/tmp/.apt_update_done`. This writes an empty string to the file, indicating that the update has been performed.

- **`trap 'python3 -c "import os; os.remove(\'/tmp/.apt_update_done\') if os.path.exists(\'/tmp/.apt_update_done\') else None"' EXIT`**:
  - This captures the exit event from the terminal and uses Python to delete the marker file only if it exists. Let’s break this down as well:
    - **`trap`**: Captures certain signals that occur, in this case, when the terminal closes (`EXIT`).
    - **`python3 -c`**: Executes the Python code written afterwards when the terminal closes.
    - **`os.remove(\'/tmp/.apt_update_done\')`**: Deletes the marker file.
    - **`if os.path.exists(\'/tmp/.apt_update_done\')`**: Checks whether the marker file exists before trying to delete it, to avoid errors if the file does not exist.
