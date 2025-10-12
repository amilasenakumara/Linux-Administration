# 🌲 Structure of the Linux File System

## 📘 Overview

Linux organizes all files and directories in a **tree-like structure**
that begins at the **root directory** (`/`).\
Every file and directory stems from this single starting point.

------------------------------------------------------------------------

## 🧩 1. Root Directory and Hierarchy

-   The **root directory** is represented by `/`.

-   Subdirectories like `/bin`, `/home`, `/etc`, etc., branch out from
    root.

-   Each **directory** acts as a **branch**, and each **file** is a
    **leaf** of the tree.

-   Example:

        /
        ├── bin
        ├── home
        │   ├── user1
        │   └── user2
        ├── etc
        └── var

------------------------------------------------------------------------

## 🏠 2. Home Directory

-   Each user has a **personal home directory**, represented by `~`
    (tilde).
-   For example:
    -   Root user's home → `/root`
    -   Regular user's home → `/home/username`
-   You automatically log into your home directory after login.

------------------------------------------------------------------------

## 🧭 3. Finding Your Current Directory

-   Command:

    ``` bash
    pwd
    ```

    ➜ **Print Working Directory**

-   Displays the **absolute path** to your current location.

Example:

``` bash
/root
/home/bogdan
```

------------------------------------------------------------------------

## 🔀 4. Absolute vs Relative Paths

### 📍 Absolute Path

-   Starts from `/` (root).
-   Example: `/boot`, `/home/user1`
-   Always points to the same location regardless of where you are.

### 🧭 Relative Path

-   Based on your **current directory**.
-   Example: `cd run` (moves into `run` subdirectory inside current
    folder)

------------------------------------------------------------------------

## 🚶 5. Changing Directories (cd Command)

-   Go to root:

    ``` bash
    cd /
    ```

-   Go to home directory:

    ``` bash
    cd
    ```

-   Move to a specific folder using:

    -   Relative path → `cd run`
    -   Absolute path → `cd /boot`

------------------------------------------------------------------------

## 🧱 6. Understanding `.` and `..`

-   `.` → Current directory\
-   `..` → Parent directory

Examples:

``` bash
cd .       # Stay in current directory
cd ..      # Go up one level
```

------------------------------------------------------------------------

## ⚡ 7. Tab Auto-Completion

-   Press **Tab** to autocomplete file or folder names.

-   Press **Tab twice** to list available options.

-   Example:

    ``` bash
    cd /m + [Tab]  → autocompletes to /media if only one match
    ```

-   A `/` after a name means it's a **directory**, no `/` means it's a
    **file**.

------------------------------------------------------------------------

## 🧹 8. Example Directory Navigation

1.  Check where you are:

    ``` bash
    pwd
    ```

2.  Move up one level:

    ``` bash
    cd ..
    ```

3.  Move to `/boot` using an absolute path:

    ``` bash
    cd /boot
    ```

4.  Go back home:

    ``` bash
    cd
    ```

------------------------------------------------------------------------

## 🧑‍💻 9. Root vs /root

  Directory   Meaning
  ----------- ---------------------------------------------
  `/`         The **root of the entire Linux filesystem**
  `/root`     The **home directory for the root user**

⚠️ Don't confuse `/` (root directory) with `/root` (root user's home).

------------------------------------------------------------------------

## 🧾 10. Summary Points 🪶

1.  Linux filesystem starts from `/` (root).
2.  Each directory branches from root.
3.  User home directories are under `/home` or `/root` (for root user).
4.  `pwd` shows your current location.
5.  Use `cd` to navigate (absolute or relative).
6.  `.` and `..` help in relative navigation.
7.  Use **Tab** for auto-completion.
8.  `/root` ≠ `/`.
9.  Paths starting with `/` are absolute.
10. You can always return home by typing `cd`.

------------------------------------------------------------------------

## 📝 Exam Questions & Answers

### 🧩 Basic Level

1.  **Q:** What symbol represents the root directory in Linux?\
    **A:** `/`

2.  **Q:** What command displays your current working directory?\
    **A:** `pwd`

3.  **Q:** What does `~` represent in Linux?\
    **A:** The current user's home directory.

4.  **Q:** What command takes you to the root directory?\
    **A:** `cd /`

5.  **Q:** What does `..` mean when used with `cd`?\
    **A:** Move to the parent directory.

### ⚙️ Intermediate Level

6.  **Q:** What's the difference between `/root` and `/`?\
    **A:** `/root` is the root user's home; `/` is the root of the file
    system.

7.  **Q:** What command returns you to your home directory from
    anywhere?\
    **A:** `cd`

8.  **Q:** What is an absolute path?\
    **A:** A path that starts with `/` and points directly to a location
    from root.

9.  **Q:** What is a relative path?\
    **A:** A path relative to the current working directory.

10. **Q:** How can you auto-complete directory names?\
    **A:** By pressing the **Tab** key.

------------------------------------------------------------------------

## 💼 Interview Questions & Answers

### 🎯 Basic Level

1.  **Q:** Explain the Linux file system hierarchy.\
    **A:** It starts at the root directory `/` and branches into
    subdirectories like `/bin`, `/etc`, `/home`, etc.

2.  **Q:** What command do you use to navigate to your home directory
    quickly?\
    **A:** `cd`

3.  **Q:** How do you check where you are currently located in the
    system?\
    **A:** Using `pwd`.

### ⚙️ Intermediate Level

4.  **Q:** Explain the difference between absolute and relative paths
    with examples.\
    **A:** Absolute starts with `/` (e.g., `/home/user`); relative
    depends on your current directory (e.g., `cd ../folder`).

5.  **Q:** What does `.` represent in Linux?\
    **A:** The current directory.

6.  **Q:** What is the purpose of the Tab key in Linux terminals?\
    **A:** To autocomplete or list possible file and directory names.

### 🚀 Advanced Level

7.  **Q:** Why is Linux designed with a single root file system
    structure?\
    **A:** To maintain a unified and hierarchical organization of all
    files and devices.

8.  **Q:** What is the significance of mounting points in Linux?\
    **A:** They allow access to different filesystems under the single
    root hierarchy.

9.  **Q:** What happens if a user deletes the `/root` directory?\
    **A:** The root user loses their home directory, but the system may
    still function with limited privileges.

10. **Q:** How does the Linux file system differ from Windows in
    structure?\
    **A:** Linux has a single root `/`, whereas Windows uses multiple
    drives (C:, D:, etc.).

------------------------------------------------------------------------

## 📂 Suggested File Name

**`linux_filesystem_structure.md`**
