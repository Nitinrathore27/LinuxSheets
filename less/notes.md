Here are the notes based on the [less - Command Line | Linux Journey](https://labex.io/lesson/less-command?learn=true) lesson you were just reading:

---

## **Linux `less` Command Notes**

The `less` command is an interactive text pager used to view long files without scrolling the entire output through the terminal.

### **1. Opening a File**

* **Basic Syntax:** `less <filename>`
* **Piping Output:** You can pipe output from other commands directly into `less` (e.g., `dmesg | less`).

### **2. Navigation Keystrokes**

* **Scroll Line/Screen:** Use `Up`, `Down`, `Page Up`, and `Page Down`.
* **Half-Screen Jump:**
* `d`: Move down half a screen
* `u`: Move up half a screen


* **File Boundaries:**
* `g`: Jump to the beginning of the file
* `G`: Jump to the end of the file


* **Help:**
* `h`: Open built-in help



### **3. Searching**

* **Forward Search:** `/search_term` (press `Enter` to execute)
* **Backward Search:** `?search_term` (press `Enter` to execute)
* **Repeat Search:**
* `n`: Repeat search in the same direction
* `N`: Repeat search in the opposite direction



### **4. Starting with Options**

* `-N`: Show line numbers
* `+G`: Open at the end of the file
* `+F`: Follow new content as it is added (similar to `tail -f`).
* *Tip:* While using `+F`, press `Ctrl + C` to stop following and return to normal navigation, then press `q` to quit.


* `-i` / `-I`: Ignore case during searches.

### **5. Quitting**

* `q`: Quit `less` and return to the shell prompt.