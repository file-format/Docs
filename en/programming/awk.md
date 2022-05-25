{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "AWK File Format - AWK Script File",
  "description":"Learn about AWK file format and APIs that can create and open AWK files.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-04-03"
}

## What is an AWK file?

An AWK file is a script file created for the text processing application **AWK** that comes bundled with Unix and Linux operating systems. It contains logical instructions to perform actions on text or contents of a file such as matching, replacing and printing text. This helps generate reports and formatted text from the input file. The awk utility is usually located in  /usr/bin/awk on most linux/unix distributions.

## How to Create AWK Script?

An AWK file can be created or opened in any text editor on Linux/Unix OS. A new AWK script file can be created as follow.

```
$ vi script.awk
```

This will open the AWK file in text editor. Enter some statements in the text editor as follow.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
The first line of this text content is explained as follow.

 * \#! – referred to as `Shebang`, which specifies an interpreter for the instructions in a script
 * /usr/bin/awk – is the interpreter
 * -f – interpreter option, used to read a program file

## How to Execute AWK Script?

Save the file and make the script executable by issuing the command below:
```
$ chmod +x script.awk
```

The script can then be run as follow.

```
$ ./script.awk
```

that results in the following output.

```
Writing my first Awk executable script!
```

## Reference ##

* [Write Scripts Using Awk Programming Language](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)
