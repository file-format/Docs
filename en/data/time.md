{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TIME File - What is .time file? Time when File was created in Linux",
  "description" : "Learn about TIME file and find out Time when file was created in Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-02-08"
}

## What is a TIME file?

TIME file format was used by a web system called LIGHT, which helped users record, organize, and share their lives. Essentially, it stored a collection of posts and represented a folder on the user's life page within the system.

## How to Find Out When a File Was Created in Linux

In Linux and al its variants like Ubuntu, Fedora, Linux Mint, etc. you can use the `stat` command to find out when a file was created. Here is how you can do it:

Open a terminal and type the following command:

```
stat <file_path>
```

Replace `<file_path>` with the path to the file you are interested in. For example:

```
stat /path/to/your/file.txt
```

This command will display various information about the file, including its creation time. Look for the line that starts with "Birth" or "File:". The "Birth" time indicates when the file was created on the filesystem.

Here is an example of what the output might look like:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

In this example, the "Birth" time indicates when the file was created.

## References

* [Take Screenshot on Linux Mint](https://how-to-take-screenshot.com/take-screenshot-on-linux-mint/)