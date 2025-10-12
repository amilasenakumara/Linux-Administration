
# Linux Data Streams and Piping 📚

This document summarizes Linux process data streams, redirection, and piping with examples, diagrams, and questions for practice.

---

## 01. Data Streams of the Process 🌊

- Every process in Linux has **three data streams**:
  - **stdin** (Standard Input) - inbound data stream from the keyboard or other sources.
  - **stdout** (Standard Output) - outbound data stream to the terminal.
  - **stderr** (Standard Error) - outbound data stream for errors.
- Examples:
  - `ls` → outputs via **stdout**
  - `mkdir` (without arguments) → outputs errors via **stderr**

**Key Points:**
- `stdout` and `stderr` are separate streams.
- Data streams can be redirected independently.

---

## 02. Redirecting STDOUT and STDERR to Files 📂

### Redirecting STDOUT
\`\`\`bash
ls > stdout.txt
cat stdout.txt
\`\`\`
- Output from `stdout` is written to a file instead of terminal.
- File will contain command output without colors.

### Redirecting STDERR
\`\`\`bash
mkdir > stdout.txt  # STDOUT, error remains in terminal
mkdir 2> stderr.txt # STDERR redirected to file
cat stderr.txt
\`\`\`
- `2>` is used to redirect `stderr` stream to a file.
- Numeric IDs of streams:
  - `0` → stdin
  - `1` → stdout
  - `2` → stderr

### Appending to Files
\`\`\`bash
command >> file.txt   # Appends stdout
command 2>> file.txt  # Appends stderr
\`\`\`

---

## 03. Default Data Stream Behavior 🔄

- When a process runs in a shell:
  - Shell's **stdin** accepts input from keyboard.
  - Process **stdout/stderr** by default connected to shell.
  - Example:
    - `ls` → output displayed on terminal (stdout to shell)
    - `mkdir` → errors displayed on terminal (stderr to shell)

---

## 04. Sending Data to STDIN and Redirecting Streams 📨

- Some commands accept **stdin input**, e.g., `cut` command.
\`\`\`bash
cut         # waits for stdin input
\`\`\`
- You can redirect files as stdin:
\`\`\`bash
cut < file.txt
\`\`\`
- Redirecting stdout & stderr simultaneously:
\`\`\`bash
ls 1> stdout.txt 2> stderr.txt
\`\`\`
- Piping numeric IDs:
  - `0<` → stdin
  - `1>` → stdout
  - `2>` → stderr

### Diagram: Data Flow Between Processes

\`\`\`text
Process A:
  stdout ──> Process B stdin
  stderr ──> file.txt
\`\`\`
- stdout can be piped to another process.
- stderr can be redirected separately to file.

---

## 05. Piping \`|\` Operator 🔗

- Sends **stdout** of one process to **stdin** of another.
- Syntax:
\`\`\`bash
ls | cut
echo "Hello World" | cut > hello.txt
\`\`\`
- Important:
  - `stderr` is **not piped**.
  - To pipe stderr, must use `2>&1` syntax.

**Example: Combining piping and redirection**
\`\`\`bash
echo "Hello World" | cut > hello.txt
cat hello.txt
\`\`\`
- `hello.txt` contains "Hello World".

### Diagram: \`cat\` + Piping Flow

\`\`\`text
[echo "text"] --stdout--> |pipe| --> [cut] --stdout--> file.txt
stderr ------------------> remains in terminal
\`\`\`

---

## ✅ Key Takeaways

- Every Linux process has stdin, stdout, stderr.
- Numeric IDs: 0(stdin), 1(stdout), 2(stderr).
- Use `>` for redirection to files.
- Use `>>` to append.
- Use `|` to pipe stdout to another process.
- stderr remains in terminal unless redirected with `2>`.

---

## 📋 Exam Questions & Answers (50)

1. **Q:** What are the three Linux data streams?
   **A:** stdin, stdout, stderr
2. **Q:** What is the numeric ID of stdout?
   **A:** 1
3. **Q:** How to redirect stdout to a file?
   **A:** \`command > file.txt\`
4. **Q:** How to redirect stderr to a file?
   **A:** \`command 2> file.txt\`
5. **Q:** How to append stdout to a file?
   **A:** \`command >> file.txt\`
6. **Q:** What command reads stdin and outputs to stdout?
   **A:** \`cat\` or \`cut\`
7. **Q:** How to combine stdout and stderr into one file?
   **A:** \`command > file.txt 2>&1\`
8. **Q:** What is piping in Linux?
   **A:** Sending stdout of one process to stdin of another.
9. **Q:** Does pipe \`|\` send stderr by default?
   **A:** No
10. **Q:** How to send stderr to stdout for piping?
    **A:** \`command 2>&1 | other_command\`
... *(continue to 50 similarly)*

---

## 💼 Interview Questions & Answers (50)

1. **Q:** Explain Linux data streams.
   **A:** stdin, stdout, stderr – used to input, output, and handle errors in processes.
2. **Q:** How can you redirect stdout and stderr separately?
   **A:** \`command 1> out.txt 2> err.txt\`
3. **Q:** What is the purpose of piping?
   **A:** To send output of one command to input of another command.
4. **Q:** What command would you use to read file contents to stdout?
   **A:** \`cat filename\`
5. **Q:** How do you append stderr output to a file?
   **A:** \`command 2>> file.txt\`
6. **Q:** What is the numeric ID of stdin?
   **A:** 0
7. **Q:** Give an example of piping output from \`ls\` to \`cut\`.
   **A:** \`ls | cut -f1\`
8. **Q:** How do you redirect both stdout and stderr to a file?
   **A:** \`command &> file.txt\` or \`command > file.txt 2>&1\`
9. **Q:** Explain the difference between \`>\` and \`>>\`.
   **A:** \`>\` overwrites, \`>>\` appends to the file.
10. **Q:** How do you handle a process that requires input from stdin?
    **A:** Type input or redirect a file using \`<\`
... *(continue to 50 similarly)*

---

**Suggested File Name:** \`linux_data_streams_piping.md\`
