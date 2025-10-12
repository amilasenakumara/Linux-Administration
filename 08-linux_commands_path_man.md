# 🐧 Linux Command Navigation, PATH, and Help

## Introduction
In this lesson, you will learn how to:
- Navigate **man pages** 📖
- Understand the **$PATH environment variable** 🌐
- Use the **which** command to find command locations 🔍
- Ask commands for **help** 🆘
- Search **man pages** efficiently 🔎

---

## 1️⃣ Navigating Man Pages

| Key | Action |
|-----|-------|
| Enter | Move down one line |
| Space | Move down one page |
| g | Go to the top of the page |
| G | Go to the bottom of the page |
| q | Quit the man page |

**Tip:** Learning man page navigation helps you explore commands directly in Linux.

---

## 2️⃣ Environment Variables

- **Definition:** Storage locations containing **name-value pairs**.  
- Usually **uppercase letters**.  
- View a variable with:

```bash
echo $VAR_NAME
```

- Example: `$PATH` is the most important environment variable for today.

---

## 3️⃣ $PATH Environment Variable

- Controls the **command search path**.  
- Contains **colon-separated directories**:

```
/usr/local/bin:/bin:/usr/bin
```

- How it works:
  1. When a command is typed, Linux searches directories in `$PATH` **in order**.
  2. Executes the **first matching command** found.
  3. If not found, it returns `command not found`.

- Example to check your path:

```bash
echo $PATH
```

---

## 4️⃣ Which Command

- Use `which` to **find the full path** of an executable:

```bash
which cat
which ls
```

- If multiple versions exist, the one **first in `$PATH`** is executed.

- Fun example:

```bash
which tac
```

- `tac` is `cat` in reverse: displays file contents **from bottom to top**.

---

## 5️⃣ Asking Commands for Help

- Many commands provide help flags:

| Command | Help Options |
|---------|--------------|
| ls      | `--help`     |
| gzip    | `-h`, `--help` |

- Use help flags to get **usage hints** directly from the command.

---

## 6️⃣ Searching Man Pages

- Use `man -k SEARCH_TERM` to **search for commands** related to a term.  
- Example:

```bash
man -k calendar
```

- From the results, use `man COMMAND` to read the documentation.

---

## 7️⃣ Putting It Together

1. **Explore your `$PATH` directories**:

```bash
ls /bin
ls /usr/bin
```

2. **Use `which`** to find the location of commands:

```bash
which ls
```

3. **Try `--help` or `-h`** on commands for usage information:

```bash
ls --help
gzip -h
```

4. **Read the man page** for detailed documentation:

```bash
man ls
```

5. **Search man pages** if unsure which command to use:

```bash
man -k calendar
```

---

## 🔹 Summary

| Concept | Command / Usage |
|---------|----------------|
| Navigate man pages | Enter / Space / g / G / q |
| Show env variable | `echo $VAR_NAME` |
| Show path | `echo $PATH` |
| Find command path | `which COMMAND` |
| Command help | `COMMAND --help` or `COMMAND -h` |
| Search man pages | `man -k SEARCH_TERM` |

---

## 📝 Exam Questions & Answers

1. **Q:** How do you display the value of the `$PATH` variable?  
   **A:** `echo $PATH`

2. **Q:** Which command shows the full path of `cat`?  
   **A:** `which cat`

3. **Q:** How to move to the top of a man page?  
   **A:** Press `g`

4. **Q:** How do you quit a man page?  
   **A:** Press `q`

5. **Q:** What flag can you use to get command help for `ls`?  
   **A:** `ls --help` or `ls -h`

6. **Q:** How can you search for commands related to `calendar`?  
   **A:** `man -k calendar`

7. **Q:** How are directories in `$PATH` separated?  
   **A:** By a colon `:`

8. **Q:** What happens if a command is not found in `$PATH`?  
   **A:** Linux returns `command not found`

9. **Q:** Which key moves one page down in man?  
   **A:** Spacebar

10. **Q:** What command displays hidden environment variables?  
    **A:** `echo $VAR_NAME` (all env variables can be shown with `printenv`)

---

## 💼 Interview Questions & Answers

1. **Q:** What is the purpose of the `$PATH` variable?  
   **A:** It specifies directories where Linux searches for executables.

2. **Q:** How do you find the location of an executable?  
   **A:** Use `which COMMAND`

3. **Q:** How can you search for commands related to a keyword?  
   **A:** `man -k SEARCH_TERM`

4. **Q:** How do you move to the bottom of a man page?  
   **A:** Press `Shift + G`

5. **Q:** What are environment variables in Linux?  
   **A:** Name-value pairs that store information accessible by programs.

6. **Q:** What is the difference between `-h` and `--help`?  
   **A:** Both provide command usage information; `--help` is often more descriptive.

7. **Q:** How can you explore directories in `$PATH`?  
   **A:** `ls /bin`, `ls /usr/bin`, etc.

8. **Q:** What is the function of `tac` command?  
   **A:** Displays a file’s contents in reverse order.

9. **Q:** How do you display a man page for a command?  
   **A:** `man COMMAND`

10. **Q:** Why is `$PATH` important when executing commands?  
    **A:** It determines which executable is run when a command is typed.

---

**Suggested File Name:**  
`linux_path_man_help.md`

