{
  "date": "2022-04-25",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about AHK file format and APIs that can create and open AHK files.",
  "title": "AHK File Format- AutoHotkey Script File",
  "linktitle": "AHK",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ahk"
    }
  },
  "lastmod": "2022-04-25"
}

## What is a AHK file?

An AHK file is a script file generated with AutoHotkey software application that is used for automation of tasks in Microsoft Windows. It contains instructions for automation of tasks using shortcut keys that can be used to perform instant actions. The file is executed by AutoHotkey and all the actions are performed sequentially. AHK files are powerful enough to carry out complex tasks using the hotkeys defined using the hotkeys. AHK files can be opened with text editors such as Microsoft Notepad and Notepad++.

## AHK File Format

AHK files are saved to disc as plain text files and contain lines of code that can be executed by AutoHotkey. AutoHotkey is a free, open-source scripting language and allows users to create simple to complex scripts to perform actions such as form fillers, auto-clicking, executing macros, etc. An AHK file at the minimum can perform a single action and then exit.

There are tools available that can be used to convert AHK to [Exe](/executable/exe/) files.

### AHK Example

The following example uses the Win+Z key to run Microsoft Notepad or bring it to front if it is already running.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## How do I create an AHK file?

The follwing steps can be used to create an AHK file. These assume that AutoHotkey is already installed on the machine.

* Right-Click on your desktop.
* Find "New" in the menu.
* Click "AutoHotkey Script" inside the "New" menu.
* Give the script a new name.
* Find the newly created file on your desktop and right-click it.
* Click "Edit Script".
* A window should have popped up, probably Notepad.
* Save the File.

## References

* [AutoHotkey](https://www.autohotkey.com/)
* [Batch file - by Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)
