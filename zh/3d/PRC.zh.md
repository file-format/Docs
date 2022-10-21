---
date: 2019-10-11
keywords: "prc, .prc, prc 文件格式, 如何打开 prc 文件, .prc 扩展名, prc 扩展名"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "中华人民共和国文件格式"
linktitle: "中华人民共和国"
description: "了解 PRC 文件格式和可以创建和打开 PRC 文件的 API。"
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## PRC 文件格式
“.prc"扩展名用于产品表示压缩 3D 文件格式和 MobiPocket 的电子书文件格式。

## 什么是产品表示契约 (PRC) 文件？

PRC (Product Representation Compact) 是一种 3D 文件格式，经过优化以存储、加载和显示 3D 数据，尤其是来自 CAD（计算机辅助设计）系统的数据。它是一个顺序二进制文件，以可移植的方式编写。 PRC 可用于在 PDF 文件中嵌入 3D 数据。 PRC 支持 CAD 的大多数主要结构，例如装配体和零件、3D 实体树、精确几何表示、三角表示和标记。 PRC 使用 .prc 扩展名，使用的 Internet 媒体类型是 *model/prc*。

PRC 是一种多用途文件格式，根据其用途，既可以使用常规压缩存储以直接表示 CAD 数据，也可以使用高压缩存储以减小文件大小。使用 PRC 格式存储在 PDF 中的 3D 数据可与 CAM 和 CAE 应用程序互操作。

### 产品表示压缩 (PRC) 文件格式规范

一个PRC文件有一个主要的标题部分，后面是一个或多个文件结构，最后是一个模型文件。一个文件结构有一个标题，后跟以下数据部分：

- **Globals**：它包含文件结构的每个树实体的引用文件结构和颜色、线条样式和坐标系。
- **树**：它包含项目树的描述，如产品出现、部件定义、表示项目和标记。
- **镶嵌**：它包含树的叶实体（表示项和标记）中的所有镶嵌（三角）数据。
- **几何**：它包含树的叶子实体的所有精确几何和拓扑数据（表示项）。
- **额外几何体**：它包含几何体的摘要数据。这允许在不加载整个几何图形的情况下部分加载文件。

下面是一个典型的PRC文件的结构。

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## 什么是带有PRC扩展名的MobiPocket电子书文件
由一家名为 **Mobipocket** 的法国公司推出的电子书文件格式也使用扩展名“.prc"。最初，Mobipocket 推出了适用于平板电脑、PDA 和智能手机等多种智能设备的免费应用程序。 “.prc"扩展名实际上与 .mobi 相同，但特别用于仅支持 **.prc** 或 **.pdb** 扩展名的 PDA。

### Mobipocket PRC 文件格式规范
MobiPocket PRC 文件格式基于使用 XHTML 的 Open eBook 标准，还可以包含 JavaScript 和框架。还可以支持与嵌入式数据库一起使用的本机 SQL 查询。

Mobipocket 阅读器有一个主页库。读者可以在书籍的任何部分插入空白页并添加可变图纸。注释、书签、更正、注释和绘图等对象可以从一个位置进行管理。图像被转换为GIF格式，最大尺寸为64K，对于小屏幕手机来说已经足够了。 Mobipocket Reader 具有电子书签和内置字典。

该阅读器具有全屏模式，可用于阅读和支持许多 PDA、通信器和智能手机。 Mobipocket 产品支持大多数 Palm 操作系统、Windows、Symbian、BlackBerry，但不支持 Android。阅读器使用 WINE 在 Linux 或 Mac OS X 下工作。

## 参考

- [中国 - 维基百科](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC 格式规范](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [电子书格式比较 - 维基百科](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

