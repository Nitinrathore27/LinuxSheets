Here are the notes on the **`touch`** command based on your recent lesson:

---

## **Overview**

The `touch` command is primarily used to change file timestamps, but it is also commonly used to create one or more empty files.

* **Basic Syntax:** `touch [OPTIONS] FILE...`

---

## **1. Creating Empty Files**

If a specified file does not exist, `touch` creates it as an empty placeholder file without adding any content.

* **Single file:**
```bash
$ touch mysuperduperfile

```


* **Multiple files:**
```bash
$ touch file1.txt file2.txt file3.log

```



*(Note: `touch` does not add text to a file; use a text editor if you need to write content.)*

---

## **2. Updating File Timestamps**

By default, running `touch` on an existing file changes both its **access time** and **modification time** to the current time, leaving the file's contents completely unchanged.

* **Example workflow:**
```bash
$ ls -l mysuperduperfile
$ touch mysuperduperfile
$ ls -l mysuperduperfile

```



---

## **3. Controlling Which Timestamp Changes**

You can use specific flags to target only one type of timestamp:

* **`-a`**: Change **only** the access time.
* **`-m`**: Change **only** the modification time.
```bash
$ touch -a notes.txt
$ touch -m notes.txt

```



---

## **4. Setting or Copying Specific Times**

* **Using a custom date string (`-d`):**
```bash
$ touch -d "2026-06-23 12:30:00" mysuperduperfile

```


* **Copying timestamps from a reference file (`-r`):**
```bash
$ touch -r file1.txt file2.txt

```


*(Here, `file1.txt` supplies the timestamps, and `file2.txt` is the file whose timestamps are updated).*

---

## **5. Avoiding File Creation (`-c`)**

Normally, `touch` creates a file if the path doesn't exist. Adding the `-c` flag suppresses file creation, meaning it will update the timestamp **only if the file already exists**:

```bash
$ touch -c existing-file.txt

```

This is particularly useful in scripts where you want to update a timestamp without accidentally introducing new, unintended files.