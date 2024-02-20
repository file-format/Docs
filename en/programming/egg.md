{
  "date": "2022-03-15",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "EGG File Format - Python Distribution File",
  "description": "Learn about EGG file format and APIs that can create and open EGG files.",
  "linktitle": "EGG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-egg"
    }
  },
  "lastmod": "2022-03-15"
}

## What is an EGG file?

An EGG file, also known as Python eggs, is an older distribution format Python distributions. It is a [ZIP](/compression/zip/) compressed archive with .egg extension and contains the Python application's source files along with meta information about the distribution. EGG files are alternative to a Windows Executable [EXE](/executable/exe/) file but is cross-platform. This older format for Python distributions has been replaced with the newer Wheel (WHL) file format in early 2010.

## EGG File Format

EGG files are saved as compressed ZIP archives. It means that if you replace the .egg extension with .zip, you will be able to open it with standard decompression utilities such as Corel WinZIP, Microsoft Explorer, or RARLAB WinRAR.

EGG files can be created using the **distutils** package available by Python. Another tool that can create and open EGG files is **SetupTools**. EGG files can be installed as a package using **easy_install**.

`NOTE - EGG file format has been obsoleted in favor of the new wheel WHL file format.`

## Reference ##

* [Python EGGs](https://python101.pythonlibrary.org/chapter38_eggs.html)
