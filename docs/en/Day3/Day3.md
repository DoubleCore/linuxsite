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

### Day 3: Working with Text Editors and Files

#### Objectives

- Learn to use basic text editors: nano and gedit.
- Understand file manipulation commands: viewing, searching, and editing text files.
- Get familiar with text processing tools like `cat`, `grep`, and `awk`.

---

#### 1. Using Text Editors

**nano Text Editor**

nano is a simple and user-friendly command-line text editor.

1. **Opening a File with nano**

   - To create or open a file:
     ```bash
     $ nano filename
     ```
2. **Basic nano Commands**

   - **Save Changes**: Press `Ctrl + O`, then press `Enter`.
   - **Exit nano**: Press `Ctrl + X`.
   - **Cut Text**: Press `Ctrl + K`.
   - **Paste Text**: Press `Ctrl + U`.
   - **Search Text**: Press `Ctrl + W`.

**gedit Text Editor**

gedit is a graphical text editor for the GNOME desktop environment.

1. **Opening a File with gedit**

   - To create or open a file:
     ```bash
     $ gedit filename &
     ```
   - The `&` symbol runs gedit in the background, allowing the terminal to be used for other commands.
2. **Basic gedit Features**

   - **Save Changes**: Click `Save` in the menu or press `Ctrl + S`.
   - **Exit gedit**: Click `Close` in the menu or press `Ctrl + Q`.
   - **Find and Replace**: Click `Search` in the menu, then `Find...` or `Replace...`.

---

#### 2. File Manipulation Commands

**Viewing Text Files**

1. **cat Command**

   - Concatenate and display file content:
     ```bash
     $ cat filename
     ```
   - Display multiple files:
     ```bash
     $ cat file1 file2
     ```
2. **more Command**

   - View file content one screen at a time:
     ```bash
     $ more filename
     ```
   - Navigate through the file using `Space` for the next page, `b` for the previous page, and `q` to quit.
3. **less Command**

   - Similar to `more` but with more navigation options:
     ```bash
     $ less filename
     ```
   - Navigate using arrow keys, `Space` for the next page, `b` for the previous page, and `q` to quit.

**Searching Text Files**

1. **grep Command**
   - Search for specific text in a file:
     ```bash
     $ grep "search_term" filename
     ```
   - Search recursively in all files in a directory:
     ```bash
     $ grep -r "search_term" directory
     ```
   - Common options:
     - `-i`: Ignore case.
     - `-n`: Show line numbers.
     - `-v`: Invert match, showing lines that do not match the search term.

**Editing Text Files**

1. **sed Command**

   - Stream editor for filtering and transforming text.
   - Replace text in a file:
     ```bash
     $ sed 's/old_text/new_text/' filename
     ```
   - Replace text globally in the file:
     ```bash
     $ sed 's/old_text/new_text/g' filename
     ```
   - Save changes to the same file:
     ```bash
     $ sed -i 's/old_text/new_text/g' filename
     ```
2. **awk Command**

   - Pattern scanning and processing language.
   - Print specific columns from a file:
     ```bash
     $ awk '{print $1, $3}' filename
     ```
   - Print lines matching a pattern:
     ```bash
     $ awk '/pattern/ {print}' filename
     ```

---

#### Practical Exercises

**Exercise 1: Using nano**

1. Open a new file with nano:
   ```bash
   $ nano myfile.txt
   ```
2. Write the following text:
   ```
   Hello, World!
   This is a sample file.
   ```
3. Save the file and exit nano.

**Exercise 2: Using gedit**

1. Open a new file with gedit:
   ```bash
   $ gedit myfile2.txt &
   ```
2. Write the following text:
   ```
   Welcome to gedit.
   Enjoy editing text files!
   ```
3. Save the file and close gedit.

**Exercise 3: Viewing Files with cat, more, and less**

1. Create a sample text file with multiple lines using nano or gedit.
2. Display the content using `cat`:
   ```bash
   $ cat myfile.txt
   ```
3. View the content one page at a time using `more`:
   ```bash
   $ more myfile.txt
   ```
4. Navigate through the file using `less`:
   ```bash
   $ less myfile.txt
   ```

**Exercise 4: Searching Files with grep**

1. Search for the word "sample" in `myfile.txt`:
   ```bash
   $ grep "sample" myfile.txt
   ```
2. Search for the word "sample" ignoring case:
   ```bash
   $ grep -i "sample" myfile.txt
   ```
3. Display line numbers while searching:
   ```bash
   $ grep -n "sample" myfile.txt
   ```

**Exercise 5: Editing Files with sed and awk**

1. Replace the word "Hello" with "Hi" in `myfile.txt` using `sed`:
   ```bash
   $ sed 's/Hello/Hi/' myfile.txt
   ```
2. Print the first and second columns of `myfile.txt` using `awk`:
   ```bash
   $ awk '{print $1, $2}' myfile.txt
   ```
