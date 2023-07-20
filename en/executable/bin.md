{
   "date":"2023-07-20",
   "keywords":[
      "BIN",
      "BIN File",
      "file",
      "BIN file extension",
      "extension",
      "file"
   ],
   "author":{
      "display_name":"Shakeel Faiz"
   },
   "draft":"false",
   "toc":true,
   "title":"BIN File Format - Unix Executable File",
   "description":"Learn about BIN format and APIs that can create and open BIN files.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
      }
   },
   "lastmod":"2023-07-20"
}

## What is a BIN file?

A BIN file is an executable file on Unix-based operating systems such as Linux or FreeBSD. It holds a compiled program composed of binary code derived from source code, making it compatible with the underlying system architecture. Unix Executable BIN files can be compared to Windows .EXE files and macOS .APP files in terms of their role as executable formats.

In the domain of software development for Unix systems, BIN files are commonly employed by developers to package and distribute programs. They offer a convenient means of delivering software to users, allowing for easy installation and execution. Alongside BIN files, there exist other types of Unix executables, including [.ELF](/executable/elf/), .X86, [.RUN](/executable/run/), and .X86_64, each tailored to specific hardware or system requirements.

When it comes to the internal structure of a BIN file, it consists of encoded data that the Unix operating system utilizes to identify, read, and execute the enclosed program. The system relies on specific file signatures or headers to recognize the BIN file as an executable, followed by the interpretation and execution of the binary instructions contained within.

BIN files often come bundled with an accompanying **INSTALL.TXT** file, which provides detailed instructions on how to properly install and set up the program. This documentation ensures that users can navigate the installation process successfully and begin utilizing the software without complications.

## How to open BIN file?

BIN files are not designed to be directly opened and viewed. However, you can execute the programs or extract the data they contain. To access the contents of a BIN file, follow these steps on the command line, assuming the name of the BIN file is "sample.bin":

1. **Ensure executable permissions:**

Before executing the BIN file, ensure it has the necessary permissions to be run as an executable. Use the command:

```
$ chmod +x sample.bin
```

This command grants the file executable privileges.

2. **Execute the BIN file:**

After setting the executable permissions, you can run the BIN file by entering the following command:

```
$ ./sample.bin
```

**Warning**

_Exercise caution when dealing with downloaded or emailed BIN files, as they can potentially be used by cybercriminals to distribute malware. Only run BIN files from trusted sources to mitigate the risk of malicious executable attacks._

## References

* [How to Execute Binary Files in Linux](https://linuxhint.com/execute-binary-files-in-linux/)

