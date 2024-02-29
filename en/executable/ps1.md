{
  "date" : "2024-03-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PS1 File - Windows PowerShell Cmdlet File - What is .ps1 file and how to open it?",
  "description" : "Learn about PS1 Windows PowerShell Cmdlet File and how to open it.",
  "linktitle" : "PS1",
  "menu" : {
    "docs" : {
      "identifier" : "executable-ps1",
      "parent" : "executable"
    }
  },
  "lastmod" : "2024-03-08"
}

## What is a PS1 file?

A PS1 file contains PowerShell script code. PowerShell is a task automation and configuration management framework from Microsoft, consisting of a command-line shell and associated scripting language.

Here is a simple example of what a PowerShell script might look like in a .ps1 file:

```
# This is a comment
Write-Host "Hello, World!"
```

This script will output "Hello, World!" when executed. PowerShell scripts can contain various commands and logic to automate tasks, manage system configurations, interact with system components, and more.

## PS1 File Format - More Information

PS1 files are similar to .BAT and .CMD files in that they are used to automate tasks and execute commands. However, while .BAT and .CMD files are executed in Windows command prompt using CMD.EXE or COMMAND.COM, PS1 files are executed in Windows PowerShell, which is more powerful and feature-rich shell and scripting language developed by Microsoft.

PowerShell offers a wider range of capabilities and integration with various system components and services compared to traditional command prompt. This makes PS1 files particularly useful for tasks requiring more advanced scripting, automation, and system administration on Windows platforms.

## How to open a PS1 file?

To open and execute a **.ps1 file** (PowerShell script file), you can follow these steps:

1. Locate PS1 file on your computer using File Explorer or any file manager.
1. Open PowerShell by searching for it in Start menu or using `Win + X` shortcut and selecting "Windows PowerShell".
1. If the PS1 file is not in default PowerShell directory, use the `cd` command to navigate to directory where the file is located.
1. If your system's execution policy doesn't allow running scripts, change it using the `Set-ExecutionPolicy` command.
1. In PowerShell window, type `.\filename.ps1` (replace filename with actual name of your PS1 file) and press Enter to execute the script.

You can also use a text editor such as Notepad, Notepad++, Visual Studio Code, or any other text editor of your choice to view the contents of .ps1 file. Simply right-click on the file, select "Open with", and choose your preferred text editor.

## References
* [PowerShell](https://en.wikipedia.org/wiki/PowerShell)
