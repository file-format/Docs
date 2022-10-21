{
  "date" : "2020-03-16",
  "keywords" :["IGS 文件","文件格式","CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 IGS 文件格式和可以创建和打开 IGS 文件的 API。",
  "title" :"IGS 文件格式：2D-3D 设计交换文件",
  "linktitle" : "IGS",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-28"
}

## 什么是一 .igs 文件？

具有 .igs（初始图形交换）扩展名的文件是一种 2D-3D 设计交换文件格式，它独立于 CAD 应用程序使用的源或目标文件格式规范。它用于在两个独立系统之间交换有关电路图、线框、自由曲面的设计信息。它类似于 [IGES](/zh/cad/iges/)，是制造商为您的产品定价和设计模具的主要要求。 IGS 最近已被更新的 STEP(.STP) 文件格式取代。 IGS 文件可以由 Autodesk、FreeCAD、CADEX CAD Exchanger 和其他类似应用程序等应用程序打开。

## IGS 文件格式

IGS 文件是 ASCII 文本文件格式，可以用任何文本编辑器打开。 IGS 文件中的每条记录长度为 80 个字符。 CAD 应用程序以 IGS 文件格式保存和导出矢量数据，以便在不同软件包之间传输 3D 模型文件。虽然 IGS 文件可以在任何文本编辑器中打开，但模型或设计只能由支持 IGS 文件格式的可视化应用程序查看。

## 参考
* [维基百科的 IGES](https://en.wikipedia.org/wiki/IGES)

