# 📚 Day 2: Basic Linux Commands – File Navigation

---

## 🔹 1. `ls` – List Files and Folders

📌 **What it does:**  
Displays all files and folders in your current directory.

### ▶️ Example:
```bash
ls
```

📤 **Output:**
```
file1.txt  my_folder  image.png
```

### 🧠 Extra Options:
```bash
ls -l     # Long listing (shows permissions, size, date, etc.)
ls -a     # Shows hidden files (starting with .)
ls -lh    # Human-readable sizes (KB, MB)
```

---

## 🔹 2. `cd` – Change Directory

📌 **What it does:**  
Moves you from one folder to another.

### ▶️ Example:
```bash
cd my_folder
```
*Now you're inside the folder `my_folder`.*

### 🧭 Some Tips:
```bash
cd ..         # Go one step back (to parent folder)
cd /          # Go to root directory
cd ~          # Go to home directory
cd /home/user # Go to a specific absolute path
```

---

## 🔹 3. `pwd` – Print Working Directory

📌 **What it does:**  
Displays your current location in the file system.

### ▶️ Example:
```bash
pwd
```

📤 **Output:**
```
/home/pratham/Documents
```
*This helps you confirm where you are in the system.*

---

## 🔹 4. `mkdir` – Make Directory (Create Folder)

📌 **What it does:**  
Creates a new folder.

### ▶️ Example:
```bash
mkdir my_new_folder
```
*This will create a folder named `my_new_folder` in your current directory.*

### 🧠 Extra Tip (Create nested folders at once):
```bash
mkdir -p folder1/folder2/folder3
```

---

## ✅ Summary Table:

| Command | Meaning | Example | What it does |
|---------|---------|---------|--------------|
| `ls` | List files and folders | `ls -l` | Shows files with details |
| `cd` | Change directory | `cd Documents` | Goes into "Documents" folder |
| `pwd` | Print current directory | `pwd` | Shows where you are |
| `mkdir` | Make directory | `mkdir myfolder` | Creates a new folder |

---

## 🔴 1. `rm` – Remove Files or Folders

📌 **What it does:**  
Deletes files and folders (even if they have content).

### ▶️ Delete a file:
```bash
rm file.txt
```
*This deletes the file named `file.txt`.*

### ▶️ Delete a folder with all files inside:
```bash
rm -r myfolder
```
*This deletes `myfolder` and everything inside it (files, subfolders).*

### ⚠️ Be careful:
```bash
rm -rf foldername
```
- `-r` = recursive (delete everything inside)
- `-f` = force (no confirmation)

❗ **This is a dangerous command — no "undo"!**

---

## 📁 2. `rmdir` – Remove Empty Directories Only

📌 **What it does:**  
Deletes a folder, but only if it is empty.

### ▶️ Example:
```bash
rmdir myemptyfolder
```
*If the folder has files inside, it will give an error.*

---

## ✅ Summary Table:

| Command | What it does | Works on | Example |
|---------|--------------|----------|---------|
| `rm file.txt` | Deletes a file | File | `rm hello.txt` |
| `rm -r folder` | Deletes folder + contents | Folder | `rm -r myfolder` |
| `rm -rf folder` | Force delete folder and contents | Folder | `rm -rf backup/` |
| `rmdir folder` | Deletes only empty folder | Empty folder | `rmdir emptyfolder` |

### 🧠 Tip:
Always double-check before using `rm -rf` — it can delete important files permanently.

---

## 🔹 Difference Between `-r` and `-rf`

### 🔹 1. `-r` (recursive)
**Stands for:** Recursive

**It means:** Delete everything inside a folder (subfolders, files, etc.)

### ▶️ Example:
```bash
rm -r myfolder
```
*Deletes `myfolder` and all files inside it.*  
*If any file is write-protected, it will ask for confirmation before deleting.*

### 🔹 2. `-rf` (recursive + force)
- `-r` = delete recursively
- `-f` = force delete without asking

### ▶️ Example:
```bash
rm -rf myfolder
```
*Deletes the entire folder without asking any questions, even if:*
- It contains many files
- Some files are write-protected
- It's a system folder (⚠️ risky)

### ⚠️ Use `-rf` with caution!
It can permanently delete important files and crash your system if used wrong.

---

## ✅ Summary:

| Flag | Meaning | What it does |
|------|---------|--------------|
| `-r` | Recursive | Deletes folders and their contents, asks first |
| `-rf` | Recursive + Force | Deletes folders and contents without asking |

---

## 🟢 1. `cat` – Concatenate and Display File

📌 **What it does:**  
`cat` shows the content of a normal text file on the terminal.

### ▶️ Example:
```bash
cat file.txt
```

**Output:**
```
Hello, this is a sample file!
```

### 🧠 Other uses:

**Combine multiple files:**
```bash
cat file1.txt file2.txt > combined.txt
```

**Create a file:**
```bash
cat > newfile.txt
```

---

## 🟡 2. `zcat` – Display Compressed File (without unzipping)

📌 **What it does:**  
`zcat` shows the content of a compressed `.gz` file directly — without needing to unzip it first.

### ▶️ Example:
```bash
zcat file.txt.gz
```
*It prints the uncompressed content of the `.gz` file to the screen.*

### ⚠️ Important:
- `cat` is for normal files
- `zcat` is for compressed `.gz` files

---

## ✅ Summary Table:

| Command | Use For | Works On | Example |
|---------|---------|----------|---------|
| `cat` | View normal file | `.txt`, `.log`, etc. | `cat notes.txt` |
| `zcat` | View compressed file | `.gz` files | `zcat log.txt.gz` |






# Linux Commands - Detailed Notes

## 1. `touch`
- **Purpose**: 
  - Creates a new, empty file.
  - Updates the timestamp of an existing file (modification and access times).
- **Syntax**: 
  ```bash
  touch filename
  ```
- **Example**:
  ```bash
  touch myfile.txt
  ```
  Creates an empty file named `myfile.txt` if it doesn't already exist.

---

## 2. `head`
- **Purpose**: 
  - Displays the first N lines of a file (default is 10 lines).
- **Syntax**: 
  ```bash
  head filename
  head -n 5 filename  # Show first 5 lines
  ```
- **Example**:
  ```bash
  head data.txt
  ```
  Shows the first 10 lines of `data.txt`.

---

## 3. `tail` and `tail -f`
- **Purpose**:
  - `tail`: Shows the last N lines of a file (default is 10).
  - `tail -f`: Continuously monitors the file for new lines (real-time).
- **Syntax**:
  ```bash
  tail filename
  tail -n 20 filename   # Show last 20 lines
  tail -f logfile.txt   # Follow the file as it grows
  ```
- **Example**:
  ```bash
  tail -f /var/log/syslog
  ```
  Useful for monitoring logs in real time.

---

## 4. `less` and `more`
- **Purpose**: 
  - View large files one page at a time.
  - `less` is more advanced (supports scrolling and searching).
- **Syntax**:
  ```bash
  less filename
  more filename
  ```
- **Controls for `less`**:
  - `q` to quit
  - `/search_term` to search
  - `↑/↓` to scroll
- **Example**:
  ```bash
  less bigfile.txt
  ```

---

✅ These commands are essential for working with files in the Linux command-line environment.
