# Internet, Servers, and Applications – DevOps Basics

## 1. How Does the Internet Work?

The internet is like a huge network that connects millions of computers and devices around the world.

When you open a website or search something:
- Your device sends a request.
- That request goes to a server.
- The server sends back the data (like a webpage), and it shows on your screen.

✅ This happens using rules called **protocols** like `HTTP` and `TCP/IP`.

---

## 2. What is a Server?

A **server** is a powerful computer that stores websites, files, or apps and sends them to users when requested.

**Example:**
> When you open YouTube, a YouTube server sends you the website and videos.

---

## 3. Difference Between Web Server and Application Server

| Web Server                          | Application Server                        |
|------------------------------------|-------------------------------------------|
| Sends only website content         | Runs full applications and business logic |
| Example: Apache, Nginx             | Example: Tomcat, JBoss                    |
| Just shows the site                | Processes data and connects to databases  |

🧠 **In simple words:**
- **Web Server** = "Dikhaata hai" (shows things)
- **App Server** = "Sochta aur kaam karta hai" (does logic and thinking)

---

## 4. Types of Applications

There are mainly **3 types** of applications:

1. **Standalone Applications** – Work without internet  
   _Example: Calculator_

2. **Web Applications** – Need internet and work in browser  
   _Example: Gmail_

3. **Mobile Applications** – Run on mobile phones  
   _Example: WhatsApp_

---

## 5. What are Standalone Apps?

Standalone apps run on your computer without needing internet.

**Examples:**
- MS Paint
- VLC Player
- Calculator

---

## 6. What are Web Applications?

Web apps run inside a **browser** and need **internet**.

**Examples:**
- Facebook
- Amazon
- Google Docs

---

## 7. What is Application Support?

Application support means **helping users and fixing problems** in a running software or app.

Includes:
- Solving bugs/errors
- Monitoring app health
- Answering queries and offering technical help

🧑‍💻 _Think of it like **customer service** for software._

---

## 8. What is Application Maintenance?

Application maintenance means **updating and improving the app** even after it’s live.

Includes:
- Fixing bugs
- Adding new features
- Improving speed/performance
- Keeping security updated

🔧 _It's like servicing a car — the app needs regular care to run smoothly._

---



# Linux Basics – Operating System, Tools, and Differences

## 📌 What is Linux?

Linux is a **free and open-source operating system (OS)** — like Windows or macOS.

An **Operating System** helps you interact with your computer and run applications.  
It manages:
- CPU
- Memory
- Disk
- Hardware resources for applications

---

## 🧑‍💻 Introduction to Linux OS

- Created by **Linus Torvalds** in **1991**
- Open-source: Anyone can view, modify, and use it freely
- Widely used in:
  - Servers (web/cloud)
  - Phones (Android)
  - IoT devices (e.g., Smart TVs)
  - Supercomputers and rockets 🚀

### 🔥 Popular Linux Distros
- Ubuntu
- Debian
- Fedora
- CentOS
- Red Hat

---

## 🛠️ How to Install Linux?

Here are 4 popular ways:

### 1. **WSL (Windows Subsystem for Linux)**
- Run Linux inside Windows without VM or dual boot
- Steps:
  1. Open PowerShell as Admin
  2. Run: `wsl --install`
  3. Choose distro (e.g., Ubuntu)

✅ **Best for:** Beginners, Developers on Windows

---

### 2. **VirtualBox (Virtual Machine)**
- Create a virtual Linux system inside your computer
- Steps:
  1. Install VirtualBox
  2. Download Linux ISO (e.g., Ubuntu)
  3. Create VM and install Linux

✅ **Best for:** Learning full Linux without changing your system

---

### 3. **Cloud Platforms (AWS, GCP, Azure)**
- Use Linux remotely in the cloud
- Steps for AWS:
  1. Create account
  2. Go to EC2 > Launch Instance
  3. Select Ubuntu/Linux AMI
  4. Launch and connect via SSH

✅ **Best for:** DevOps, Server setup, Projects

---

### 4. **Vagrant (Infrastructure as Code)**
- Automate VM setup using code
- Steps:
  1. Install VirtualBox & Vagrant
  2. Run in terminal:

