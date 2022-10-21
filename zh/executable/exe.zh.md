{
  "date" : "2021-06-30",
  "keywords" :["exe文件","exe文件格式","什么是exe文件","文件","exe示例","exe文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":".exe 文件是在 Windows 操作系统上运行的 Microsoft 可执行文件。了解有关 EXE 文件格式的更多信息。",
  "title" :"什么是可执行的 EXE 文件？",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## 什么是 .exe 文件？

EXE 是 **executable** 的缩写。 .exe 文件是可以在 Microsoft Windows 操作系统上执行的程序。应用程序开发人员大多以可执行格式将他们的 Windows 操作系统程序发布为 exe 文件。它是在 Windows 上运行应用程序的标准文件格式。 **Setup.exe**、**Install.exe** 和 **cmd.exe** 是一些常见且熟悉的 EXE 文件名称。

## EXE 文件格式

MS-DOS 编译器是随具有 64K 内存限制的内存模型引入的。一般的概念是在x86 CPU（CS、DS、ES、SS）中设置不同的段寄存器指向不同或相同的段，从而允许不同程度的访问内存。一些特定的内存模型是：

- **Tiny**：所有内存访问都是 16 位的（段寄存器不变）。生成 .COM 文件而不是 .EXE 文件。
- **小**：所有内存访问都是 16 位的（段寄存器不变）。
- **紧凑**：数据地址包括段和偏移量，在访问时重新加载 DS 或 ES 寄存器并允许高达 1M 的数据。代码访问不会改变 CS 寄存器，允许 64K 的代码。
- **中**：代码地址包括段地址、访问时重新加载 CS 并允许最多 1M 的代码。数据访问不会更改 DS 和 ES 寄存器，允许 64K 数据。
- **大**：代码和数据地址都是（段，偏移）对，总是重新加载段地址。整个 1M 字节的存储空间可用于代码和数据。
- **Huge**：与大型模型相同，编译器生成额外的算术以允许访问大于 64K 的数组。

开发人员必须在创建 exe 文件时决定应该选择哪个模型。

### 便携式 EXE 文件格式

可移植可执行文件格式 (PE) 包含许多信息标头，以下是标头列表：

- **DOS 标头**：MS-DOS 标头确保向后兼容或优雅地拒绝新文件类型。
- **PE Header**：在从 DOS 头开始的偏移量 60 (0x3C) 处是指向 PE 文件头的指针
- **COFF 标头**：COFF 标头包含一些对可执行文件有用的信息，以及一些对目标文件更有用的信息。
- **PE 可选标头**：PE 可选标头直接出现在 COFF 标头之后，一些来源甚至将这两个标头显示为同一结构的一部分。
- **Section Table**：紧接在 PE Optional Header 之后，我们找到了一个节表。节表由一组 IMAGE_SECTION_HEADER 结构组成。
- **可映射部分**：可以通过将库的代码映射到多个进程来节省内存空间。

## 可以在 Mac 上运行 EXE 文件吗？

Exe 文件不用作 Mac OS 上的可执行文件。但是，如果要在 Mac OS 上运行 exe 文件，可以使用以下方法。

1. **Wine** - 对于想要在 Mac 系统上使用 PC 应用程序的人来说，Wine 是完美的解决方案。这是一个首字母缩写词，代表“Wine Is Not A Emulator"的意思。 Wine 创建与 Microsoft 相同的目录环境，因此您可以使用它运行您的 Windows 应用程序。
2. **虚拟机** - 使用 Parallel Desktop 或 VM Virtual Box 创建 Windows 虚拟机，并在虚拟机中运行您的应用程序。
3. **Boot Camp** - 在 Mac OS 上安装和配置 Windows Boot Camp 让您可以在 Mac 机器上运行 Windows OS。

## 参考

* [.exe- 维基百科](https://en.wikipedia.org/wiki/.exe)
* [x86 反汇编/Windows 可执行文件](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

