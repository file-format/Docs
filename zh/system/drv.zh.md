{
  "date" : "2021-07-08",
  "keywords" :["DRV","扩展名","文件","格式","系统","驱动程序","Windows 设备驱动程序","程序","计算机","应用程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Windows 设备驱动程序",
  "description":"了解 DRV 文件格式和可以创建和打开 DRV 文件的 API。",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## 什么是一 .drv 文件？ ##

扩展名为 .drv 的文件属于 Windows 设备驱动程序。 Windows 操作系统使用这些文件连接内部和外部硬盘设备。 DRV 文件包含有关设备和操作系统如何链接在一起的说明和参数。这些文件有助于安装设备驱动程序以在 Windows 中正常运行。此外，通过总线或电缆与 PC 主板链接的设备需要 DRV 文件。


## DRV 文件格式##

DRV 文件通常打包为动态库（[DDL](/zh/system/dll/) 文件）或 [EXE](/zh/executable/exe/) 文件。所有系统平台（例如智能手机）都可以支持这些文件，并且无法保证每个平台都能正确支持这些文件。但是，使用 .drv 文件扩展名的一些最常见的设备是：

* 声卡
* 显卡
* 打印机
* 存储设备
* 网络适配器
* 电脑硬件配件

建议不要打开通过电子邮件发送的 DRV 文件，因为这种文件格式包含病毒和其他恶意程序。确保在打开任何未知的 DRV 文件之前执行全面扫描。


## DRV 示例##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

