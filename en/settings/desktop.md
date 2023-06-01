{
  "date": "2023-05-31",
  "keywords": [
    "desktop file",
    "what is a desktop file",
    "what does desktop file contain",
    "example desktop file",
    "how to open desktop file",
    "what is the format of desktop file",
    "file",
    "desktop file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "DESKTOP File Format - Desktop Entry File",
  "description": "Learn about DESKTOP format and APIs that can create and open DESKTOP files.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
    }
  },
  "lastmod": "2023-05-31"
}

## What is a DESKTOP file?

A .desktop file is a configuration file used by Linux desktop environments to define application shortcuts and launchers. It provides metadata about an application such as its name, icon, command to execute and other properties. These files are typically used to create shortcuts in application menus, desktop launchers or panels in Linux-based systems.

## What does DESKTOP file contain?

A .desktop file follows specific format and contains several key fields:

- **[Desktop Entry]:** This is the main section header for the .desktop file.
- **Name:** Specifies the name of application.
- **Comment:** Provides brief description or comment about application.
- **Exec:** Defines command to execute when launching application.
- **Icon:** Specifies path to icon file associated with application.
- **Terminal:** Specifies whether application should be run in a terminal window.
- **Type:** Specifies type of entry such as "Application" or "Link."
- **Categories:** Specifies categories or groups under which the application should be displayed in the menu.
- **StartupNotify:** Specifies whether desktop environment should show a startup notification for application.
- **NoDisplay:** Specifies whether application should be hidden from menus.
- **Actions:** Defines additional actions that can be performed on application such as opening a specific file.

## Example DESKTOP file

Here is an example of a .desktop file for a fictitious text editor called "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

In this example, the .desktop file defines application "MyTextEditor" with its associated properties. It also includes two additional actions, "Open New Window" and "Open Existing File," which can be accessed from context menu of application launcher.

By placing a .desktop file in specific directories such as `/usr/share/applications` or `~/.local/share/applications`, the desktop environment will recognize it and display application accordingly in menus or allow it to be launched from desktop.

## How to open DESKTOP file?

Several software programs can open and handle .desktop files. These programs are typically file managers or desktop environments on Linux-based systems. Here are some examples:

- **Nautilus (Files):** The default file manager for GNOME desktop environment.
- **Nemo:** The file manager for Cinnamon desktop environment.
- **Dolphin:** The default file manager for KDE Plasma desktop environment.
- **Thunar:** The default file manager for Xfce desktop environment.
- **KDE Menu Editor:** A tool specific to KDE Plasma desktop environment that allows you to view and edit .desktop files.

These file managers and desktop environments provide graphical interface for managing .desktop files. They allow you to view and edit properties of .desktop files, create application launchers and organize shortcuts in application menus or on the desktop.

The .desktop files are plain text files, so you can also open and edit them with a text editor of your choice. Simply right-click on the .desktop file and select "Open with" or "Open with another application" to choose a text editor from the list of installed programs.

## What is the format of DESKTOP file?

The .desktop file format follows specific structure and format. It is a plain text file with a set of key-value pairs organized into sections. Here is an overview of the format:

- **Section Headers:** Each section begins with a header enclosed in square brackets ([]). The primary section is typically named [Desktop Entry], which contains the main metadata for application or launcher.
- **Key-Value Pairs:** Within each section, you define properties using key-value pairs. The format is "Key=Value". The key identifies property and value provides corresponding data.
- **Property Syntax:** The property values can be of different types including strings, boolean values, file paths or lists. The format for each property value depends on its type.
- **Comments:** You can include comments in .desktop file using '#' symbol. Anything following '#' on line is considered a comment and is ignored.

## References
* [Desktop Entry Files](https://www.baeldung.com/linux/desktop-entry-files)
