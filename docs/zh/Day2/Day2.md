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

### 第三天：命令行基础与文件权限管理

#### 目标：

- 掌握基本的命令行操作，增强对CLI的信心。
- 理解并管理Linux文件权限和所有权。

---

#### 1. 命令行基础

**理解命令行的意义：**

命令行界面（CLI）是与计算机交互的强大工具。相比图形用户界面（GUI），CLI更加灵活和高效，特别适合批处理任务和自动化脚本。

**基本命令和操作：**

1. **导航文件系统：**

   - `pwd`：显示当前工作目录。
   - `ls`：列出当前目录内容。
     - 选项：`ls -l`（长格式）、`ls -a`（包括隐藏文件）。
   - `cd`：改变工作目录。
     - 使用：`cd /path/to/directory`、`cd ..`（上一级目录）、`cd ~`（主目录）。
2. **文件和目录操作：**

   - `mkdir`：创建目录。
     - 使用：`mkdir new_directory`
   - `touch`：创建空文件。
     - 使用：`touch new_file`
   - `cp`：复制文件或目录。
     - 使用：`cp source_file destination_file`
   - `mv`：移动或重命名文件或目录。
     - 使用：`mv old_name new_name`、`mv file_name /path/to/directory`
   - `rm`：删除文件或目录。
     - 使用：`rm file_name`、`rm -r directory_name`（递归删除目录）
3. **查看和编辑文件：**

   - `cat`：连接并显示文件内容。
     - 使用：`cat file_name`
   - `nano`：文本编辑器。
     - 使用：`nano file_name`
   - `gedit`：图形化文本编辑器。
     - 使用：`gedit file_name`
4. **获取帮助：**

   - `man`：查看命令的手册页。
     - 使用：`man command`
   - `--help`：显示命令的帮助信息。
     - 使用：`command --help`

---

#### 2. 文件权限和所有权

**理解Linux文件权限：**

Linux文件权限定义了谁可以访问和操作文件或目录。权限分为三类：所有者（Owner）、组（Group）和其他人（Others）。每类权限包括读取（Read）、写入（Write）和执行（Execute）三种操作。

**查看文件权限：**

- `ls -l`：长格式列出目录内容，包括权限信息。
  - 示例输出：`-rwxr-xr-- 1 user group size date time file_name`
    - `-rwxr-xr--`：权限字符串（文件类型和权限）
      - 第一个字符表示文件类型（`-`为普通文件，`d`为目录，`l`为符号链接等）。
      - 后九个字符分为三组，每组三个字符表示所有者、组和其他人的权限。
      - `r`：读取权限，`w`：写入权限，`x`：执行权限，`-`：无权限。

**修改文件权限：**

- `chmod`：修改文件权限。
  - 使用：`chmod permissions file_name`
  - 方式：
    - 符号法：`chmod u+rwx,g+rx,o-r file_name`（给所有者添加读写执行权限，组添加读执行权限，去除其他人的读权限）
    - 数字法：`chmod 755 file_name`（权限转换为八进制数：`rwxr-xr-x`）

**修改文件所有权：**

- `chown`：修改文件所有者和组。
  - 使用：`chown owner:group file_name`
  - 示例：`chown user:newgroup file_name`

**文件权限和所有权示例：**

1. **查看文件权限和所有权：**

   - `ls -l file_name`：查看文件的详细信息，包括权限和所有权。
   - 输出示例：`-rwxr-xr-- 1 alice users 1024 Jun 2 10:00 example.txt`
2. **修改文件权限：**

   - `chmod u+w,o-r example.txt`：给所有者添加写权限，去除其他人的读权限。
   - `chmod 644 example.txt`：将权限设置为`rw-r--r--`（所有者可读写，组和其他人只读）。
3. **修改文件所有权：**

   - `chown bob:developers example.txt`：将文件所有者改为bob，组改为developers。

---

#### 3. 实践练习

**练习1：基本命令操作**

1. 打开终端，进入主目录：`cd ~`
2. 创建一个新目录：`mkdir test_directory`
3. 进入新目录：`cd test_directory`
4. 创建一个新文件：`touch test_file.txt`
5. 将文件重命名：`mv test_file.txt renamed_file.txt`
6. 查看当前目录内容：`ls -l`

**练习2：文件权限和所有权管理**

1. 创建一个新文件：`touch permissions_test.txt`
2. 查看文件的初始权限：`ls -l permissions_test.txt`
3. 修改文件权限，使所有者有读写权限，组和其他人只有读权限：`chmod 644 permissions_test.txt`
4. 验证权限更改：`ls -l permissions_test.txt`
5. 修改文件所有者和组：`sudo chown $USER:$USER permissions_test.txt`
6. 验证所有权更改：`ls -l permissions_test.txt`

---

通过第三天的学习，用户将熟悉基本的命令行操作，理解并能管理文件权限和所有权。这些技能对于有效使用Linux系统和保障系统安全至关重要。
