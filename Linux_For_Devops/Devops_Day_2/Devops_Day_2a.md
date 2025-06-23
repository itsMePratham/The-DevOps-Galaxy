# 📚 Day 2: Basic Linux Commands – File Navigation

---

## 🔹 1. `ls` – List Files and Folders

📌 **What it does:**  
Displays all files and folders in your current directory.

### ▶️ Example:
```bash
ls
📤 Output:

arduino
Copy
Edit
file1.txt  my_folder  image.png
🧠 Extra Options:

bash
Copy
Edit
ls -l     # Long listing (shows permissions, size, date, etc.)
ls -a     # Shows hidden files (starting with .)
ls -lh    # Human-readable sizes (KB, MB)
🔹 2. cd – Change Directory
📌 What it does:
Moves you from one folder to another.

▶️ Example:
bash
Copy
Edit
cd my_folder
Now you're inside the folder my_folder.

🧭 Some Tips:

bash
Copy
Edit
cd ..         # Go one step back (to parent folder)
cd /          # Go to root directory
cd ~          # Go to home directory
cd /home/user # Go to a specific absolute path
🔹 3. pwd – Print Working Directory
📌 What it does:
Displays your current location in the file system.

▶️ Example:
bash
Copy
Edit
pwd
📤 Output:

arduino
Copy
Edit
/home/pratham/Documents
This helps you confirm where you are in the system.

🔹 4. mkdir – Make Directory (Create Folder)
📌 What it does:
Creates a new folder.

▶️ Example:
bash
Copy
Edit
mkdir my_new_folder
This will create a folder named my_new_folder in your current directory.

🧠 Extra Tip (Create nested folders at once):

bash
Copy
Edit
mkdir -p folder1/folder2/folder3




🔹 1. ls – List Files and Folders
📌 What it does:
Shows all files and folders in your current directory.

▶️ Example:
bash
Copy
Edit
ls
Output:

arduino
Copy
Edit
file1.txt  my_folder  image.png
🧠 Extra Options:
bash
Copy
Edit
ls -l      # long list (shows details like size, date, permissions)
ls -a      # shows hidden files too (those starting with .)
ls -lh     # human-readable sizes (like KB, MB)
🔹 2. cd – Change Directory
📌 What it does:
Moves you from one folder to another.

▶️ Example:
bash
Copy
Edit
cd my_folder
Now you're inside the folder my_folder.

🧭 Some tips:
bash
Copy
Edit
cd ..         # go one step back (to parent folder)
cd /          # go to root directory
cd ~          # go to home folder
cd /home/user # go to a specific path
🔹 3. pwd – Print Working Directory
📌 What it does:
Shows your current location in the file system.

▶️ Example:
bash
Copy
Edit
pwd
Output:

arduino
Copy
Edit
/home/pratham/Documents
This helps you know where you are in the system.

🔹 4. mkdir – Make Directory (Create Folder)
📌 What it does:
Creates a new folder.

▶️ Example:
bash
Copy
Edit
mkdir my_new_folder
This will create a folder named my_new_folder in your current location.

🧠 Extra Tip:
bash
Copy
Edit
mkdir -p folder1/folder2/folder3
This will create nested folders all at once.

✅ Summary Table:
Command	Meaning	Example	What it does
ls	List files and folders	ls -l	Shows files with details
cd	Change directory	cd Documents	Goes into "Documents" folder
pwd	Print current directory	pwd	Shows where you are
mkdir	Make directory	mkdir myfolder	Creates a new folder



🔴 1. rm – Remove files or folders
📌 What it does:
Deletes files and folders (even if they have content).

▶️ Delete a file:
bash
Copy
Edit
rm file.txt
This deletes the file named file.txt.

▶️ Delete a folder with all files inside:
bash
Copy
Edit
rm -r myfolder
This deletes myfolder and everything inside it (files, subfolders).

⚠️ Be careful:
bash
Copy
Edit
rm -rf foldername
-r = recursive (delete everything inside)

-f = force (no confirmation)

❗ This is a dangerous command — no “undo”!

📁 2. rmdir – Remove empty directories only
📌 What it does:
Deletes a folder, but only if it is empty.

▶️ Example:
bash
Copy
Edit
rmdir myemptyfolder
If the folder has files inside, it will give an error.

✅ Summary Table:
Command	What it does	Works on	Example
rm file.txt	Deletes a file	File	rm hello.txt
rm -r folder	Deletes folder + contents	Folder	rm -r myfolder
rm -rf folder	Force delete folder and contents	Folder	rm -rf backup/
rmdir folder	Deletes only empty folder	Empty folder	rmdir emptyfolder

🧠 Tip:
Always double-check before using rm -rf — it can delete important files permanently.

Let me know if you want this in Hinglish, or want to learn about touch, cp, or mv next 😊








You said:
what is the difference between -r , -rf


ChatGPT said:
Question: What is the difference between -r and -rf in Linux?
✅ Simple Answer:
These are options (flags) used with the rm command to delete folders and files.

🔹 1. -r (recursive)
Stands for: Recursive

It means: Delete everything inside a folder (subfolders, files, etc.)

▶️ Example:
bash
Copy
Edit
rm -r myfolder
Deletes myfolder and all files inside it.
If any file is write-protected, it will ask for confirmation before deleting.

🔹 2. -rf (recursive + force)
-r = delete recursively

-f = force delete without asking

▶️ Example:
bash
Copy
Edit
rm -rf myfolder
Deletes the entire folder without asking any questions, even if:

It contains many files

Some files are write-protected

It's a system folder (⚠️ risky)

⚠️ Use -rf with caution!
It can permanently delete important files and crash your system if used wrong.

✅ Summary:
Flag	Meaning	What it does
-r	Recursive	Deletes folders and their contents, asks first
-rf	Recursive + Force	Deletes folders and contents without asking


🟢 1. cat – Concatenate and Display File
📌 What it does:
cat shows the content of a normal text file on the terminal.

▶️ Example:
bash
Copy
Edit
cat file.txt
Output:

kotlin
Copy
Edit
Hello, this is a sample file!
🧠 Other uses:
Combine multiple files:

bash
Copy
Edit
cat file1.txt file2.txt > combined.txt
Create a file:

bash
Copy
Edit
cat > newfile.txt
🟡 2. zcat – Display Compressed File (without unzipping)
📌 What it does:
zcat shows the content of a compressed .gz file directly — without needing to unzip it first.

▶️ Example:
bash
Copy
Edit
zcat file.txt.gz
Output:
It prints the uncompressed content of the .gz file to the screen.

⚠️ Important:
cat is for normal files

zcat is for compressed .gz files

✅ Summary Table:
Command	Use For	Works On	Example
cat	View normal file	.txt, .log, etc.	cat notes.txt
zcat	View compressed file	.gz files	zcat log.txt.gz