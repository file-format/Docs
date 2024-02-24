{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME 文件 - 什么是 .time 文件？ Linux中文件创建的时间",
  "description" : "了解 TIME 文件并找出 Linux 中文件创建的时间",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-zh",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## 什么是TIME文件？

TIME 文件格式由名为 LIGHT 的网络系统使用，该系统帮助用户记录、组织和分享他们的生活。本质上，它存储了帖子的集合，并代表系统内用户生活页面上的一个文件夹。

## 如何在 Linux 中查找文件的创建时间

在 Linux 中，您可以使用stat”命令来查明文件的创建时间。您可以这样做：

打开终端并键入以下命令：

```
stat <file_path>
```

替换 `<file_path> ` 替换为您感兴趣的文件的路径。例如：

```
stat /path/to/your/file.txt
```

该命令将显示有关文件的各种信息，包括其创建时间。查找以出生”或文件：”开头的行。 出生”时间表示文件在文件系统上创建的时间。

以下是输出的示例：

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

在此示例中，出生”时间表示文件的创建时间。

