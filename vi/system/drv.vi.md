{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "phần mở rộng", "tệp", "định dạng", "hệ thống", "Trình điều khiển", "Trình điều khiển thiết bị Windows", "chương trình", "máy tính", "ứng dụng" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Trình điều khiển thiết bị Windows",
  "description":"Tìm hiểu về định dạng tệp DRV và API có thể tạo và mở tệp DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Tệp DRV là gì? ##

Các tệp có phần mở rộng .drv thuộc về Trình điều khiển thiết bị Windows. Hệ điều hành Windows sử dụng các tệp này để kết nối các thiết bị cứng bên trong và bên ngoài. Các tệp DRV bao gồm các hướng dẫn và tham số về cách thiết bị và hệ điều hành liên kết với nhau. Các tệp này giúp cài đặt trình điều khiển thiết bị để hoạt động bình thường với Windows. Ngoài ra, các thiết bị được liên kết với bo mạch chủ của PC thông qua bus hoặc cáp yêu cầu tệp DRV.


## Định dạng tệp DRV ##

Tệp DRV thường được đóng gói dưới dạng thư viện động (tệp [DDL](/vi/system/dll/) hoặc tệp [EXE](/vi/executable/exe/). Các tệp này có thể được hỗ trợ trên tất cả các nền tảng hệ thống, chẳng hạn như điện thoại thông minh và không có gì đảm bảo rằng mỗi nền tảng sẽ hỗ trợ đúng các tệp này. Tuy nhiên, một số thiết bị phổ biến nhất sử dụng phần mở rộng tệp .drv là:

* Card âm thanh
* Card đồ họa
* Máy in
* Thiêt bị lưu trư
* Bộ điều hợp mạng
* Phụ kiện phần cứng máy tính

Không nên mở các tệp DRV được gửi qua email vì định dạng tệp này chứa vi-rút và các chương trình độc hại khác. Đảm bảo thực hiện quét toàn diện trước khi mở bất kỳ tệp DRV không xác định nào.


## VNDCCH Ví dụ ##

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

