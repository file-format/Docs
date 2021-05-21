{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SH - Bash Shell Script File",
  "description":"Learn about SH file format and APIs that can create and open SH files.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-05-21"
}

## What is a SH file?

A file with .sh extension is a scripting language commands file that contains computer program to be run by Unix shell. It can contain a series of commands that run sequentially to carry out operations such as files processing, execution of programs and other such tasks. These are executed from the command line interface by user or in batch to carry out multiple operations at the same time. Script files can be opened in text editors like Notepad, Notepad++, Vim, Apple Terminal and other similar applications on Windows, MacOS and Linux OS.

## SH File Format

SH files are written in plain text following the defined syntax. These script files support:

 * `Comments` - Comments start with a # and are ignored by the shell.
 * `Shortcuts` - These can be used to rename a command for short and easy execution.
 * `Batch Jobs` - Several commands can be be executed automatically that would otherwise need to be entered manually. This removes the need to wait for a user to trigger each stage of the sequence.
 * `Generalization` - Using simple loops, much more generalization is achieved for operations such as conversion of images from one fromat to another.

## SH file example

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## How to run SH file?
The SH files usually run on Linux, even in Windows you need to connect with a Linux terminal using softwares such as Putty to run the sh files. Following are the steps to run an SH file on a Linux terminal.

1. Open the Linux terminal and go to the directory where the SH file is located.
2. By Using `chmod` command, set execute permission on your script (if not set already).
3. Run script using one of the following
	1. `./filename.sh`
	2.  `sh filename.sh`
	3.  `bash script-name-here.sh`

## References

* [Bashscripting for Beginners](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)
