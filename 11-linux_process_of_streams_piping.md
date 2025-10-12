# Linux Process Data Streams and Redirection 📚

## Table of Contents
- [Data Streams of the Process](#data-streams-of-the-process)
- [Redirecting STDOUT and STDERR to Files](#redirecting-stdout-and-stderr-to-files)
- [Where Process Data Streams Send Data by Default](#where-process-data-streams-send-data-by-default)
- [Sending Data to STDIN and Redirecting STDOUT/STDERR](#sending-data-to-stdin-and-redirecting-stdoutstderr)
- [Piping](#piping)
- [Exam Questions & Answers](#exam-questions--answers)
- [Interview Questions & Answers](#interview-questions--answers)

---

## 01. Data Streams of the Process 🛠️

- Every process in Linux has **three data streams**:
  - `stdin` – **Standard Input**: inbound data stream.
  - `stdout` – **Standard Output**: outbound data stream.
  - `stderr` – **Standard Error**: outbound error stream.
- Examples of processes:
  - Short-running: `mkdir`
  - Long-running: `bash`, `firefox`
- **Key points**:
  - `stdout` and `stderr` are separate streams.
  - You can **redirect streams independently**.
  - Example: `ls` outputs via `stdout`; `mkdir` without arguments produces an error via `stderr`.

---

## 02. Redirecting STDOUT and STDERR to Files 💾

- **Redirect `stdout`**:
  ```bash
  ls > stdout.txt
  ```
  - Output goes into `stdout.txt` instead of terminal.
- **Redirect `stderr`**:
  ```bash
  mkdir > stdout.txt 2> stderr.txt
  ```
  - `stdout` and `stderr` can be redirected to separate files.
- **Reading file contents**:
  ```bash
  cat stdout.txt
  cat stderr.txt
  ```
- **Appending to files**:
  ```bash
  command >> file.txt
  ```
  - Double `>>` appends rather than overwrites.

---

## 03. Where Process Data Streams Send Data by Default 🔄

- Default flow of streams:
  1. Keyboard → `stdin` of shell
  2. Shell → creates child process
  3. Child process `stdout`/`stderr` → Shell → Terminal
- Example:
  - `ls` → Output goes via `stdout` to shell → printed in terminal
  - `mkdir` without arguments → Error via `stderr` to shell → printed in terminal

---

## 04. Sending Data to STDIN and Redirecting STDOUT/STDERR ↔️

- **Processes can accept input via `stdin`** (e.g., `cat` command).
- Example:
  ```bash
  cat
  ```
  - Type `hello cat` → sent to `stdin` → output returned via `stdout`.
- **Numeric IDs of streams**:
  - `0` → stdin
  - `1` → stdout
  - `2` → stderr
- **Redirecting using numeric IDs**:
  ```bash
  command 1> stdout.txt 2> stderr.txt
  ```
- **Example with error file appending**:
  ```bash
  cat absent_file.txt 2>> stderr.txt
  ```
  - Error appended to existing `stderr.txt`.

---

## 05. Piping | Process to Process Communication 🔗

- **Pipe operator (`|`)**: send `stdout` of one process to `stdin` of another.
- Example:
  ```bash
  ls | cat
  ```
  - `stdout` of `ls` → `stdin` of `cat`.
- **STDERR is not piped**:
  ```bash
  cat missing_file.txt | cat
  ```
  - Error remains in terminal, not piped.
- **Combining piping and file redirection**:
  ```bash
  echo "Hello world" | cat > hello.txt
  ```
  - `stdout` flows through `cat` → written to `hello.txt`.

---

## Exam Questions & Answers 📝

1. **Q:** Name the three standard data streams of a process.  
   **A:** `stdin`, `stdout`, `stderr`.

2. **Q:** How do you redirect `stdout` to a file?  
   **A:** `command > file.txt`

3. **Q:** What is the numeric ID for `stderr`?  
   **A:** `2`

4. **Q:** Explain the difference between `>` and `>>`.  
   **A:** `>` overwrites a file; `>>` appends to a file.

5. **Q:** How can you send `stdout` of one process to `stdin` of another?  
   **A:** Using the pipe operator `|`, e.g., `ls | cat`.

---

## Interview Questions & Answers 💼

1. **Q:** What happens if `mkdir` is run without arguments?  
   **A:** It produces an error sent via `stderr`.

2. **Q:** Can `stderr` be piped to another process by default?  
   **A:** No, `stderr` is not piped by default.

3. **Q:** How would you redirect both `stdout` and `stderr` to separate files in a single command?  
   **A:** `command 1> out.txt 2> err.txt`

4. **Q:** What is the difference between `stdin` and `stdout`?  
   **A:** `stdin` is input to a process; `stdout` is output from a process.

5. **Q:** How can you append errors from a command to an existing file?  
   **A:** `command 2>> errors.txt`

---



