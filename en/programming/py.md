---
date: 2020-24-11
keywords: py, python, .py, py file format, how to open py files, how to run py files, how to run python files, how to run python
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: What are PY files?
linktitle: PY
description: .py files contain the Python source code that can be executed on multiple platforms.
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## What are PY files? ##

Files with the .py extension contain the python source code. It is a very popular language that can be used for web development, software development, mathematics, and system scripting. Python is a cross-platform language that can work on different platforms like Windows, MAC, Linux, Raspberry Pi, etc. Python provides a simple syntax that is similar to the English language and is easier to read. Pythons syntax allows programs to be written with fewer lines of code. Python runs on an interpreter system so the code can be executed as soon as it is written which makes it very good for prototyping.

## Brief History ##

Python was conceived in the late 1980s by Guido van Rossum as a successor to ABC programming language. Its implementation began in December 1989 with Van Rossum as the sole lead developer. He worked on python until 12 July 2018. In January 2019, the active Python core developers elected a five-member "Steering Council" comprising of Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw, and Van Rossum to lead the project.

### Versions ###

- Python 2.0 was released on 16 October 2000.
- Python 3.0 was released on 3 December 2008.

## How to open Python files ##

To open Python files, you can use the following:

- Notepad (this will not execute the script)
- VS Code
- Visual Studio
- PyCharm

## How to run/execute Python files ##

To check the version of Python installed, you can use the following command:

```cmd
python --version
```

This will output the version on the console like

```cmd
Python 3.7.4
```

If Python is not installed on your machine, you can go to [python.org](https://www.python.org/) and download and install Python for your relevant operating system.

To execute a Python script, you can use the following command:

```cmd
python helloworld.py
```

*helloworld.py* is a script file that contains the following code

```py
print("Hello World from Python")
```

This will print the following on the console window.

```cmd
Hello World from Python
```

Note: If you use IDEs, they provide buttons on the screen or different keyboard shortcuts to run Python. For example, a play button is shown in the gutter with the editor in PyCharm that lets you execute the Python script.

## PY File Format ##

Python was designed for readability and has similarities to English and Math. Python uses new lines to indicate the complete command as opposed to semicolons or parenthesis used in other languages. For scopes, loops, and functions, Python relies on indentation and whitespaces as opposed to curly braces used in other languages.

### Syntax ###

The following is an example of Python syntax.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## References ##

- [Python Introduction - W3schools](https://www.w3schools.com/python/default.asp)
- [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))
