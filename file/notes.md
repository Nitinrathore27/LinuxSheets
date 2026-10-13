Here are the notes based on the [`file` command lesson](https://labex.io/lesson/file-command?learn=true) you were just viewing:

---

### **Overview**

The `file` command is used to inspect a file and determine its likely content type without relying on its name or extension. Linux filenames do not dictate contents; for example, a file named `funny.gif` is not necessarily a GIF image.

---

### **1. Basic Usage**

* **Inspect a single file:**
```bash
$ file banana.jpg
banana.jpg: JPEG image data

```


* **How it works:** It examines filesystem metadata and recognizable patterns in the content rather than trusting the extension. The output is a classification, not a guarantee (damaged or unusual files may be labeled as generic `data`).

---

### **2. Checking Multiple Files & Wildcards**

* **Check several files at once:**
```bash
$ file notes.txt image.png archive.tar.gz

```


* **Use shell wildcards:** The shell expands `*` to match names in the current directory before `file` examines them:
```bash
$ file *

```



---

### **3. Useful Options**

* **`-i` (MIME Information):** Prints MIME-style information including media type and character set (useful for programs expecting values like `text/html`).
```bash
$ file -i index.html
index.html: text/html; charset=us-ascii

```


* **`-b` (Brief Mode):** Omit the filename from the output.
```bash
$ file -b notes.txt
ASCII text

```


* **`-L`:** Follow symbolic links and classify their targets.
* **`-z`:** Try to examine the contents of compressed files.