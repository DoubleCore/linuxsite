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

### Day 5: Shell Scripting and Automation

#### Objectives

- Understand the basics of shell scripting.
- Learn to write simple scripts to automate tasks.
- Use variables, conditionals, and loops in scripts.
- Schedule tasks using `cron`.

---

#### 1. Introduction to Shell Scripting

**What is a Shell Script?**

- A shell script is a text file containing a sequence of commands for a Unix-based operating system.
- It can automate repetitive tasks, manage system operations, and perform batch processing.

**Creating and Running a Shell Script**

1. **Create a Script File**

   - Use a text editor like `nano` or `gedit` to create a script file.
     ```bash
     $ nano myscript.sh
     ```
2. **Write a Simple Script**

   - Example content:
     ```bash
     #!/bin/bash
     echo "Hello, World!"
     ```
3. **Make the Script Executable**

   - Change the file permissions to make it executable:
     ```bash
     $ chmod +x myscript.sh
     ```
4. **Run the Script**

   - Execute the script:
     ```bash
     $ ./myscript.sh
     ```

---

#### 2. Shell Scripting Basics

**Using Variables**

- Assign values to variables:
  ```bash
  #!/bin/bash
  NAME="John"
  echo "Hello, $NAME"
  ```

**Reading User Input**

- Read input from the user:
  ```bash
  #!/bin/bash
  echo "Enter your name:"
  read NAME
  echo "Hello, $NAME"
  ```

**Using Conditionals**

- Use `if` statements to execute commands based on conditions:
  ```bash
  #!/bin/bash
  echo "Enter a number:"
  read NUM
  if [ $NUM -gt 10 ]; then
    echo "The number is greater than 10"
  else
    echo "The number is 10 or less"
  fi
  ```

**Using Loops**

- Use `for` and `while` loops to repeat commands:
  ```bash
  #!/bin/bash
  for i in 1 2 3 4 5; do
    echo "Looping ... number $i"
  done

  COUNT=1
  while [ $COUNT -le 5 ]; do
    echo "Count is $COUNT"
    COUNT=$((COUNT + 1))
  done
  ```

---

#### 3. Automating Tasks with `cron`

**Introduction to `cron`**

- `cron` is a time-based job scheduler in Unix-like operating systems.
- It allows users to schedule scripts or commands to run automatically at specified times and intervals.

**Editing the Crontab**

- Open the crontab file for editing:

  ```bash
  $ crontab -e
  ```
- Add a new cron job using the following format:

  ```plaintext
  * * * * * /path/to/script.sh
  ```

**Cron Job Timing Format**

- The cron timing format consists of five fields representing:
  - Minute (0 - 59)
  - Hour (0 - 23)
  - Day of the month (1 - 31)
  - Month (1 - 12)
  - Day of the week (0 - 7) (Sunday is both 0 and 7)

**Example Cron Jobs**

1. **Run a script every day at 2 AM:**

   ```plaintext
   0 2 * * * /path/to/script.sh
   ```
2. **Run a script every Monday at 5 PM:**

   ```plaintext
   0 17 * * 1 /path/to/script.sh
   ```
3. **Run a script every hour:**

   ```plaintext
   0 * * * * /path/to/script.sh
   ```

---

#### Practical Exercises

**Exercise 1: Create and Run a Basic Shell Script**

1. Create a script file named `greet.sh`:
   ```bash
   $ nano greet.sh
   ```
2. Add the following content:
   ```bash
   #!/bin/bash
   echo "Hello, welcome to Linux shell scripting!"
   ```
3. Make the script executable:
   ```bash
   $ chmod +x greet.sh
   ```
4. Run the script:
   ```bash
   $ ./greet.sh
   ```

**Exercise 2: Write a Script with Variables and User Input**

1. Create a script file named `userinfo.sh`:
   ```bash
   $ nano userinfo.sh
   ```
2. Add the following content:
   ```bash
   #!/bin/bash
   echo "Enter your name:"
   read NAME
   echo "Enter your age:"
   read AGE
   echo "Hello, $NAME. You are $AGE years old."
   ```
3. Make the script executable:
   ```bash
   $ chmod +x userinfo.sh
   ```
4. Run the script:
   ```bash
   $ ./userinfo.sh
   ```

**Exercise 3: Schedule a Cron Job**

1. Create a script file named `backup.sh`:
   ```bash
   $ nano backup.sh
   ```
2. Add the following content to back up a directory:
   ```bash
   #!/bin/bash
   tar -czf /path/to/backup/backup.tar.gz /path/to/directory
   ```
3. Make the script executable:
   ```bash
   $ chmod +x backup.sh
   ```
4. Schedule the script to run every day at midnight:
   ```bash
   $ crontab -e
   ```
5. Add the following line to the crontab:
   ```plaintext
   0 0 * * * /path/to/backup.sh
   ```

By the end of Day 5, users will be capable of writing basic shell scripts, using variables, conditionals, and loops, and scheduling tasks with `cron`. These skills are essential for automating tasks and managing a Linux system efficiently.
