{
  "date" : "2021-06-24",
  "keywords": [ "bat file", "what is a bat file", "file", "bat file example", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "title" : "BAT - Batch File Format",
  "toc" : true,
  "description":"Learn about BAT file format and APIs that can create and open BAT files.",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable",
     }
  },
  "lastmod" : "2021-06-24"
}

## What is a BAT file?
A BAT file is known as a batch file runs with DOS and all versions of Windows, under cmd.exe. It consists of a series of line commands in plain text to be executed by the command-line interpreter to perform different tasks, such as running maintenance utilities within Windows or starting typical programs. A batch file may include any command that can be accepted by the interpreter interactively and use the structure of code that enable conditional branching and looping as written within the batch file.
## BAT file format
A BAT file format is simply a script incorporated to automate command sequences which are repetitive in nature. The term "batch" is used for batch processing, It can be considered as "non-interactive execution". Therefore a batch file may not process a batch of multiple data. In the old Disk Operating System (DOS), the batch file was run under the command line interface by typing the filename and the extension .bat. The earlier Microsoft graphical interface based operating system such as Microsoft Windows was dependent on DOS. The users had to use DOS to perform typical operations like repair, optimize or re-installing Windows. Later on the Microsoft introduced Windows NT which was not dependent on DOS operating system. Therefore, the batch files can  be run by using Command Prompt or **cmd.exe** in the modern days Microsoft operating systems.
### Batch file parameters
Command prompt supports a number of special variables such as **%0, %1 to %9** in order to refer to the name and path of the batch job and the nine calling parameters from within the batch job. Non-existent parameters are replaced by a string having zero-length. Although, they can be used similar to environment variables, but are not saved in the environment. Microsoft and IBM refer to these variables as replacement parameters, While Novell, Digital Research, and Caldera introduced the term replacement variables for them. 

Here are some useful Batch file commands:
| Command |   Description |
------|------------|
|  VER | This batch command shows the version of MS-DOS you are using. |
|ASSOC| This is a batch command that associates an extension with a file type (FTYPE), displays existing associations, or deletes an association. |
|CD| This batch command helps in making changes to a different directory, or displays the current directory. |
|CLS| This batch command clears the screen. |
|COPY| This batch command is used for copying files from one location to the other. |
|DEL| This batch command deletes files and not directories. |
|DIR| This batch command lists the contents of a directory. |
|DATE| This batch command help to find the system date. |
|ECHO| This batch command displays messages, or turns command echoing on or off. |
|EXIT| This batch command exits the DOS console. |
|MD| This batch command creates a new directory in the current location. |
|MOVE| This batch command moves files or directories between directories. |
|PATH| This batch command displays or sets the path variable. |
|PAUSE| This batch command prompts the user and waits for a line of input to be entered. |
|PROMPT| This batch command can be used to change or reset the cmd.exe prompt. |
|RD| This batch command removes directories, but the directories need to be empty before they can be removed. |
|REN| Renames files and directories |
|REM| This batch command is used for remarks in batch files, preventing the content of the remark from being executed. |
|START| This batch command starts a program in new window, or opens a document. |
|TIME| This batch command sets or displays the time. |
|TYPE| This batch command prints the content of a file or files to the output. |
|VOL| This batch command displays the volume labels. |
|ATTRIB| Displays or sets the attributes of the files in the curret directory |
|CHKDSK| This batch command checks the disk for any problems. |
|CHOICE| This batch command provides a list of options to the user. |
|CMD| This batch command invokes another instance of command prompt. |
|COMP| This batch command compares 2 files based on the file size. |
|CONVERT| This batch command converts a volume from FAT16 or FAT32 file system to NTFS file system. |
|DRIVERQUERY| This batch command shows all installed device drivers and their properties. |
|EXPAND| This batch command extracts files from compressed .cab cabinet files. |
|FIND| This batch command searches for a string in files or input, outputting matching lines. |
|FORMAT| This batch command formats a disk to use Windows-supported file system such as FAT, FAT32 or NTFS, thereby overwriting the previous content of the disk. |
|HELP| This batch command shows the list of Windows-supplied commands. |
|IPCONFIG| This batch command displays Windows IP Configuration. Shows configuration by connection and the name of that connection. |
|LABEL| This batch command adds, sets or removes a disk label. |
|MORE| This batch command displays the contents of a file or files, one screen at a time. |
|NET| Provides various network services, depending on the command used. |
|PING| This batch command sends ICMP/IP "echo" packets over the network to the designated address. |
|SHUTDOWN| This batch command shuts down a computer, or logs off the current user. |
|SORT| This batch command takes the input from a source file and sorts its contents alphabetically, from A to Z or Z to A. It prints the output on the console. |
|SUBST| This batch command assigns a drive letter to a local folder, displays current assignments, or removes an assignment. |
|SYSTEMINFO| This batch command shows configuration of a computer and its operating system. |
|TASKKILL| This batch command ends one or more tasks. |
|TASKLIST| This batch command lists tasks, including task name and process id (PID). |
|XCOPY| This batch command copies files and directories in a more advanced way. |
|TREE| This batch command displays a tree of all subdirectories of the current directory to any level of recursion or depth. |
|FC |This batch command lists the actual differences between two files. |
|DISKPART |This batch command shows and configures the properties of disk partitions. |
|TITLE |This batch command sets the title displayed in the console window. |
|SET | Displays the list of environment variables on the current system. |

## BAT file example
Batch scripts are usually saved as simple text files; containing commands that get executed in a sequence. These files are saved with .bat extension; recognized and executed by using **Command Interpreter** software. This software is natively available in Microsoft Windows with name **cmd.exe**.

Here is a sample Batch Script which deletes all files in the current directory:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## References 

* [Batch Script - Quick Guide](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Batch file - by Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)
