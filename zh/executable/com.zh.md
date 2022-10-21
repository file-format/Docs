{
  "date" : "2021-06-29",
  "keywords" :["com 文件","什么是 com 文件","文件","com 示例","com 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 COM 文件格式和可以创建和打开 COM 文件的 API。",
  "title" :"COM - DOS 命令文件格式",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## 什么是一 .com 文件？
COM 文件仅用于执行一组命令或指令。 COM 文件由一个可执行程序组成，该程序能够从 Windows 或 MS-DOS 运行。与 EXE 文件一样，COM 文件也以二进制格式保存，但它与 EXE 文件不同，因为它没有标题或元数据，并且最大大小约为 64KB。当 COM 文件第一次在 32 位系统上运行时，它会提示安装 NT Virtual DOS Machine (NTVDM) 组件。 COM 文件可以在带有支持 MS-DOS 环境的虚拟机的 64 位版本的 Microsoft Windows 上运行。

## COM 文件格式
COM 文件格式是在 Microsoft Windows 或 MS-DOS 中使用的二进制可执行格式。它的结构仅由一组指令组成；它没有标头，也不包含标准元数据。它将所有数据和代码仅存储在一个段中，其二进制文件的最大大小为 64KB。尝试重新运行时，此文件格式不会自行重新定位。因此操作系统将其加载到预设地址。此外，可以使 COM 文件以 **fat binary** 的形式在两个操作系统下执行。在指令级没有任何实际的兼容性。入口点的指令选择在两个操作系统中功能相同但不同，并使程序运行，跳转到操作系统正在使用的部分。它基本上是两个不同的程序，在一个文件中具有相同的程序，前面是选择要使用的程序的代码。
### COM 文件示例
执行 COM 文件时，从第一个字节开始读取指令，然后连续执行，直到找到最后一条指令。这是一个 ASM 代码示例：

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## 参考

* [COM 文件 - 由 Wikipewdia 提供](https://en.wikipedia.org/wiki/COM_file)

