{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PET 文件格式 - Puppy Linux 安装包文件",
  "description":"了解 PET 文件格式和可以创建和打开 PET 文件的 API。",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## 什么是 Linux PET 文件？

PET 文件是与 Linux 操作系统的 PuppyLinux 变体一起创建和使用的应用程序安装包文件。它被创建为压缩的 [TGZ](/zh/compression/tgz/) 文件，可减小压缩存档的文件大小。 PET 文件格式的完整性由附加到文件末尾的 md5sum 校验和来确保，以便在远程端进行验证。可以使用标准的 TGZ 文件提取器和 WinRAR 提取 PET 文件。 PET 文件替换了旧的 [PUP](/zh/compression/pup/) 软件包安装文件。

## PET 文件格式

PET 文件以二进制文件格式作为压缩档案保存到光盘中。但是，PET 文件格式的内部文件格式细节尚不清楚。与 [.exe](/zh/executable/exe/) 和 [.msi](/zh/executable/msi/) 软件包安装文件类似，PET 文件在执行时开始安装。

## 参考

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [PuppyLinux PET 软件包索引](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

