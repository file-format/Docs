{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Shell script - How to run it on Ubuntu and Linux",
  "description":"Learn about what is Shell Script and how to run it on Ubuntu and Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script",
      "parent" : "misc"
    }
  },
  "lastmod" : "2023-08-07"
}

## What is Shell Script?

Shell scripting involves writing a series of commands in a plain text file, often referred to as a **Shell Script**. These scripts are executed by a shell, which is a command-line interpreter. The most common shells include 

1. Bash (Bourne Again SHell)
2. Zsh (Z Shell)
3. Fish.

Shell scripts can range from simple one-liners to complex programs, and they are used to perform a wide variety of tasks, such as file manipulation, system administration, and automation of repetitive tasks.

## Benefits of Shell Scripting:

1.  **Automation:** Shell scripts allow users to automate repetitive tasks, saving time and reducing the chance of human error.
    
2.  **Customization:** Users can create scripts tailored to their specific needs, providing a high degree of customization.
    
3.  **Batch Processing:** Shell scripts are excellent for handling batch processing tasks, where multiple commands need to be executed in sequence.
    
4.  **System Administration:** Shell scripts are commonly used for system administration tasks, such as backups, log rotation, and software installation.

## Writing a Simple Shell Script:

Let's create a basic shell script that prints a greeting message. Open a text editor and create a file named `greeting.sh`. Add the following lines:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Save the file and make it executable by running the following command in the terminal:

```
chmod +x greeting.sh
```

Now, you can execute the script:

```
./greeting.sh
```

The output should be:

```
Hello, welcome to the world of shell scripting!
```

## Running Shell Scripts on Ubuntu and Linux:

Now, we will discuss **how to run a .sh file in Ubuntu and Linux**.

1.  **Make the Script Executable:** Before running a shell script, ensure it is executable. Use the `chmod` command as shown earlier.
    
2.  **Navigate to the Script Directory:** Open a terminal and use the `cd` command to navigate to the directory containing your shell script.
    
3.  **Run the Script:** Execute the script by typing `./scriptname.sh` in the terminal, replacing "scriptname" with the actual name of your script.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Using the Bash Command:** If your script begins with `#!/bin/bash` (known as a **shebang**), you can also run it using the `bash` command.

```
bash greeting.sh
```
