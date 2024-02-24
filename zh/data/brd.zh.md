{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BRD 文件 - EAGLE 电路板文件 - 什么是 .brd 文件以及如何打开它？",
  "description" : "了解 BRD EAGLE 电路板文件以及如何打开它。",
  "linktitle" : "BRD",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-brd-zh",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## 什么是 .brd 文件？

BRD 文件格式用于印刷电路板 (PCB) 设计的电子设计自动化 (EDA) 软件。 Eagle、KiCad、Altium Designer 等 PCB 设计软件利用这种文件格式来存储印刷电路板的布局、连接和其他设计相关信息。

BRD 文件是 CAD 文件的一种，是工程师和设计师用来创建、修改和分析设计的数字文件。 BRD 文件与 Autodesk EAGLE 相关联，这是电子行业中常用的用于设计印刷电路板 (PCB) 的软件应用程序。 Autodesk EAGLE 提供了用于原理图捕获（创建电路的可视化表示）和 PCB 布局（安排组件和布线连接）的工具。

BRD 文件是使用 EAGLE 布局编辑器创建的，该编辑器是 Autodesk EAGLE 软件套件的组件。该编辑器允许用户设计 PCB 布局，包括放置元件、布线、定义设计规则以及创建制造所需的文件。

BRD 文件用作 PCB 电子电路设计的模板或蓝图。设计人员使用 EAGLE 和.brd”文件将原理图转换为可制造的物理布局。

.BRD 文件可以以 Gerber 钻孔数据格式保存。 Gerber 文件是 PCB 制造中使用的标准格式，用于描述 PCB 设计的图案、层和功能。以这种格式保存.brd”文件允许计算机辅助制造 (CAM) 程序使用它们，该程序生成制造 PCB 所需的指令。

## BRD 文件查看器

有多种软件工具可用于查看.brd”文件，允许用户可视化和检查使用 Autodesk EAGLE 等软件创建的 PCB 布局。

1.  **Autodesk EAGLE**：如果您有权访问 Autodesk EAGLE，则只需在软件中直接打开.brd”文件即可进行查看和编辑。
    
2.  **KiCad**：KiCad 是一款开源 EDA 软件套件，其中包括 PCB 布局编辑器。它能够导入和查看使用 Autodesk EAGLE 创建的.brd”文件。
    
3.  **ViewPlot**：ViewPlot 是独立的 Gerber 查看器，支持各种 PCB 文件格式，包括.brd”。它允许用户无需原始设计软件即可查看 PCB 设计。
    
4.  **GC-Prevue**：GC-Prevue 是另一种流行的 Gerber 查看器，也可以处理.brd”文件。它提供了可视化 PCB 布局、测量距离和检查设计细节的功能。
    
5.  **Gerbv**：Gerbv是一个开源的Gerber查看器，支持查看Gerber文件，其中可以包括以Gerber格式保存的.brd”文件。
    
6.  **在线查看器工具**：还有一些在线工具可让您直接在网络浏览器中上传和查看.brd”文件。 EasyEDA 的Online Gerber Viewer”就是这样的一个例子，它支持查看各种 PCB 文件格式，包括 Gerber 和.brd”。

## 如何打开 .brd 文件？

PCB 设计中使用的 BRD 文件可以在各种 PCB 设计应用程序中打开。

- **Autodesk EAGLE**：这是由 Autodesk 开发的跨平台 PCB 设计软件。它支持原理图、PCB 布局和电气连接布线的创建。用户可以直接在 Autodesk EAGLE 中打开.brd”文件进行查看和进一步编辑。
    
- **Altium Designer**：Altium Designer 是一款综合性 PCB 设计软件，主要适用于 Windows 操作系统。它提供了广泛的原理图捕获、PCB 布局和设计分析功能。 Altium Designer还支持打开.brd”文件，允许用户导入和使用在其他软件中创建的设计。
    
- **Open Board Viewer**：Open Board Viewer是一款专为Linux操作系统设计的PCB查看软件。它是一个开源工具，允许用户可视化 PCB 布局、检查组件并查看布线详细信息。 Open Board Viewer 支持打开.brd”文件，使 Linux 平台上的用户能够查看和分析在其他软件中创建的设计。

以下是可用于打开 BRD 文件的程序列表。

- **Autodesk EAGLE**（免费试用）适用于（Windows、Mac、Linux）
- **Altium Designer**（免费试用）适用于（Windows、Mac、Linux）
- **开放板查看器**（免费）适用于 Linux

## 参考
* [EAGLE 计划](https://en.wikipedia.org/wiki/EAGLE_(program))


