{
  "date" : "2021-06-29",
  "keywords" :["CFG","扩展名","文件","格式","系统","配置","设置","程序","计算机","应用程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - 文件格式",
  "description":"了解 CFG 文件格式和可以创建和打开 CFG 文件的 API。",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## 什么是一 .cfg 文件？ ##

具有 .cfg 扩展名的文件是一种“设置"文件。它是一种常用的文件类型，用于存储有关计算机程序配置和设置的信息。大多数类型的 CFG 文件都以文本格式存储，不应手动打开，而应使用文本编辑器打开。但是，有不同类型的 CFG 文件，它们存储信息的格式不同。 CFG 文件提供的功能因应用程序而异。一些计算机应用程序使用户能够通过使用图形干扰来修改或开发他们的配置文件语法，而其他计算机应用程序只允许使用文本编辑器进行修改。在修改这些文件后，用户可以指示应用程序再次读取这些文件并将修改应用到系统中。


## CFG 文件格式 ##

CFG 文件受到各种操作系统的支持，例如 Unix 和类 Unix 操作系统、MS-DOS、macOS、Microsoft Windows 和 IBM OS/2。这些文件在这些操作系统中的存储和使用格式各不相同。大多数系统以人类可读和可编辑的纯文本格式使用和存储这些文件，而其他系统则以更复杂的格式存储这些文件，具体取决于文件使用情况和操作系统的要求。

在 Unix 和类 Unix 操作系统中，大多数 CFG 文件使用几种不同的 CFG 文件格式样式，但是，最常见的格式是易于阅读的纯文本格式，并且几乎所有格式都允许进行注释和编辑。这些操作系统中 CFG 文件最常见的文件扩展名是 CNF、CONF、CF 和 INI。

在 MS-DOS 操作系统中，最初只有一种配置文件格式，即纯文本，但是，MS-DOS 6 引入了 INI 配置文件格式。

macOS 使用标准的属性列表格式样式配置文件。

在 Microsoft Windows 中，纯文本 INI 样式的配置文件是存储和编辑信息的重要来源，然而，1993 年引入了新的数据库系统，导致 1993 年后 Microsoft Windows 中配置文件的使用减少。


## CFG 示例 ##

示例 CFG 文件如下所示：

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```
