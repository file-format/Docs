{
  "date" : "2021-06-29",
  "keywords" :["CUR","扩展名","文件","格式","图像","设备无关位图","光标文件格式","光标","Windows","应用程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - 光标文件格式",
  "description":"了解 CUR 文件格式和可以创建和打开 CUR 文件的 API。",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## 什么是一 .cur 文件？ ##

CUR 文件是一种静态的 Microsoft Windows 光标文件格式。基本上，它们是与 ICO（图标）文件相同的固定图像，除了扩展名之外。 CUR和[ICO](/zh/image/ico/)都是基于Device-Independent Bitmap [DIB](/zh/image/dib/)（Device-Independent Bitmap）规范建立的。默认值以及自定义光标（例如用于 Windows 操作系统的 Windows 鼠标指针）都存储在 CUR 文件中。它可以是正常使用的箭头，可以是显示等待时间的旋转沙漏，也可以是用于文本编辑的 I-bar。 CUR 文件随自定义桌面主题的安装包一起提供，以确保 Windows 光标与自定义桌面主题匹配。

## 技术规格##

CUR 文件是二进制系统文件，可以在运行 Microsoft Windows 操作系统的设备上找到。 CUR 指针图像有不同的标准尺寸，如 16×16、32×32 等。CUR 文件与 ICO 文件非常相似；它们都由小的静止图像组成。只有 CUR 和 ICO 文件的扩展名不同。此外，CUR 文件头中对热点的解释与 ICO 文件不同。热点解释从左上角到您指向鼠标的位置的像素偏移。 Windows 系统仍在使用 CUR 文件，但现在动画光标通常具有文件扩展名 ANI 而不是 CUR。

## 历史简介 ＃＃

CUR 文件由 ICO 文件制成。第一个 CUR 文件格式于 1981 年并入 Microsoft 的 Windows 1.0 操作系统，以使商业使用更加顺畅。很快，更多的交互式光标被引入，允许用户从可用的预安装选项修改他们的光标首选项。但是，即使您没有足够的技术知识，也很容易自己编辑 CUR 文件。


## CUR 示例 ##

CUR 文件可以在 *C:\Windows\Cursors* 中找到：

{{< figure src="../cur.png" alt="CUR 文件格式" >}}

