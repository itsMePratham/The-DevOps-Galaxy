# Linux Commands Notes

## 1. cp (Copy)

### Purpose:

Copy files and directories.

### Syntax:

```bash
cp [options] source destination
```

### Examples:

- **Copy a file to another location:**

```bash
cp file1.txt backup/
```

- **Copy a file and rename it:**

```bash
cp file1.txt file2.txt
```

- **Copy a directory:**

```bash
cp -r myfolder backup/
```

### Options:

| Option | Description                        |
| ------ | ---------------------------------- |
| -r     | Recursively copy directories       |
| -i     | Prompt before overwrite            |
| -u     | Copy only if source is newer       |
| -v     | Show what's being copied (verbose) |
| -f     | Force overwrite without prompt     |

### Notes:

- Files do not need to be in the same directory level.
- Works with both relative and absolute paths.

---

## 2. mv (Move/Rename)

### Purpose:

Move or rename files and directories.

### Syntax:

```bash
mv [options] source destination
```

### Examples:

- **Move a file:**

```bash
mv file1.txt /home/user/Documents/
```

- **Rename a file:**

```bash
mv oldname.txt newname.txt
```

- **Move and rename:**

```bash
mv file1.txt backup/file_backup.txt
```

### Options:

| Option | Description                       |
| ------ | --------------------------------- |
| -i     | Prompt before overwrite           |
| -u     | Move only if destination is older |
| -v     | Show what's being moved           |
| -f     | Force move without prompt         |

### Notes:

| Feature | cp (Copy)            | mv (Move)             |
| ------- | -------------------- | --------------------- |
| Effect  | Leaves original file | Deletes original file |

---

## 3. wc (Word Count)

### Purpose:

Count lines, words, characters, or bytes in files.

### Syntax:

```bash
wc [options] filename
```

### Examples:

- **Full count:**

```bash
wc file.txt
```

- **Count lines only:**

```bash
wc -l file.txt
```

- **Count words only:**

```bash
wc -w file.txt
```

- **Count characters only:**

```bash
wc -m file.txt
```

- **Count from pipe:**

```bash
echo "Hello World" | wc -w
```

### Options:

| Option | Description            |
| ------ | ---------------------- |
| -l     | Count lines            |
| -w     | Count words            |
| -c     | Count bytes            |
| -m     | Count characters       |
| -L     | Length of longest line |

---

## 4. ln (Link)

### Purpose:

Create hard links and soft (symbolic) links.

### Syntax:

```bash
ln [options] source target
```

### Hard Link:

```bash
ln original.txt hardlink.txt
```

- Points to the same data block (inode).
- File survives if the original is deleted.
- Cannot link directories or across file systems.

### Soft Link (Symlink):

```bash
ln -s original.txt symlink.txt
```

- Works like a shortcut.
- Breaks if the original file is deleted.
- Can link directories and across file systems.

### Summary:

| Feature               | Hard Link         | Soft Link |
| --------------------- | ----------------- | --------- |
| Points to             | File data (inode) | File path |
| Breaks if source gone | No                | Yes       |
| Link directories      | No                | Yes       |
| Cross file systems    | No                | Yes       |

---

## 5. cut (Extract Data)

### Purpose:

Extract specific parts (fields/columns) from text.

### Syntax:

```bash
cut [options] filename
```

### Examples:

- **Extract characters:**

```bash
cut -c 1-5 file.txt
```

- **Extract fields from CSV:**

```bash
cut -d ',' -f 1 data.csv
```

- **Extract multiple fields:**

```bash
cut -d ',' -f 1,3 data.csv
```

- **From command output:**

```bash
echo "hello world" | cut -d ' ' -f 2
```

### Options:

| Option | Description                        |
| ------ | ---------------------------------- |
| -b     | Select by byte positions           |
| -c     | Select by character positions      |
| -f     | Select fields based on delimiter   |
| -d     | Specify delimiter (default is TAB) |

---

## 6. tee (Display and Save Output)

### Purpose:

Read input and simultaneously display and save it to a file.

### Syntax:

```bash
command | tee [options] filename
```

### Examples:

- **Display and save:**

```bash
echo "Hello World" | tee hello.txt
```

- **Append to file:**

```bash
echo "New Line" | tee -a hello.txt
```

- **With sudo:**

```bash
echo "Data" | sudo tee -a /etc/file.conf
```

### Options:

| Option | Description                 |
| ------ | --------------------------- |
| -a     | Append instead of overwrite |
| -i     | Ignore interrupt signals    |

---

## 7. sort (Sort Data)

### Purpose:

Sort text lines alphabetically or numerically.

### Syntax:

```bash
sort [options] filename
```

### Examples:

- **Sort alphabetically:**

```bash
sort names.txt
```

- **Sort numerically:**

```bash
sort -n numbers.txt
```

- **Sort in reverse:**

```bash
sort -r names.txt
```

- **Sort by specific column:**

```bash
sort -k 2 data.txt
```

### Options:

| Option | Description                   |
| ------ | ----------------------------- |
| -n     | Numeric sort                  |
| -r     | Reverse order                 |
| -k     | Sort by specific column       |
| -u     | Remove duplicates             |
| -o     | Save output to specified file |

---

## 8. clear (Clear Terminal)

### Purpose:

Clear the terminal screen.

### Syntax:

```bash
clear
```

### Notes:

- Shortcut: `Ctrl + L`
- Clears the visible terminal screen only, not the history.

---

## 9. diff (Compare Files)

### Purpose:

Compare files line by line.

### Syntax:

```bash
diff [options] file1 file2
```

### Example:

```bash
diff file1.txt file2.txt
```

### Output Example:

```
2c2
< World
---
> Word
```

### Options:

| Option | Description         |
| ------ | ------------------- |
| -u     | Unified format      |
| -i     | Ignore case         |
| -w     | Ignore white spaces |

### Real-World Uses:

- Compare code versions
- Compare config files
- Detect differences between documents

