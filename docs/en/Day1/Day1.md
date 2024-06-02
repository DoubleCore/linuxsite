---
{
    "title": "how to ues",
    "description": "",
    "navbar": true,
    "sideBar": true,
    "footer": false,
    "outline": [
        1,
        3
    ],
    "editLink": false,
    "lastUpdated": true,
    "aside": "right",
    "layout": "doc",
    "custom": {},
    "hero": {
        "image": {
            "src": "",
            "alt": "",
            "width": "",
            "height": ""
        },
        "name": "VitePressSimple",
        "text": "quick to config vitePress",
        "description": "",
        "tagline": "",
        "actions": [],
        "features": [],
        "head": []
    }
}
---

### Day 1: Introduction to Linux

#### Objectives

- Understand the basic concepts of Linux.
- Learn the differences between Linux and Windows.
- Familiarize with different Linux distributions and why we are using Ubuntu.
- Grasp essential Linux concepts.

---

#### 1. Differences Between Linux and Windows

**Brief Introduction and Comparison**

Linux and Windows are both operating systems, but they differ significantly in terms of design, usage, and philosophy.

1. **Open Source vs. Proprietary**

   - **Linux**: Open-source, free to use and modify. Community-driven development.
   - **Windows**: Proprietary software, requires a license. Developed by Microsoft.
2. **Customization**

   - **Linux**: Highly customizable. Users can modify almost every aspect of the OS.
   - **Windows**: Limited customization options compared to Linux.
3. **Security**

   - **Linux**: Generally considered more secure due to its permission and user management model.
   - **Windows**: More targeted by malware and viruses, requiring regular updates and antivirus software.
4. **Software Availability**

   - **Linux**: Extensive repositories of free and open-source software. Some proprietary software may not be available.
   - **Windows**: Wide range of proprietary software available. Extensive support for gaming and commercial applications.
5. **Performance**

   - **Linux**: Can be more efficient and faster on older hardware due to its lightweight nature.
   - **Windows**: Requires more resources, which can impact performance on older hardware.
6. **File System**

   - **Linux**: Supports various file systems like ext4, Btrfs, XFS.
   - **Windows**: Primarily uses NTFS, FAT32.

**User Experience and Usage**

- **Linux**: Preferred by developers, IT professionals, and those who require a high level of control over their OS.
- **Windows**: Popular among general users, gamers, and businesses due to its user-friendly interface and widespread software support.

---

#### 2. Linux Distributions

**Common Linux Distributions**

1. **Ubuntu**

   - User-friendly, suitable for beginners.
   - Strong community support and regular updates.
   - Default choice for this course due to its ease of use and widespread adoption.
2. **Debian**

   - Stable and reliable.
   - Focus on free software.
   - Basis for many other distributions, including Ubuntu.
3. **Fedora**

   - Cutting-edge features and technologies.
   - Sponsored by Red Hat.
4. **CentOS**

   - Community-supported version of Red Hat Enterprise Linux (RHEL).
   - Suitable for servers and enterprise environments.
5. **Arch Linux**

   - Rolling release model.
   - Highly customizable but requires advanced knowledge.

**Why Ubuntu?**

- **User-friendly Interface**: Easy to navigate, especially for beginners.
- **Strong Community Support**: Large user base and extensive documentation.
- **Regular Updates**: Frequent updates and a predictable release cycle.
- **Comprehensive Software Repositories**: Access to a wide range of software.

---

#### 3. Essential Linux Concepts

**Kernel**

- The core of the operating system.
- Manages system resources and hardware interaction.

**Shell**

- Command-line interface for interacting with the system.
- Examples: Bash, Zsh, Fish.

**File System**

- Hierarchical structure of files and directories.
- Root directory (`/`) is the top-level directory.

**Process Management**

- Each running program is a process.
- Processes have unique IDs (PIDs) and can be managed using commands like `ps`, `top`, `kill`.

**Package Management**

- Software is distributed in packages.
- Package managers like APT (Advanced Package Tool) are used to install, update, and remove software.

---

#### Detailed Explanation of Key Concepts

**Kernel**

- Acts as a bridge between applications and hardware.
- Manages CPU, memory, and peripheral devices.
- Example: Linux kernel.

**Shell**

- Interface for executing commands.
- Shell scripting allows automation of tasks.
- Popular shells: Bash, Zsh.

**File System Hierarchy**

- Organized into directories and subdirectories.
- Important directories:
  - `/`: Root directory.
  - `/home`: User home directories.
  - `/etc`: Configuration files.
  - `/var`: Variable data like logs.
  - `/usr`: User applications and utilities.

**Process Management**

- Commands to manage processes:
  - `ps`: View current processes.
  - `top`: Real-time system monitoring.
  - `kill`: Terminate processes.

**Package Management**

- Commands for package management:
  - `apt-get update`: Update package list.
  - `apt-get upgrade`: Upgrade installed packages.
  - `apt-get install package_name`: Install a new package.
  - `apt-get remove package_name`: Remove a package.

---

### Day 1: Practical Exercises

**Exercise 1: Basic Navigation**

1. Open the terminal.
2. Display the current directory:
   ```
   $ pwd
   ```
3. List files and directories:
   ```
   $ ls
   ```
4. Change directory:
   ```
   $ cd /path/to/directory
   ```

**Exercise 2: File System Exploration**

1. Navigate to the root directory:
   ```
   $ cd /
   ```
2. List contents of `/etc` directory:
   ```
   $ ls /etc
   ```
3. Navigate to your home directory:
   ```
   $ cd ~
   ```

**Exercise 3: Process Management**

1. View current processes:
   ```
   $ ps
   ```
2. Monitor system processes in real-time:
   ```
   $ top
   ```
3. Kill a process (use with caution):
   ```
   $ kill <PID>
   ```

By the end of Day 1, users will have a foundational understanding of Linux, its differences from Windows, key distributions, and essential system concepts, preparing them for more advanced topics.
