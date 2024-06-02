---
{
    "title": "linux importance",
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

### Day 2: Basic Command Line Operations

#### Objectives

- Learn basic command line operations.
- Understand file and directory management.
- Get familiar with permissions and how to modify them.

---

#### 1. Basic Command Line Operations

**Navigating the File System**

1. **Print Working Directory**

   - Display the current directory:
     ```bash
     $ pwd
     ```
2. **Listing Directory Contents**

   - List files and directories in the current directory:
     ```bash
     $ ls
     ```
   - List detailed information including hidden files:
     ```bash
     $ ls -al
     ```
3. **Changing Directories**

   - Change to a specific directory:
     ```bash
     $ cd /path/to/directory
     ```
   - Change to the home directory:
     ```bash
     $ cd ~
     ```
   - Change to the previous directory:
     ```bash
     $ cd -
     ```

**File and Directory Management**

1. **Creating Directories**

   - Create a new directory:
     ```bash
     $ mkdir new_directory
     ```
2. **Creating Files**

   - Create an empty file:
     ```bash
     $ touch new_file
     ```
3. **Copying Files and Directories**

   - Copy a file:
     ```bash
     $ cp source_file destination_file
     ```
   - Copy a directory and its contents:
     ```bash
     $ cp -r source_directory destination_directory
     ```
4. **Moving/Renaming Files and Directories**

   - Move or rename a file or directory:
     ```bash
     $ mv source destination
     ```
5. **Deleting Files and Directories**

   - Delete a file:
     ```bash
     $ rm file_name
     ```
   - Delete a directory and its contents:
     ```bash
     $ rm -r directory_name
     ```

---

#### 2. Understanding Permissions

**File Permissions Basics**

- Each file and directory has permissions that control who can read, write, or execute them.
- Permissions are divided into three groups:
  - **Owner**: The user who owns the file.
  - **Group**: Users who are members of the file’s group.
  - **Others**: All other users.

**Viewing Permissions**

- Use the `ls -l` command to view detailed information, including permissions:
  ```bash
  $ ls -l
  ```

**Permission Symbols**

- Permissions are represented by a string of characters, e.g., `-rwxr-xr--`.
  - `-`: File type (e.g., `-` for a regular file, `d` for a directory).
  - `r`: Read permission.
  - `w`: Write permission.
  - `x`: Execute permission.
  - The first set of three characters represents the owner's permissions, the second set represents the group's permissions, and the third set represents others' permissions.

**Changing Permissions**

- Use the `chmod` command to change permissions.
  - Add permission:
    ```bash
    $ chmod +x file_name
    ```
  - Remove permission:
    ```bash
    $ chmod -w file_name
    ```
  - Set specific permissions (e.g., `rwxr-xr--`):
    ```bash
    $ chmod 754 file_name
    ```

**Changing Ownership**

- Use the `chown` command to change the owner of a file or directory:

  ```bash
  $ sudo chown new_owner file_name
  ```
- Change the group of a file or directory:

  ```bash
  $ sudo chown :new_group file_name
  ```

**Using `sudo` for Superuser Privileges**

- `sudo` allows a permitted user to execute a command as the superuser or another user.
  - Run a command with superuser privileges:
    ```bash
    $ sudo command
    ```
  - Example: Update package lists:
    ```bash
    $ sudo apt update
    ```

---

#### Practical Exercises

**Exercise 1: Basic Navigation and Management**

1. Open the terminal.
2. Navigate to the home directory:
   ```bash
   $ cd ~
   ```
3. Create a new directory named `practice`:
   ```bash
   $ mkdir practice
   ```
4. Navigate to the `practice` directory:
   ```bash
   $ cd practice
   ```
5. Create an empty file named `example.txt`:
   ```bash
   $ touch example.txt
   ```
6. List the contents of the directory:
   ```bash
   $ ls
   ```

**Exercise 2: File Permissions**

1. View the permissions of `example.txt`:
   ```bash
   $ ls -l example.txt
   ```
2. Add execute permission to the owner:
   ```bash
   $ chmod u+x example.txt
   ```
3. Verify the changes:
   ```bash
   $ ls -l example.txt
   ```
4. Remove write permission from others:
   ```bash
   $ chmod o-w example.txt
   ```
5. Verify the changes:
   ```bash
   $ ls -l example.txt
   ```

**Exercise 3: Superuser Commands**

1. Update the package list using `sudo`:
   ```bash
   $ sudo apt update
   ```
2. Install a package (e.g., `curl`):
   ```bash
   $ sudo apt install curl
   ```
