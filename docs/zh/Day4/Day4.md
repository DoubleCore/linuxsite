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

### 第四天：软件包管理与系统监控

#### 目标

- 了解如何在Ubuntu系统上安装、更新和删除软件包。
- 掌握系统监控工具，学会查看系统资源使用情况。

---

#### 1. 软件包管理

**什么是软件包管理？**

软件包管理系统用于在Linux上安装、更新、配置和删除软件。Ubuntu使用APT（Advanced Package Tool）作为其主要的软件包管理工具。

**APT包管理器**

1. **更新软件包列表**

   - 在安装新软件之前，更新软件包列表以确保获取最新版本的信息：
     ```
     $ sudo apt update
     ```
2. **升级已安装的软件包**

   - 升级系统中所有已安装的软件包：
     ```
     $ sudo apt upgrade
     ```
3. **安装软件包**

   - 安装指定的软件包：
     ```
     $ sudo apt install package_name
     ```
   - 示例：
     ```
     $ sudo apt install vim
     ```
4. **删除软件包**

   - 删除指定的软件包：
     ```
     $ sudo apt remove package_name
     ```
   - 示例：
     ```
     $ sudo apt remove vim
     ```
5. **清理不再需要的软件包**

   - 自动删除不再需要的包：
     ```
     $ sudo apt autoremove
     ```
6. **查找软件包**

   - 搜索可用的软件包：
     ```
     $ apt search package_name
     ```
   - 示例：
     ```
     $ apt search gimp
     ```

**PPA（Personal Package Archive）**

PPA是第三方软件源，用户可以通过PPA安装特定版本的软件。

1. **添加PPA**

   - 添加PPA：
     ```
     $ sudo add-apt-repository ppa:repository_name
     ```
   - 示例：
     ```
     $ sudo add-apt-repository ppa:graphics-drivers/ppa
     ```
2. **更新软件包列表**

   - 更新列表：
     ```
     $ sudo apt update
     ```
3. **安装软件包**

   - 安装软件包：
     ```
     $ sudo apt install package_name
     ```

---

#### 2. 系统监控

**监控系统资源**

1. **使用 `top` 命令**

   - 实时显示系统中正在运行的进程和资源使用情况：
     ```
     $ top
     ```
2. **使用 `htop` 命令**

   - `htop` 是 `top` 的增强版，需要先安装：
     ```
     $ sudo apt install htop
     $ htop
     ```
3. **使用 `free` 命令**

   - 查看内存使用情况：
     ```
     $ free -h
     ```
4. **使用 `df` 命令**

   - 查看磁盘使用情况：
     ```
     $ df -h
     ```
5. **使用 `du` 命令**

   - 查看目录和文件的磁盘使用情况：
     ```
     $ du -sh /path/to/directory
     ```
6. **使用 `ps` 命令**

   - 显示系统中正在运行的进程：
     ```
     $ ps aux
     ```

**图形化系统监控工具**

1. **系统监视器**

   - Ubuntu自带的系统监视器工具，可以通过应用菜单启动，或在终端中运行：
     ```
     $ gnome-system-monitor
     ```
2. **`GNOME System Monitor`**

   - 提供图形化界面显示CPU、内存、网络使用情况，及管理进程。

**网络监控**

1. **使用 `ifconfig` 命令**

   - 查看网络接口配置：
     ```
     $ ifconfig
     ```
   - 注意：`ifconfig` 在一些系统上已被 `ip` 命令取代：
     ```
     $ ip a
     ```
2. **使用 `ping` 命令**

   - 测试网络连接：
     ```
     $ ping www.example.com
     ```
3. **使用 `netstat` 命令**

   - 显示网络连接、路由表、接口统计等：
     ```
     $ netstat -tuln
     ```
4. **使用 `traceroute` 命令**

   - 跟踪数据包路由：
     ```
     $ sudo apt install traceroute
     $ traceroute www.example.com
     ```

---

#### 实践练习

**练习1：软件包管理**

1. 更新软件包列表：
   ```
   $ sudo apt update
   ```
2. 升级系统中所有已安装的软件包：
   ```
   $ sudo apt upgrade
   ```
3. 搜索并安装`curl`软件包：
   ```
   $ apt search curl
   $ sudo apt install curl
   ```
4. 删除`curl`软件包：
   ```
   $ sudo apt remove curl
   ```
5. 清理不再需要的软件包：
   ```
   $ sudo apt autoremove
   ```

**练习2：系统监控**

1. 使用`top`命令查看系统进程和资源使用情况：
   ```
   $ top
   ```
2. 使用`htop`命令（先安装`htop`）：
   ```
   $ sudo apt install htop
   $ htop
   ```
3. 查看内存使用情况：
   ```
   $ free -h
   ```
4. 查看磁盘使用情况：
   ```
   $ df -h
   ```
5. 查看目录和文件的磁盘使用情况：
   ```
   $ du -sh /path/to/directory
   ```
6. 查看网络接口配置：
   ```
   $ ifconfig
   或
   $ ip a
   ```
7. 使用`ping`命令测试网络连接：
   ```
   $ ping www.example.com
   ```

---

通过第四天的学习，用户将掌握在Ubuntu上管理软件包的基本操作，并能使用系统监控工具查看系统资源使用情况和管理进程。这些技能对于维护系统的正常运行和解决问题至关重要。
