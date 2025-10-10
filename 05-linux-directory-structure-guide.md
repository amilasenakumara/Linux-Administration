# 🗂️ Linux Directory Structure – Complete Lecture Notes

## 🧑‍🏫 Instructor Overview
In this lesson, you’ll learn about the **Linux directory structure** — the foundation of how files and folders (called directories in Linux) are organized.  
Understanding this structure improves navigation, troubleshooting, and application management on Linux systems.

---

## 🧠 Why Understanding the Linux Directory Structure Matters
- 📈 Improves your **overall Linux knowledge**
- 🔍 Helps you **navigate** efficiently
- 🧰 Speeds up **troubleshooting**
- ⚙️ Helps you **find config and log files**
- 🏗️ Enables you to **administer applications** effectively
- 🧭 Boosts confidence in using and managing Linux systems

---

## 🌳 Linux Directory Structure Overview
- The structure resembles a **tree**.
- The **root directory** (`/`) is the **base** of everything.
- All other directories **branch off** from `/`.
- The **directory separator** in Linux is a **forward slash (/)**.
- Root (`/`) is often called **“slash”**.

---

## 📁 Common Top-Level Directories

### `/ (Root)`
- The **base** of the entire Linux file system.
- No directories exist above it.
- Contains all other system directories.

---

### `/bin`
- Stores **binary files** (executables or programs).
- These are **compiled machine code** applications.
- Contains essential programs like `ls`, `cp`, `mv`, etc.

---

### `/etc`
- Contains **configuration files** for:
  - The **operating system**
  - Installed **applications**
- Example: Boot mode configuration files.

---

### `/home`
- Stores **user directories** (e.g., `/home/jason`).
- Each user has a **separate home directory**.
- Used to save **personal files**, documents, and media.

---

### `/opt`
- Holds **optional or third-party software** not bundled with Linux.
- Example: Google Earth or Chrome.

---

### `/tmp`
- Used for **temporary files**.
- Automatically cleared on **system reboot**.
- Do **not** store long-term files here.

---

### `/usr`
- Stands for **user-related programs**.
- Contains subdirectories such as:
  - `/usr/bin` → binaries
  - `/usr/lib` → libraries
  - `/usr/local` → locally installed software

---

### `/var`
- Stands for **variable data**.
- Contains **log files**, cache, and spool files.
- Commonly changes as the system runs.

---

## 🧮 Other Important Directories

### `/boot`
- Contains **boot loader** files and the **Linux kernel**.
- Essential for starting the operating system.

---

### `/media`
- Used for **removable media** (CD-ROMs, DVDs, USB drives).
- Automatically **mounts devices** for easy access.

---

### `/root`
- The **home directory** of the **root user (administrator)**.
- Located at `/root`, not `/home/root`.

---

### `/srv`
- Contains **service data** for servers.
- Examples:
  - Web data in `/srv/www`
  - FTP data in `/srv/ftp`

---

## 🧱 Application Directory Structures

### 🧩 1. Installed in `/usr/local`
- Common for **locally installed apps**.
- Example:
/usr/local/crashplan/
├── bin
├── etc
└── logs          

- Binary → `/usr/local/crashplan/bin`  
- Config → `/usr/local/crashplan/etc`  
- Logs → `/usr/local/crashplan/logs`

---

### 🧩 2. Installed in `/opt`
- Used for **third-party or commercial applications**.
- Example:  
- AVG installs in `/opt/avg`
- Google Chrome installs in `/opt/google/chrome`

---

### 🧩 3. Hybrid Example (`myapp`)
- Some apps use multiple paths:
- `/opt/myapp` → main files  
- `/etc/opt/myapp` → configuration  
- `/var/opt/myapp` → logs

---

### 🧩 4. Company-Based Structure
- For internal organization or enterprise setups:
- `/opt/acme/bin` → company-specific software  
- `/opt/google/chrome` → product-based layout

---

## 🧾 Summary of Key Directories
| Directory | Purpose |
|------------|----------|
| `/` | Root directory, base of all paths |
| `/bin` | Essential binaries |
| `/etc` | Configuration files |
| `/home` | User data and profiles |
| `/opt` | Optional/third-party apps |
| `/tmp` | Temporary files |
| `/usr` | User programs and shared data |
| `/var` | Variable data like logs |
| `/boot` | Boot and kernel files |
| `/media` | Mounted removable media |
| `/srv` | Server data |
| `/root` | Root user’s home directory |

---

