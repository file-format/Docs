{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPIO 文件 - Unix CPIO 存档文件格式",
  "description":"了解什么是 CPIO 文件以及可以创建和打开 CPIO 文件的 API。",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## 什么是一 .cpio 文件？

CPIO 文件是以 Unix 的 Copy In Copy Out (CPIO) 格式创建的存档文件。除了未压缩之外，它与 TAR 文件格式类似。 CPIO文件可以存储设备文件、符号链接和扩展文件属性。

## CPIO 文件格式

CPIO 存档被创建为人类无法读取的二进制文件。它存储文件和目录的集合。 CPIO 存档的内容通过文件名、权限、所有权和时间戳等元数据信息进行标识。该元数据信息也存储在存档文件中，以供系统横向访问。

## CPIO 存档的格式

CPIO 文件由一个或多个串联的成员文件组成。存档中的每个文件都包含一个标头（可选地后跟标头中提到的文件内容）。存档末尾包含另一个标头，该标头由名为 TRAILER!! 的空文件描述。

### CPIO 档案的类型

CPIO 档案有两种类型。它们仅在标题样式上有所不同。

* ASCII 存档 - 这些 CPIO 存档具有可打印的标头，如果存档本身由 ASCII 文件组成，该标头将成为 CPIO 存档的一部分
* 二进制存档 - 这些 CPIO 存档具有二进制标头。

## 使用 CPIO 存档

### 如何创建 CPIO 档案？

您可以使用 **cpio** 命令在类 Unix 系统上创建 CPIO。以下命令将查找当前目录及其子目录中的所有文件和目录。然后，此输出通过管道传输到 cpio 命令，该命令将生成名为 archive.cpio 的新 CPIO 存档。

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### 如何从 CPIO 档案中提取文件？

以下命令从现有存档中提取文件。

```
cpio -id < archive_cpio.cpio
```
它将从标准输入读取 archive.cpio 文件并将文件提取到当前目录。


## 参考

* [CPIO - 来自维基百科](https://en.wikipedia.org/wiki/Cpio)
* [CPIO 文件格式](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

