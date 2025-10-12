# 🐧 Linux Process Commands and `grep`

## 📌 1. `ps` Command — Process Status
The `ps` command is used to **display information about active processes**.

### 🔸 Common Usage:
```bash
ps aux
```
- `a` → show processes for all users  
- `u` → display user-oriented format  
- `x` → show processes not attached to a terminal

### 🧾 Example Output:
```
USER       PID  %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.1 169260  1156 ?        Ss   10:23   0:02 /sbin/init
user     12988  0.1  0.3 263992  6544 ?        Sl   11:00   0:01 gnome-terminal
```

---

## 📌 2. `man` Command — Manual Pages
The `man` command is used to **display the manual page** of other commands.

### 🔸 Common Usage:
```bash
man ps
```
- Opens the manual page for `ps` command.

👉 Press `q` to quit the manual view.

---

## 📌 3. `grep` Command — Global Regular Expression Print
The `grep` command is used to **search text or output using patterns**.

### 🔸 Common Usage:
```bash
grep "pattern" filename
```
- Searches for the word `pattern` inside the file `filename`.

```bash
ps aux | grep firefox
```
- Searches for all processes containing the word `firefox`.

### 🧠 Common Options:
- `-i` → ignore case (case-insensitive)
- `-n` → show line number
- `-v` → invert match (show lines *not* matching)

---

## 📌 4. Example: Combine `ps` and `grep`
```bash
ps aux | grep nginx
```
✅ This shows all running processes and filters only those containing `nginx`.

---

## 🏁 Quick Tips
- Use `ps aux` to list all processes.  
- Use `man <command>` to learn about any command.  
- Use `grep` to filter and find what you’re looking for fast.  
- You can combine commands with pipes (`|`) for more power.

---

✍️ **Author:** amilasenakumara  
📅 **Generated:** 2025-10-12