## 🎯 Summary Points
- Linux uses a **hierarchical tree structure**.
- **Everything** begins from `/` (root).
- Directories organize system, user, and application data.
- Applications may reside in `/opt` or `/usr/local`.
- The **root user’s home** is `/root`, not under `/home`.
- Understanding this structure is **essential** for troubleshooting and administration.

---

## 📝 10 Exam Questions & Answers

### 🧩 Basic
1. **Q:** What is the root directory symbol in Linux?  
 **A:** `/` (forward slash)

2. **Q:** Where are binary executable files stored?  
 **A:** `/bin` and `/usr/bin`

3. **Q:** What is the purpose of `/etc`?  
 **A:** To store configuration files.

4. **Q:** Which directory holds user data?  
 **A:** `/home`

5. **Q:** Where are temporary files stored?  
 **A:** `/tmp`

---

### ⚙️ Intermediate
6. **Q:** What happens to files stored in `/tmp` after a reboot?  
 **A:** They are deleted automatically.

7. **Q:** Which directory contains the Linux kernel?  
 **A:** `/boot`

8. **Q:** What is `/var` used for?  
 **A:** For variable files like logs and cache.

9. **Q:** Where is third-party software usually installed?  
 **A:** `/opt` or `/usr/local`

10. **Q:** What is the difference between `/root` and `/home/root`?  
  **A:** `/root` is the root user’s home; `/home/root` does not exist by default.

---

## 💼 10 Interview Questions & Answers

### 🟢 Basic
1. **Q:** Explain the purpose of the root directory `/`.  
 **A:** It’s the topmost directory in Linux; all other directories branch from it.

2. **Q:** Why is understanding the Linux directory structure important?  
 **A:** It helps with navigation, troubleshooting, and system management.

3. **Q:** What is stored in `/opt`?  
 **A:** Optional or third-party applications.

4. **Q:** What does `/usr` contain?  
 **A:** User programs, binaries, and shared resources.

5. **Q:** What is the function of `/media`?  
 **A:** To mount external media like USBs or DVDs.

---

### 🔵 Advanced
6. **Q:** How do `/usr/local` and `/opt` differ?  
 **A:** `/usr/local` is for locally compiled software; `/opt` is for vendor-provided packages.

7. **Q:** Describe the path structure of an app like CrashPlan.  
 **A:** Installed in `/usr/local/crashplan/` with subfolders for bin, etc, and logs.

8. **Q:** What is the significance of `/srv` in server systems?  
 **A:** It stores service-specific data (e.g., web or FTP).

9. **Q:** Why does `/tmp` get cleared on boot?  
 **A:** To maintain system hygiene and free space for temporary processes.

10. **Q:** How can understanding directory conventions help in deploying applications?  
  **A:** It ensures proper file placement, simplifies backups, and standardizes configuration.

---

# 🧠 Advanced Linux Directory Structure – Questions & Answers

## 1. What is the purpose of the `/proc` directory?
The `/proc` directory is a **virtual filesystem** that provides information about running processes and system resources. It doesn’t contain real files on disk — it’s dynamically generated by the kernel.  
Example: `/proc/cpuinfo` shows CPU details, and `/proc/meminfo` shows memory usage.

---

## 2. How does `/sys` differ from `/proc`?
`/sys` belongs to the **sysfs** virtual filesystem. It exposes details about devices, drivers, and kernel subsystems.  
While `/proc` focuses on process and runtime data, `/sys` provides a structured representation of kernel and device information.

---

## 3. What is stored in the `/dev` directory?
`/dev` contains **device files** representing hardware or virtual devices.  
Examples: `/dev/sda` (hard disk), `/dev/null` (data sink), `/dev/tty` (terminal).

---

## 4. Why is `/bin` important in Linux?
`/bin` holds **essential user binaries** needed for basic system operation, even in single-user or recovery mode.  
Examples: `ls`, `cat`, `cp`, and `mv`.

---

## 5. How does `/usr/bin` differ from `/bin`?
`/usr/bin` stores **non-essential user commands** that are not required for system boot or repair. `/bin` is for critical utilities, while `/usr/bin` is for everyday tools installed after system setup.

---

## 6. What is the role of `/sbin`?
`/sbin` contains **system binaries** used mainly by administrators for system management.  
Examples: `ifconfig`, `fsck`, `reboot`.

---

## 7. What does `/etc` contain?
`/etc` holds **system-wide configuration files** and scripts.  
Examples: `/etc/fstab` (mount points), `/etc/hostname` (system name).

