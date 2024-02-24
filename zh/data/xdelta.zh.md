{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XDELTA 文件 - xdelta 差异文件 - 什么是 .xdelta 文件以及如何打开它？",
  "description" : "了解 xdelta 差异文件以及如何打开它。",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta-zh",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## 什么是 XDELTA 文件？

XDELTA 文件格式保存两个其他文件之间的二进制差异，由 xdelta 工具生成，xdelta 工具是用于增量编码的命令行实用程序，其中涉及计算两个文件之间的差异并以紧凑格式对这些差异进行编码。 XDELTA 文件存储表示原始文件和更新文件之间的更改或差异的二进制数据。 XDELTA 文件中的二进制数据表示将一个文件（原始文件）转换为另一个文件（更新或修补版本）所需的更改。

XDELTA 文件经常在游戏社区中用于分发视频游戏的修改 (mod)。这些模组可以包括从外观变化到游戏机制重大改变的任何内容。 XDELTA 文件允许用户通过使用 XDELTA 文件中指定的更改修补原始游戏文件，将这些修改应用到其游戏安装中。

## 三角洲

`xdelta` 是一个用于增量编码和解码的命令行实用程序；它主要用于在两个文件之间创建和应用二进制补丁，通常称为增量补丁”或x增量补丁”；这些补丁代表原始文件与修改或更新版本之间的差异，允许有效分发更新，特别是在带宽或存储空间有限的情况下。

以下是 `xdelta` 主要功能的简要概述：

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

xdelta”通常用于各种场景，例如分发软件更新、修补视频游戏以及更新嵌入式设备或网络设备中的系统文件。它提供了一种灵活有效的方式来管理文件更新，同时最大限度地减少带宽使用和存储要求。

## 德尔塔用户界面

xdeltaui 是一个图形用户界面 (GUI) 应用程序，用于管理和应用 XDELTA 补丁。 xdelta gui提供了一个用户友好的界面，供用户与XDELTA文件交互并将其应用到相应的原始文件，有效地修补或更新它们。

与通过基于文本的命令操作的 xdelta 命令行版本不同，xdeltaui 提供了一种更直观的方式来处理 XDELTA 文件，特别是对于不熟悉命令行界面或喜欢图形工具的用户。

使用xdeltaui，用户通常可以执行诸如选择原始文件、选择XDELTA补丁文件以及应用补丁来生成更新文件等任务。这对于安装视频游戏或其他软件应用程序的模组或更新特别有用。

## 下载

在 Linux 系统上，您可以使用apt”、yum”或dnf”等包管理器来安装xdelta”。例如，在 Ubuntu 上，您可以使用以下命令：

```
sudo apt-get install xdelta3
```

## 如何使用xdelta

要使用xdelta”，您通常需要遵循以下一般步骤：

1.  **下载并安装**：首先，确保您的系统上安装了xdelta”。您可以从其官方网站、包管理器或其他可信来源下载它。
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **创建补丁**：
    
- 打开命令行界面（终端或命令提示符）。
- 使用带有适当选项的xdelta”命令来创建补丁。基本语法是：
               
````
x 德尔塔 德尔塔<original_file><updated_file><patch_output_file>
````
        
替换 `<original_file> ` 带有原始文件的路径，`<updated_file> ` 包含更新文件的路径，以及 `<patch_output_file> ` 带有所需的补丁文件名称。
- 例子：
               
````
xdelta delta 原始文件 更新文件 patch.xdelta
````
        
4.  **应用补丁**：
    
- 确保您有可用的原始文件和补丁文件。
- 打开命令行界面。
- 使用带有适当选项的xdelta”命令来应用补丁。基本语法是：
        
      
````
xdelta补丁<original_file><patch_file><output_file>
````
        
替换 `<original_file> ` 带有原始文件的路径，`<patch_file> ` 以及补丁文件的路径，以及 `<output_file> ` 具有所需的输出文件名称。
- 例子：
                
````
xdelta 补丁原始文件 patch.xdelta 更新文件
````
        
5.  **查看帮助**：如果您需要特定选项或命令的帮助，您可以使用带有--help”选项的xdelta”命令来显示使用信息和可用选项。
    
## 如何打开 XDELTA 文件

XDELTA 文件不适合直接打开。如果您希望将 XDELTA 补丁应用于游戏或其他文件，您可以选择使用跨多个平台兼容的 xdelta 或专为 Windows 用户设计的 xdelta UI。

## 参考
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)


