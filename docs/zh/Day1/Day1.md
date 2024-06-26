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

## 准备工作

**准备Ubuntu环境：**

* 安装Ubuntu图形化界面（可以在虚拟机或真实机器上安装）。
* 确保系统已经更新，并安装了基本的工具和软件（如gedit）。

如果没有可以先看 'some useful tools'

## Linux系统简介

### Windows与Linux的对比分析

1. **操作界面和使用习惯：**

   * **Windows**：主要使用图形用户界面（GUI），用户通过点击图标和菜单来进行操作。GUI界面设计直观，适合大多数用户。
   * **Linux**：虽然也有GUI，但更强调命令行界面（CLI），许多操作通过输入命令来完成。CLI强大而灵活，但对新手有一定的学习曲线（新手推荐使用有GUI的图形画界面运行）
2. **系统架构：**

   * **Windows**：封闭源代码，由微软开发和维护，用户无法查看或修改系统代码。
   * **Linux**：开源操作系统，任何人都可以查看、修改和分发源代码。全球开发者社区共同维护和改进。
3. **软件管理：**

   * **Windows**：软件主要通过安装.exe或.msi文件添加，软件来源多样，包括官方网站、第三方网站等。
   * **Linux**：使用包管理系统（如APT、YUM），软件通过官方或第三方软件仓库提供。安装、更新和卸载软件更加便捷和安全。
4. **文件系统：**

   * **Windows**：文件路径使用反斜杠（\\）。
   * **Linux**：文件路径使用正斜杠（/）。文件和目录权限管理更为严格。
5. **用户和权限：**

   * **Windows**：管理员用户（Admin）和普通用户，权限管理较为简单。
   * **Linux**：**超级用户（root）和普通用户，权限管理细致**。用户需要提升权限（如使用`sudo`命令）才能执行某些系统级操作。

   > 大多数指令都可能需要使用sudo才能运行，否则会不允许执行
   >

## 2. Linux的相关版本

1. **Ubuntu：**

   * **特点**：用户友好，广泛使用于桌面和服务器。
   * **优点**：易于安装和使用，强大的社区支持，定期发布和更新。
   * **适用场景**：适合新手学习和日常使用。
     我们后续会用Ubuntu作为启动的方式
2. **Fedora：**

   * **特点**：由Red Hat支持，注重最新技术和软件。
   * **优点**：及时引入新技术和软件，适合开发者和技术爱好者。
   * **适用场景**：适合想尝试最新技术的用户。
3. **Debian：**

   * **特点**：稳定性强，是许多其他发行版（如Ubuntu）的基础。
   * **优点**：高度稳定和安全，庞大的软件库。
   * **适用场景**：适合服务器和需要高稳定性的环境。
4. **CentOS：**

   * **特点**：Red Hat Enterprise Linux的免费版本，常用于服务器。
   * **优点**：企业级稳定性和安全性，长时间支持。
   * **适用场景**：适合企业和服务器环境。

### 3. Linux内部的相关概念

1. **内核（Kernel）(不重要)：**
   * **功能**：管理硬件资源、提供系统调用接口，负责任务调度、内存管理、设备控制等。
   * **重要性**：Linux内核是整个系统的核心，控制所有底层操作，确保系统的稳定和高效运行。
2. **Shell：**
   * **功能**：命令行解释器，用户通过Shell与系统交互。
   * **常见Shell**：Bash（默认）、Zsh、Fish等。Shell脚本可以自动化执行一系列命令，提高工作效率。
3. **文件系统：**
   * **目录结构**：层次化目录结构，以根目录（/）为起点，所有文件和目录都在这个树状结构下。
   * **常见目录**：
     * `/bin`：存放基本命令二进制文件。
     * `/etc`：存放系统配置文件。
     * `/home`：用户的主目录，每个用户有一个子目录。
     * `/var`：存放系统运行时的数据，如日志文件。
     * `/tmp`：临时文件目录，系统重启后会清空。
4. **进程管理：**
   * **概念**：程序在系统上运行的实例称为进程。
   * **管理工具**：通过命令（如`ps`、`top`、`kill`）查看和管理进程。每个进程有一个唯一的进程ID（PID）。
5. **包管理：**
   * **APT（Advanced Package Tool）**：Ubuntu使用的包管理系统。
   * **基本命令**：
     * `sudo apt update`：更新软件包列表。
     * `sudo apt upgrade`：升级已安装的软件包。
     * `sudo apt install <package>`：安装新软件包。
     * `sudo apt remove <package>`：卸载软件包。