```bash
vagrant init ubuntu/bionic64
vagrant up



# 🆚 Difference Between Linux and Windows

| Feature           | Linux                                  | Windows                          |
|-------------------|-----------------------------------------|----------------------------------|
| Type              | Open-source (free)                      | Closed-source (paid license)     |
| User Interface    | Mostly terminal + GUI                   | Mostly GUI                       |
| Security          | Very secure                             | More virus-prone                 |
| Customizability   | Highly customizable                     | Limited customization            |
| Software Support  | Great for devs and servers              | Great for general use/gaming     |
| Usage             | Servers, cloud, DevOps, hacking         | Homes, offices, schools          |
| Speed             | Lightweight and fast                    | Heavier                          |
| File System       | ext4, XFS                               | NTFS, FAT32                      |
| Popular Distros   | Ubuntu, Fedora, Debian, Red Hat         | Windows 10/11                    |

✅ **Summary:**
- **Linux** = Free, secure, dev-friendly  
- **Windows** = Easy, user-friendly, gaming-focused

---

# 🌐 What Are Software Remote Location Server Tools?

**Remote tools** help access or control servers that are far away — using the internet.

## 🔧 Popular Tools:

| Tool             | Purpose                               | Example Use Case                          |
|------------------|----------------------------------------|-------------------------------------------|
| **SSH**          | Secure command-line access             | Managing Linux cloud server               |
| **PuTTY**        | SSH tool for Windows                   | Access Ubuntu from Windows                |
| **MobaXterm**    | SSH + GUI tools                        | Remote Linux access with UI               |
| **RDP**          | Full GUI remote access                 | Control Windows server                    |
| **FileZilla**    | SFTP file transfer                     | Upload files to server                    |
| **VS Code (SSH)**| Code editing directly on remote        | Live coding on remote VM                  |
| **Ansible**      | Automate tasks on multiple servers     | Update software on 100+ servers           |
| **AWS SSM**      | Secure cloud server access             | AWS EC2 management without SSH            |

🧠 **In Short:**  
These tools let **DevOps engineers** manage remote servers easily from their own laptop — no need to be physically near the server.

---

# 🧠 Kernel, Bootloader, and Shell

## 1. Kernel
- Core of the OS  
- Connects hardware with software  
- Manages memory, CPU, processes, files

🧩 _Think of it as the manager between hardware and apps_

---

## 2. Bootloader
- First software that runs when the computer starts  
- Loads the Operating System (Linux/Windows)

🧩 _Like the key to start your OS engine_

---

## 3. Shell
- Interface between user and OS  
- Takes your command → passes it to the kernel

### Types of Shell:
- **CLI Shell**: Bash, Zsh  
- **GUI Shell**: Desktop with icons

🧩 _Like a translator between you and the system_

---

## ✅ Summary Table

| Term        | What it Does                       | Example                  |
|-------------|-------------------------------------|--------------------------|
| **Kernel**  | Connects hardware & software        | Linux kernel             |
| **Bootloader** | Starts the OS                   | GRUB, Windows Boot Mgr   |
| **Shell**   | Command interface for users         | Bash, Command Prompt     |

---

# 🖥️ What is a Desktop Environment?

A **Desktop Environment (DE)** is the graphical part of your OS — the part you interact with:

- Icons 🖼️  
- Taskbar 🧰  
- Menus 🧾  
- Windows 🪟  
- File Manager 📁  

It gives you a **Graphical User Interface (GUI)** so you don’t need to type commands for everything.

---

## 💡 Examples of Linux Desktop Environments:

| DE Name    | Description                          |
|------------|--------------------------------------|
| **GNOME**  | Simple, modern (default in Ubuntu)   |
| **KDE**    | Highly customizable and powerful     |
| **XFCE**   | Lightweight and fast                 |
| **LXDE**   | Super light for old systems          |
| **Cinnamon**| Windows-like look and feel          |

🧠 **In Short:**  
A Desktop Environment = The "look and feel" of your Linux system.

---



# 🧱 Linux System Architecture

Linux System Architecture defines how Linux works internally — like building blocks arranged in layers.

## 📊 4 Main Layers of Linux

### 1. 🧱 Hardware Layer
The **physical parts** of your system.

Examples:
- CPU 🧠
- RAM 💾
- Hard Disk 📀
- Keyboard ⌨️
- Mouse 🖱️

👉 Hardware does not understand software directly.

---

### 2. 💓 Kernel Layer
The **core (heart)** of Linux. It connects software and hardware.

**Kernel Responsibilities:**
- Memory management
- CPU and process management
- File system handling
- I/O device control

👉 _Acts like a manager between hardware and applications._

---

### 3. 🧑‍💻 Shell Layer
The **interface** between user and kernel.

**Types:**
- CLI Shell (e.g., Bash)
- GUI Shell (e.g., Desktop)

👉 User types command → Shell → Kernel → System responds

---

### 4. 📦 Application Layer
Programs the user interacts with.

Examples:
- Firefox / Chrome
- VS Code / Nano
- Music Player
- Terminal

👉 Apps use **system calls** to talk to the Kernel.

---

### 🧠 Summary Diagram (Text-based)





| Layer       | What it Does                       |
|-------------|-------------------------------------|
| Hardware    | Physical parts of computer          |
| Kernel      | Connects hardware and software      |
| Shell       | Takes user input and passes to OS   |
| Applications| Programs that users interact with   |

---

# 🔧 What is Hardware?

**Hardware** = Physical parts of a computer (you can touch and see).

Just like our body has organs, a computer has components.

## 🧱 Types of Hardware

### 1. Input Devices
> Devices used to give data to the computer  
Examples:
- Keyboard ⌨️  
- Mouse 🖱️  
- Scanner 📠  
- Webcam 📷  
- Microphone 🎙️

---

### 2. Output Devices
> Show the result  
Examples:
- Monitor 🖥️  
- Printer 🖨️  
- Speakers 🔊  
- Projector 📽️

---

### 3. Storage Devices
> Store data  
Examples:
- HDD (Hard Disk Drive)  
- SSD (Solid State Drive)  
- Pendrive  
- Memory Card

---

### 4. Processing Units
> Brain of the computer  
Examples:
- CPU (Central Processing Unit)  
- GPU (Graphics Processing Unit)

---

### 5. Memory Devices
- **RAM**: Temporary memory  
- **ROM**: Permanent boot memory

---

### 6. Motherboard
> Connects all hardware components

---

### 7. Power Supply (SMPS)
> Provides electricity to components

---

💡 **In Simple Words:**  
Hardware = Body parts of a computer that run software and perform tasks.

---

# 📂 Linux File System

**Linux File System** organizes how Linux stores files and folders.

👉 Everything is treated as a file (even USBs and devices).

### 📌 Root Directory `/`
Unlike Windows (C:, D:), Linux has a **single root `/`**, and everything branches from it.

---

## 📁 Important Linux Directories

| Directory | Purpose / Contents                              |
|-----------|-------------------------------------------------|
| `/`       | Root of the entire system                        |
| `/home`   | User files and folders (e.g., `/home/pratham`)  |
| `/bin`    | Essential Linux commands (`ls`, `cp`, etc.)     |
| `/sbin`   | System admin commands (`reboot`, `shutdown`)    |
| `/etc`    | Configuration files                              |
| `/var`    | Log files, cache, mail                           |
| `/usr`    | User-installed software and libraries            |
| `/lib`    | Shared libraries for system programs             |
| `/tmp`    | Temporary files                                  |
| `/dev`    | Device files (USB, disks)                        |
| `/boot`   | Boot files like kernel, GRUB                     |
| `/proc`   | Virtual process-related files                    |
| `/mnt` or `/media` | Mount external drives (e.g., USB)      |

---

## 🌳 Linux File System Structure (Tree Style)





🧠 **In Short:**  
Everything starts from `/`, and the structure branches like a tree.

---

# 🆚 Difference Between Linux and Unix

| Feature          | Linux                                  | Unix                                |
|------------------|-----------------------------------------|--------------------------------------|
| Type             | Open-source (free)                      | Closed-source (paid license)         |
| Developed By     | Linus Torvalds (1991)                   | AT&T Bell Labs (1970s)               |
| Source Code      | Publicly available                      | Not available                        |
| Cost             | Free                                    | Commercial (requires license)        |
| User Base        | Devs, servers, personal systems         | Large enterprises, mainframes        |
| Security         | Very secure                             | Also secure                          |
| Examples         | Ubuntu, Fedora, CentOS, Red Hat         | AIX, Solaris, HP-UX                  |
| Portability      | Runs on any hardware                    | Limited hardware support             |
| Flexibility      | Highly customizable                     | Less flexible                        |
| DevOps Usage     | Widely used                             | Rarely used now                      |

✅ **In Simple Words:**
- **Linux** = Free, modern, widely used  
- **Unix** = Paid, original, used by enterprises

---

# 🔄 Process States in Linux

A **process** = running program.  
It can be in different **states** based on what it's doing.

### 🌀 1. Running (R)
- Process is using CPU or ready to use it  
**Example:** Performing calculations

---

### ⏸️ 2. Sleeping (S or D)
- Process is waiting (like for input or disk)

**Types:**
- `S` = Interruptible (can be woken up)  
- `D` = Uninterruptible (can’t be interrupted, like I/O wait)

---

### ⛔ 3. Stopped (T)
- Manually paused  
**Example:** Pressing `Ctrl + Z`

---

### 💀 4. Zombie (Z)
- Process finished but not fully removed  
**Takes space but does nothing**

---

### 👶 5. Orphan
- Parent process ended before child  
- Linux reassigns it to `init`

---

## 🔍 How to View Process States

Use command:

```bash
ps aux