---

## 8. What is `/var` used for?
`/var` stores **variable data** that changes frequently, such as logs, caches, and spool files.  
Examples: `/var/log`, `/var/tmp`, `/var/lib`.

---

## 9. What is the function of `/home`?
`/home` contains **user directories** where personal files, configurations, and data are stored.  
Example: `/home/alex/Downloads`.

---

## 10. What is `/root` and how is it different from `/`?
`/root` is the **home directory of the root user**, not to be confused with `/`, which is the **root of the filesystem hierarchy**.

---

## 11. What is stored in `/boot`?
`/boot` holds **bootloader files**, including the kernel image and initial RAM disk (initrd).  
Example: `/boot/vmlinuz-5.15.0`.

---

## 12. What is `/lib` used for?
`/lib` contains **shared libraries** required by binaries in `/bin` and `/sbin`.  
Example: `/lib/x86_64-linux-gnu/libc.so.6`.

---

## 13. What is the purpose of `/opt`?
`/opt` is for **optional or third-party software packages** that aren’t part of the base system.  
Example: `/opt/google/chrome`.

---

## 14. What is `/srv` used for?
`/srv` holds **data served by the system**, such as websites or FTP content.  
Example: `/srv/www` for Apache web data.

---

## 15. What is `/media`?
`/media` is the **mount point for removable media** like USB drives or DVDs.  
Example: `/media/usb`.

---

## 16. What is `/mnt` used for?
`/mnt` is a **temporary mount point** used by administrators for manual mounts or testing purposes.

---

## 17. What is `/tmp` used for?
`/tmp` stores **temporary files** created by applications or users. Files here are usually deleted at reboot.

---

## 18. What is `/run` in modern Linux systems?
`/run` is a **temporary filesystem** that stores runtime information since the system booted, such as process IDs and sockets. It replaces `/var/run` in modern distros.

---

## 19. What is the purpose of `/lost+found`?
`/lost+found` contains **recovered file fragments** from a corrupted filesystem after running a repair tool like `fsck`.

---

## 20. What is `/usr/local` used for?
`/usr/local` is reserved for **locally installed software and scripts** that aren’t managed by the system’s package manager.

---

### ✅ Summary
These directories collectively define the **Linux Filesystem Hierarchy Standard (FHS)**, ensuring that applications and administrators can locate essential files consistently across distributions.

---
# 🌳 Linux File System Structure (Tree View)

/
├── bin/               # Essential binaries
│   ├── bash
│   ├── ls
│   └── cp
├── boot/              # Boot loader files
│   ├── vmlinuz
│   ├── initrd.img
│   └── grub/
├── dev/               # Device files
│   ├── sda
│   ├── tty
│   └── null
├── etc/               # Configuration files
│   ├── fstab
│   ├── hostname
│   ├── hosts
│   └── network/
├── home/              # User directories
│   ├── alice/
│   │   ├── Documents/
│   │   ├── Downloads/
│   │   └── Pictures/
│   └── bob/
├── lib/               # Shared libraries
│   ├── libc.so.6
│   └── modules/
├── lib64/             # 64-bit libraries
├── media/             # Mount points for removable media
│   └── usb/
├── mnt/               # Temporary mount points
├── opt/               # Optional/third-party software
│   ├── google/
│   │   ├── chrome/
│   │   └── earth/
│   └── myapp/
├── proc/              # Virtual filesystem for processes
│   ├── cpuinfo
│   └── meminfo
├── root/              # Root user home directory
├── run/               # Runtime variable data
│   ├── lock/
│   └── pid/
├── sbin/              # System binaries for admin
│   ├── fsck
│   ├── reboot
│   └── ifconfig
├── srv/               # Service data (web, FTP)
│   ├── www/
│   └── ftp/
├── sys/               # Kernel & device info (sysfs)
├── tmp/               # Temporary files
├── usr/               # User programs and data
│   ├── bin/
│   │   ├── nano
│   │   └── gcc
│   ├── lib/
│   ├── local/
│   │   ├── bin/
│   │   └── myapp/
│   └── share/
├── var/               # Variable data (logs, spool, cache)
│   ├── log/
│   │   └── syslog
│   ├── spool/
│   └── tmp/
└── lost+found/        # Recovered files from fsck




---

## ✅ Final Notes
Understanding the Linux directory structure is **fundamental** for anyone using, administering, or developing on Linux.  
It’s not just about memorizing directories — it’s about knowing **where things belong** and **how the system organizes itself**.

---

