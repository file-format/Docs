{
  "date" : "2020-08-20",
  "keywords" :["fon 文件","fon 文件格式","什么是 fon 文件","文件","fon 示例","fon 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - 字体库文件",
  "description":"了解 FON 文件格式和可以创建和打开 FON 文件的 API。",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## 什么是一 .fon 文件？

带有 .fon 扩展名的文件是 Microsoft Windows 3.x 字体库，它实际上是一个可执行文件，但重命名为 .fon。它本身是 [.fnt](/zh/font/fnt/) 文件的集合，应用程序在访问系统字体时会引用它。这就是为什么它充当资源文件的原因。它可以在 Windows 操作系统上使用 Microsoft Windows Font View 应用程序打开。

## FON 文件格式

FON 文件包含字体资源并具有资源 (.res) 文件格式。 .res 文件格式指定文件头和数据段规范。 .fnt 也是资源文件中包含的资源数据文件。 FON 文件具有二进制文件格式并具有 application/octet-stream MIME 类型。

与其他类型的资源不同，字体资源不会添加到应用程序的资源中。相反，它们被添加到 EXE 文件中并重命名为 .fon 文件，从而生成库文件而不是应用程序。多个单独的字体构成字体组的组件，其中每个组都遵循资源组结构。字体资源使用这些资源组结构。组头包含从组中访问特定字体所需的所有信息。字体组件资源具有以下格式。
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/zh/font/fnt/) file)
```
单个 .rc 资源文件可以有混合的资源声明。字体组可以位于资源文件中的任何位置，并且不必是连续的。创建 .RES 文件的程序必须添加 FONTDIR 的手动输入。以下是组头的结构。

```
[普通资源头（类型 = 7）]

字数字体； // .RES 文件中的总数
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
struct FontDirEntry {
WORD df版本；
DWORD dfSize;
char df版权[60]；
字 df 类型；
WORD dfPoints;
字 dfVertRes;
字 dfHorizRes;
单词 dfAscent;
WORD dfInternalLeading；
WORD dfExternalLeading；
字节df斜体；
字节df下划线；
字节 dfStrikeOut;
字df重量；
字节 dfCharSet;
字 dfPixWidth;
字 dfPixHeight;
字节 dfPitchAndFamily；
字 dfAvgWidth;
字 dfMaxWidth;
字节 dfFirstChar;
字节 dfLastChar;
字节 dfDefaultChar；
字节 dfBreakChar;
字 dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD df 保留；
字符 szDeviceName[];
字符 szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

