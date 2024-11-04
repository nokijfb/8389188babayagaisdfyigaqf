---
date: 2023-05-19 
categories:
  - Devlog
tags:
  - ruby
  - bash
  - learning
---

# Ruby and Bash Scripting Adventure 0.1
#### Optimizing Terminal Scripts with it

When I open the terminal, I often have to check and update the system using `sudo apt update`. I thought this process could be made more efficient, so I started considering creating a script that would automatically perform this update only once each time the terminal is opened.<!-- more -->

I planned to write the script in the `.bashrc` file. The goal was to check if the marker file `/tmp/.apt_update_done` exists. If it doesn’t, the terminal will run the update and then create the marker file. To ensure this process starts over the next time I open the terminal, the marker file must be deleted every time I exit the terminal.

### Combining the Power of Bash and Ruby

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
However, I wanted to add a little Ruby touch mwehehe... This was my way to practicing Ruby. I modified my code to this:

```bash linenums="1"
if [ ! -f /tmp/.apt_update_done ]; then
    ruby -e 'system("sudo apt update"); File.write("/tmp/.apt_update_done", "")'
fi

trap 'ruby -e "File.delete(\"/tmp/.apt_update_done\") if File.exist?(\"/tmp/.apt_update_done\")"' EXIT
```

- **`ruby -e 'system("sudo apt update"); File.write("/tmp/.apt_update_done", "")'`**:
  - Here, we run the command `sudo apt update` using Ruby and create the marker file using `File.write`. Let’s break this down:
    - **`ruby -e`**: Executes the Ruby code written afterwards.
    - **`system('sudo apt update')`**: Calls the command `sudo apt update` from within Ruby, just like running it in the terminal. This will update the package list on the system.
    - **`;`**: Provides a separator between two statements in Ruby, allowing us to execute the next command after the previous one completes.
    - **`File.write('/tmp/.apt_update_done', '')`**: Creates the marker file `/tmp/.apt_update_done`. This writes an empty string to the file, indicating that the update has been performed.

- **`trap 'ruby -e "File.delete(\"/tmp/.apt_update_done\") if File.exist?(\"/tmp/.apt_update_done\")"' EXIT`**:
  - This captures the exit event from the terminal and uses Ruby to delete the marker file only if it exists. Let’s break this down as well:
    - **`trap`**: Captures certain signals that occur, in this case, when the terminal closes (`EXIT`).
    - **`ruby -e`**: Executes the Ruby code written afterwards when the terminal closes.
    - **`File.delete(\"/tmp/.apt_update_done\")`**: Deletes the marker file.
    - **`if File.exist?(\"/tmp/.apt_update_done\")`**: Checks whether the marker file exists before trying to delete it, to avoid errors if the file does not exist.

---
my first step of a journey to learn ruby for terminal scripting
