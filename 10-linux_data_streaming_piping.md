# Linux Data Streaming and Piping 📡

---

## Table of Contents
1. Introduction
2. Data Streaming
3. Piping in Linux
4. Common Use-Cases
5. Redirection vs Piping
6. Tips for Efficient Streaming
7. Exam Questions & Answers
8. Interview Questions & Answers

---

## 1️⃣ Introduction
- Linux commands often produce output (stdout) and accept input (stdin).
- Data streaming and piping allow **real-time processing** of data.
- Reduces the need for intermediate files.

---

## 2️⃣ Data Streaming 🌊
- Continuous flow of data between commands or programs.
- Uses standard input (`stdin`) and standard output (`stdout`).

**Example:**
```bash
cat file.txt
```
- Streams the content of `file.txt` to your terminal.

---

## 3️⃣ Piping in Linux |
- Sends the output of one command as input to another.
- Syntax: `command1 | command2 | command3`

**Example:**
```bash
cat file.txt | grep "error" | sort
```
- `cat file.txt` → streams file content.
- `grep "error"` → filters lines containing 'error'.
- `sort` → sorts the filtered output.

**Another Example:**
```bash
ps aux | grep firefox | awk '{print $2}'
```
- Lists PIDs of processes containing 'firefox'.

---

## 4️⃣ Common Use-Cases 🔧

### a) Count lines in a file
```bash
cat file.txt | wc -l
```

### b) Monitor logs in real-time
```bash
tail -f /var/log/syslog | grep "warning"
```

### c) View long files page by page
```bash
cat bigfile.txt | less
```

### d) Save and display output simultaneously
```bash
cat file.txt | grep "error" | tee errors.txt
```

---

## 5️⃣ Redirection vs Piping 🔄

| Feature | Symbol | Description |
|---------|--------|-------------|
| Output redirection | `>` | Save output to file (`ls > files.txt`) |
| Append output | `>>` | Append to file instead of overwriting (`ls >> files.txt`) |
| Input redirection | `<` | Read input from file (`sort < file.txt`) |
| Pipe | `|` | Send output to another command (`ls | grep txt`) |

---

## 6️⃣ Tips for Efficient Streaming 💡
- Use `less` or `more` to paginate large streams.
- Combine multiple commands with pipes instead of creating temp files.
- Use `tee` to log output while viewing it.
- Avoid unnecessary `cat` usage; many commands accept filenames directly.

---

## 7️⃣ Exam Questions & Answers 📚

1. **What does `|` (pipe) do in Linux?**
   - Sends output of one command as input to another.

2. **How do you count the number of lines in a file using a pipe?**
   - `cat file.txt | wc -l`

3. **Difference between `>` and `>>`?**
   - `>` overwrites file, `>>` appends to file.

4. **What is the purpose of `tee` command?**
   - Writes output to both file and stdout simultaneously.

5. **How to monitor a log file in real-time?**
   - `tail -f /var/log/syslog | grep "keyword"`

6. **What does `cat file.txt | grep error` do?**
   - Streams content of file.txt and filters lines containing 'error'.

7. **How to sort filtered output from a command?**
   - Use `| sort` at the end of the command chain.

8. **Which stream does `grep` read from by default?**
   - Standard input (`stdin`).

9. **Explain why data streaming is preferred over temporary files.**
   - Reduces disk usage and allows real-time processing.

10. **How to display the next page of a command’s output?**
    - Pipe output to `less` and press space to move page by page.

---

## 8️⃣ Interview Questions & Answers 💼

1. **Explain piping in Linux.**
   - Piping connects multiple commands, passing output from one as input to the next using `|`.

2. **How is data streaming different from redirection?**
   - Streaming sends data between commands in real-time; redirection saves/reads data from files.

3. **Give an example of using `tee`.**
   - `cat file.txt | grep error | tee errors.txt`

4. **What is the difference between `stdin`, `stdout`, and `stderr`?**
   - `stdin` = input stream, `stdout` = output stream, `stderr` = error stream.

5. **Why is `cat file | command` sometimes unnecessary?**
   - Many commands accept filenames directly, e.g., `grep error file.txt`.

6. **How to combine multiple filters in a pipeline?**
   - `command1 | command2 | command3` applies commands sequentially.

7. **How to monitor changes in a log file while filtering specific entries?**
   - `tail -f logfile | grep "keyword"`

8. **How do you debug long pipelines?**
   - Use intermediate commands with `tee` or split the pipeline step by step.

9. **What are common pitfalls of pipelines?**
   - Commands may fail silently, case-sensitivity, or incorrect order.

10. **How does Linux handle large data streams efficiently?**
    - Streams data in memory without creating temporary files on disk.

---

**Suggested File Name:** `linux_data_streaming_and_piping.md`

