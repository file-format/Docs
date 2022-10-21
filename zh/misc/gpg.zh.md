{
  "date" : "2022-02-17",
  "keywords" :["gpg 文件","gpg 文件格式","什么是 gpg 文件","文件","gpg 示例","gpg 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPG 文件 - GNU 隐私保护公共密钥环文件",
  "description":"了解 GPG 文件和可以创建和打开 GPG 文件的 API。",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## 什么是一 .gpg 文件？

GPG 文件是 GNU Privacy Guard (GnuPG) 加密程序使用的加密/解密密钥文件。 GnuPC 程序本身基于定义为 RFC4880 的 OpenPGP 标准，也称为 PGP。在现代操作系统中成功使用 GPG 的关键是其多功能的密钥管理系统。 GPG 的命令行实用程序使其可以轻松地与其他应用程序集成。

## GPG 文件格式

GPG 文件被保存为加密的二进制文件，当然它们不是人类可读的。要解密加密的 GPG 文件，您需要使用相同的安全密钥。这就是为什么这些文件的内部文件格式未知的原因。

## 在 Linux 上使用 GPG 加密和解密文件

GPG 命令行实用程序可用于在 Linux 上加密和解密文件。

### 加密文件

可以使用带有 -c（创建）选项的 gpg 命令对文件进行加密，如下所示。

```
gpg -c file1.txt
```
运行此命令会要求输入用于加密原始文件 `file1.txt` 的内容的密钥短语。这将导致创建加密文件 file1.txt.gpg。

### 解密和提取文件

为了解密和提取加密文件，可以使用以下命令。

```
gpg cfile.txt.gpg
```

## 参考

* [GNUPG](https://gnupg.org/)
* [HDF - 维基百科](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

