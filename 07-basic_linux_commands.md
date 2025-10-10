# 🐧 Basic Linux Commands: Lets Get the ball rolling

## Introduction
In this lesson, you'll learn some basic yet essential Linux commands.  
These commands help you navigate the system, perform common tasks, and are universal across all Linux distributions.  

---

## ⚠️ Important Note
- Linux commands are **case sensitive**.  
  Example: `pwd` ≠ `PWD`  

---

## 1. 📍 Present Working Directory (`pwd`)
- Displays the **current directory** you are in.  
- Example:
  ```bash
  $ pwd
  /home/adminuser
  ```
- Logging in defaults to your **home directory**: `/home/username`.

---

## 2. 🔀 Change Directory (`cd`)
- Changes the current directory.  
- Usage:
  ```bash
  $ cd /path/to/directory
  ```
- Examples:
  ```bash
  $ cd /etc       # moves to /etc directory
  $ cd           # moves back to home directory
  ```
- Shortcut:
  - `~` represents your **home directory**.  
  - Example: `/home/adminuser` for `adminuser`.

- **Case matters**:
  - `/etc` ≠ `/ETC`  

---

## 3. 📂 List Directory Contents (`ls`)
- Shows files and directories in the current location.  
- Examples:
  ```bash
  $ ls            # basic listing
  $ ls -l         # long format with details
  ```
- Tips:
  - Add a **space** between `ls` and options: `ls -l` ✅
  - Output may be color-coded depending on the distribution.

---

## 4. 📖 Display File Contents (`cat`)
- Shows the contents of a file.  
- Example:
  ```bash
  $ cat filename
  ```
- Use case:  
  - View configuration files, logs, or simple text files.

---

## 5. 🧾 Manual Pages (`man`)
- Displays **documentation** for a command.  
- Example:
  ```bash
  $ man ls
  ```
- Tips:
  - Press **space** to scroll down.  
  - Press **q** to quit.

---

## 6. 🧹 Clear Screen (`clear`)
- Clears cluttered terminal output.  
- Example:
  ```bash
  $ clear
  ```

---

## 7. ❌ Exit Shell (`exit`)
- Logs out or exits your terminal session.  
- Example:
  ```bash
  $ exit
  ```

---

## 🔹 Summary of Commands
| Command | Function |
|---------|---------|
| `pwd`   | Display current directory |
| `cd`    | Change directory |
| `ls`    | List directory contents |
| `ls -l` | List with detailed info |
| `cat`   | Display file contents |
| `man`   | Access command manual |
| `clear` | Clear terminal screen |
| `exit`  | Exit shell session |

---

## 📝 Exam Questions & Answers

1. **Q:** What command shows the current directory?  
   **A:** `pwd`

2. **Q:** How do you change to the `/etc` directory?  
   **A:** `cd /etc`

3. **Q:** How can you return to your home directory using `cd`?  
   **A:** `cd` or `cd ~`

4. **Q:** What is the command to list files in long format?  
   **A:** `ls -l`

5. **Q:** Which command displays file contents?  
   **A:** `cat filename`

6. **Q:** How do you access a manual page for the `ls` command?  
   **A:** `man ls`

7. **Q:** What does the `clear` command do?  
   **A:** Clears the terminal screen

8. **Q:** How do you exit a Linux shell?  
   **A:** `exit`

9. **Q:** Are Linux commands case sensitive?  
   **A:** Yes

10. **Q:** What does `~` represent in Linux?  
    **A:** The home directory of the logged-in user

---

## 💼 Interview Questions & Answers

1. **Q:** Explain the `pwd` command.  
   **A:** Displays the present working directory.

2. **Q:** How does `cd` without arguments behave?  
   **A:** Returns to the home directory.

3. **Q:** What is the difference between `ls` and `ls -l`?  
   **A:** `ls` lists files; `ls -l` lists with detailed information like permissions and size.

4. **Q:** How do you view the contents of a text file?  
   **A:** Using the `cat` command.

5. **Q:** What are man pages?  
   **A:** Built-in documentation for commands, accessed using `man`.

6. **Q:** How do you scroll through a man page?  
   **A:** Press the **space bar** to move down pages.

7. **Q:** How do you exit a man page?  
   **A:** Press **q**.

8. **Q:** Why is case sensitivity important in Linux?  
   **A:** Commands and file names with different cases are treated as distinct.

9. **Q:** What does the tilde (`~`) symbol indicate?  
   **A:** Represents the user's home directory.

10. **Q:** Give an example of clearing the terminal screen.  
    **A:** `clear`

---


