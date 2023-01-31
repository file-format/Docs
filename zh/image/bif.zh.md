{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BIF 文件 - Ventana 全幻灯片图像格式",
  "description":"了解 BIF 文件格式和可以创建和打开 BIF 文件的 API。",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## 什么是 .BIF 文件？

BIF 文件是包含载玻片标本图像的光栅图像文件。它包含多个 TIFF 图像，这些图像由幻灯片查看应用程序组合成单个合成图像。 BIF 文件由 Ventana Medical 系统数字幻灯片扫描仪创建，完全符合 [TIFF](/zh/image/tiff/) v 6.0 定义的 BigTIFF 变体。

## BIF 文件格式

BIF 文件保存为二进制图像文件，包含多达 200,000 x 200,000 像素。这会导致文件变大，从而打破由 TIF 标准定义的 32 位文件指针强加的 4 GB 大小限制。然而，对于 64 位文件指针，TIFF 标准的 BigTIFF 变体克服了这个文件大小障碍。

### 谁使用 BIF 文件？

BIF 文件被数字载玻片扫描仪用来扫描和创建载玻片标本的数字副本。如果您是病理学家，则可以在幻灯片查看应用程序中打开这些 BIF 文件。凭借高水平的细节和高分辨率数据，您可以放大和缩小幻灯片图像以或多或少地查看标本切片的细节。这些文件中的 [XML](/zh/web/xml/) 元数据文件定义了图像的组合方式，以及应该用作文件缩略图的图像。

## 如何打开 BIF 文件？

您可以使用以下命令打开 BIF 文件：

* OpenSlide（跨平台）
* ImageJ（跨平台）
* NetScope 查看器 (Windows)

## 参考 ＃＃

* [罗氏数字病理学 BIF 白皮书](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

