# 🐧 Installing Linux on Windows Using WSL — Complete Guide

**Instructor’s Lesson Notes (Structured & Summarized)**  
Learn how to install, access, and manage Linux on Windows using **WSL (Windows Subsystem for Linux)**.

---

## 📘 Overview

- This lesson is for **Windows users** only.
- You’ll learn:
  1. How to **install Linux using WSL**
  2. How to **access Linux files** from Windows File Explorer
  3. How to **remove Linux distributions** installed via WSL

---

## ⚙️ What is WSL?

- **WSL** = *Windows Subsystem for Linux*
- It allows you to **run Linux directly on Windows**, without:
  - Virtual Machines
  - Dual boot setups
- You can run **multiple Linux distributions** at once.
- **Lightweight:** Uses fewer resources than virtual machines.

---

## 🧠 Requirements Before Installation

1. **Windows 10 or newer**  
2. **Virtualization enabled** in BIOS  
   - If you see a message about enabling virtualization, restart and do so in BIOS.  
   - BIOS instructions vary by manufacturer.  
3. **Active Internet connection** for downloading Linux distributions.

---

## 🐧 Supported Linux Distributions

- Ubuntu (default)
- AlmaLinux
- Debian
- Kali Linux
- Oracle Linux
- SUSE Linux  
- Many others available via WSL or Microsoft Store.

📝 **Note:**  
If you don’t specify a distro, WSL installs the **latest Ubuntu LTS (Long-Term Support)** automatically.

---

## 💻 Step-by-Step: Installing WSL and Linux

1. **Open Windows Terminal as Administrator**
   - Search “Terminal” → Right-click → “Run as administrator”

2. **Run Installation Command**
   ```bash
   wsl --install
   ```
   - Installs WSL & Ubuntu automatically.
   - Prompts: Click “Yes” or “Allow” when asked.

3. **Reboot your Computer**

4. **Create a Linux User**
   - Enter a username (e.g., `adminuser`)
   - Create a password
   - This is **separate** from your Windows user.

---

## 🔁 Accessing Linux After Setup

- Search for your installed distro name (e.g., “Ubuntu”)  
- Launch it → Linux terminal opens  
- To exit:
  ```bash
  exit
  ```
- To reopen: Search the distro name again in Start Menu.

💡 **Tip:** You can increase the font size by:
> Right-click window top bar → Properties → Font → Set preferred size.

---

## 🧩 Installing Additional Linux Distributions

1. List all available distros:
   ```bash
   wsl -l -o
   ```
   - `-l` = list  
   - `-o` = online

2. Install a specific distro (e.g., Debian):
   ```bash
   wsl --install -d Debian
   ```

3. Create a username & password again.

4. To list installed distros:
   ```bash
   wsl -l
   ```

---

## 🏬 Installing from Microsoft Store

If a distro isn’t available via `wsl -l -o`:
1. Open **Microsoft Store**
2. Search for the desired Linux (e.g., AlmaLinux)
3. Click **Get → Install**
4. Launch and set up username/password

---

## 📂 Accessing Linux Files from Windows

1. Open **File Explorer**
2. In the left sidebar → Click on **Linux (penguin icon)**
3. You’ll see all installed distros (e.g., Ubuntu, Debian, AlmaLinux)
4. Double-click a distro → Explore its file system (root level)

🧭 Example Path:
```
\\wsl.localhost\Ubuntu\
```

---

## 🗑️ Removing a Linux Distribution

### Step 1: Unregister from WSL
```bash
wsl --unregister <DistroName>
```
Example:
```bash
wsl --unregister Debian
```
→ Removes distro’s root file system from WSL.

### Step 2: Verify Removal
```bash
wsl -l
```
(Debian should no longer appear)

### Step 3: Uninstall from Windows Apps
1. Open **Installed Apps**
2. Search for distro (e.g., Debian)
3. Click **Uninstall → Confirm**

---

## ✅ Summary — What You Learned

- Install Linux using **WSL**
- Manage multiple Linux distributions
- Access Linux files via **Windows File Explorer**
- Uninstall distros completely
- WSL is lightweight, simple, and ideal for developers.

---

# 🧩 10 Exam Questions & Answers

### 1️⃣ What does WSL stand for?  
**Answer:** Windows Subsystem for Linux

### 2️⃣ Which Windows versions support WSL?  
**Answer:** Windows 10 and newer

### 3️⃣ What is the default Linux distribution installed by WSL?  
**Answer:** Ubuntu LTS

### 4️⃣ What command installs WSL and Ubuntu together?  
**Answer:** `wsl --install`

### 5️⃣ How do you list all available Linux distros online?  
**Answer:** `wsl -l -o`

### 6️⃣ How do you install Debian via WSL?  
**Answer:** `wsl --install -d Debian`

### 7️⃣ What does the `-d` flag represent?  
**Answer:** Distribution (Distro)

### 8️⃣ Where can you install unsupported distros from?  
**Answer:** Microsoft Store

### 9️⃣ How do you remove a distro from WSL?  
**Answer:** `wsl --unregister <DistroName>`

### 🔟 What does “LTS” stand for in Ubuntu?  
**Answer:** Long-Term Support

---

# 💼 10 Interview Questions & Answers

### 1️⃣ What’s the main advantage of using WSL over Virtual Machines?  
**Answer:** WSL is lightweight, faster, and consumes fewer system resources.

### 2️⃣ Can you run multiple Linux distributions in WSL simultaneously?  
**Answer:** Yes, WSL supports multiple distros running side by side.

### 3️⃣ How can you access Linux files from Windows?  
**Answer:** Via File Explorer → Linux icon → Select Distro → Browse files.

### 4️⃣ How do you check installed distros in WSL?  
**Answer:** `wsl -l`

### 5️⃣ What is the difference between `wsl -l` and `wsl -l -o`?  
**Answer:**  
- `wsl -l` → lists installed distros  
- `wsl -l -o` → lists available distros online

### 6️⃣ What is needed before installing WSL?  
**Answer:** Virtualization must be enabled in BIOS.

### 7️⃣ How do you completely remove a Linux distro from Windows?  
**Answer:** Use `wsl --unregister` and uninstall it via Installed Apps.

### 8️⃣ Can you access WSL files from Windows applications?  
**Answer:** Yes, via File Explorer or file path `\\wsl.localhost\\<distro>\\`

### 9️⃣ What’s the main purpose of using WSL for developers?  
**Answer:** To use Linux tools and environments within Windows easily.

### 🔟 What command allows installing a specific version of WSL?  
**Answer:** `wsl --set-version <DistroName> <VersionNumber>`

---

## 🗂️ Suggested File Name
**install-linux-on-windows-using-wsl.md**

---

## 🏁 Final Notes
WSL bridges the gap between Windows and Linux seamlessly.  
Perfect for developers, cloud engineers, and DevOps professionals who want the power of Linux without leaving Windows.

> 💡 **Pro Tip:** Once WSL is installed, you can run Docker, Kubernetes, and other Linux-based DevOps tools right inside Windows.
