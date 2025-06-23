# 📚 Day 2: Basic Linux Commands – File Navigation

---

## 1. `ls` – List Files and Folders

| Command | What it does | Example Output |
|---------|--------------|----------------|
| `ls` | Shows files and folders | `file1.txt  my_folder  image.png` |
| `ls -l` | Long listing with details | Shows permissions, size, date |
| `ls -a` | Shows hidden files too | Includes files starting with `.` |
| `ls -lh` | Human-readable sizes | Shows KB, MB instead of bytes |

🧠 **In simple words:**
- **ls** = "Kya hai yahan?" (What's here?)
- **ls -l** = "Sabki details batao" (Tell me all details)

---

## 2. `cd` – Change Directory

| Command | What it does | Example |
|---------|--------------|---------|
| `cd foldername` | Go into a folder | `cd Documents` |
| `cd ..` | Go one step back | Goes to parent folder |
| `cd /` | Go to root directory | Goes to system root |
| `cd ~` | Go to home folder | Goes to `/home/username` |
| `cd /home/user` | Go to specific path | Direct navigation |

🧠 **In simple words:**
- **cd** = "Chalo vahaan" (Let's go there)
- **cd ..** = "Wapas jaao" (Go back)

---

## 3. `pwd` – Print Working Directory

| Command | What it does | Example Output |
|---------|--------------|----------------|
| `pwd` | Shows current location | `/home/pratham/Documents` |

🧠 **In simple words:**
- **pwd** = "Main kahan hun?" (Where am I?)

---

## 4. `mkdir` – Make Directory

| Command | What it does | Example |
|---------|--------------|---------|
| `mkdir foldername` | Creates a new folder | `mkdir my_new_folder` |
| `mkdir -p path/to/folder` | Creates nested folders | `mkdir -p folder1/folder2/folder3` |

🧠 **In simple words:**
- **mkdir** = "Naya folder banao" (Create new folder)
- **mkdir -p** = "Saare folders ek saath banao" (Create all folders together)

---

## 5. Difference Between `rm` Commands

| Command | What it does | Safety Level | Example |
|---------|--------------|--------------|---------|
| `rm file.txt` | Deletes a file | ✅ Safe | `rm hello.txt` |
| `rm -r folder` | Deletes folder + contents | ⚠️ Asks confirmation | `rm -r myfolder` |
| `rm -rf folder` | Force delete everything | ❌ Very dangerous | `rm -rf backup/` |
| `rmdir folder` | Deletes only empty folder | ✅ Safe | `rmdir emptyfolder` |

🧠 **In simple words:**
- **rm** = "Delete karo" (Delete it)
- **rm -r** = "Sab kuch delete karo, lekin pehle poocho" (Delete everything, but ask first)
- **rm -rf** = "Sab kuch delete karo, koi sawal nahi" (Delete everything, no questions)

---

## 6. Difference Between `-r` and `-rf` Flags

| Flag | Meaning | What it does | Risk Level |
|------|---------|--------------|------------|
| `-r` | Recursive | Deletes folders and contents, asks first | ⚠️ Medium |
| `-rf` | Recursive + Force | Deletes everything without asking | ❌ High Risk |

🧠 **In simple words:**
- **-r** = "Poore folder ko saaf karo, lekin permission leke" (Clean whole folder, but take permission)
- **-rf** = "Bas delete karo, kuch mat poocho" (Just delete, don't ask anything)

---

## 7. File Viewing Commands

| Command | Use For | Works On | Example |
|---------|---------|----------|---------|
| `cat` | View normal file | `.txt`, `.log`, etc. | `cat notes.txt` |
| `zcat` | View compressed file | `.gz` files | `zcat log.txt.gz` |

### Additional `cat` uses:
```bash
cat file1.txt file2.txt > combined.txt  # Combine files
cat > newfile.txt                       # Create new file
```

🧠 **In simple words:**
- **cat** = "File ka content dikhao" (Show file content)
- **zcat** = "Compressed file ka content dikhao" (Show compressed file content)

---

## 8. Navigation Summary

There are mainly **4 types** of navigation commands:

1. **ls** – See what's around you  
   _Example: `ls -la`_

2. **cd** – Move to different places  
   _Example: `cd Documents`_

3. **pwd** – Know where you are  
   _Example: Shows `/home/user/Documents`_

4. **mkdir** – Create new places  
   _Example: `mkdir projects`_

---

## ⚠️ Safety Tips

| ❌ Dangerous | ✅ Safe Alternative | Why |
|-------------|-------------------|-----|
| `rm -rf /` | Never do this | Deletes entire system |
| `rm -rf *` | `rm -r foldername` | Deletes everything in current directory |
| `rm -rf ~` | `rm -r ~/foldername` | Deletes entire home directory |

🧠 **Golden Rule:**
**"Socho phir karo"** (Think then do) - Always double-check before using `rm -rf`

---

## 🎯 Quick Reference Card

| Task | Command | Remember As |
|------|---------|-------------|
| See files | `ls` | "List karo" |
| Go somewhere | `cd folder` | "Change directory" |
| Where am I? | `pwd` | "Path batao" |
| Make folder | `mkdir name` | "Make directory" |
| Delete file | `rm file` | "Remove karo" |
| Delete folder | `rm -r folder` | "Remove recursively" |
| View file | `cat file` | "Content dikhao" |