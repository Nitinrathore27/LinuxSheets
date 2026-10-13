Here are the notes based on the [cat command lesson](https://labex.io/lesson/cat-command?learn=true) you were just viewing:

### Overview

The name `cat` is short for **"concatenate."** It is used to display, combine (concatenate), and redirect file contents safely in the terminal.

---

### 1. Viewing File Contents

* **Basic Usage:** Displays an entire file directly to standard output in the terminal.
```bash
cat myfile.txt

```


* *Tip:* This works well for short text, but long files may scroll past too quickly. For long files, using `less` is usually more convenient since it lets you scroll and search.

---

### 2. Concatenating Multiple Files

* **Combine files in order:** Reads files in operand order and writes their contents one after another.
```bash
cat dogfile birdfile

```


* **Save combined output to a new file:** Use standard output redirection (`>`) to save the combined results into a new or replaced file.
```bash
cat dogfile birdfile > animals

```


> **Warning:** Do not use one of the input files as the destination (e.g., `cat file1 file2 > file1`), because the file may be emptied before `cat` finishes reading it.



---

### 3. Reading Terminal Input into a File

* **Create/Overwrite a file:** Running `cat` without an input file reads standard input. Combine it with `>` to type text directly from the terminal into a file. Press `Ctrl + D` to send an end-of-file signal and exit.
```bash
cat > newfile.txt

```


*(Note: If `newfile.txt` already exists, `>` will truncate its previous contents.)*
* **Append to an existing file:** Use `>>` to add new input to the end of a file without overwriting its existing contents.
```bash
cat >> notes.txt

```



---

### 4. Formatting the Output

Several options help inspect and format output clearly:

* **`-n`**: Number all output lines, starting from 1 (`cat -n script.sh`).
* **`-b`**: Number only non-empty output lines (`cat -b notes.txt`).
* **`-s`**: Squeeze multiple consecutive blank lines into a single blank line (`cat -s messy.txt`).
* **`-A`**: Show non-printing characters, tabs, and line endings.