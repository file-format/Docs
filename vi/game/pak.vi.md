{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "định dạng tệp", "tệp pak là gì", "tệp", "ví dụ pak", "Tệp gói trò chơi điện tử","phần mở rộng"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về tệp .pak và các API có thể tạo và mở tệp PAK.",
  "title" :"Định dạng tệp PAK- Tệp gói trò chơi điện tử",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Tệp PAK là gì?

Tệp PAK là tệp gói được tạo bởi các trò chơi video khác nhau để lưu trữ dữ liệu trò chơi. Về cơ bản, đó là một định dạng tệp trò chơi. Điều này có thể bao gồm nhiều yếu tố trò chơi như đồ họa, kết cấu, âm thanh, đối tượng, cùng với dữ liệu trò chơi khác. Kho lưu trữ hầu hết được lưu dưới dạng tệp .zip và có thể được giải nén bằng phần mềm giải nén phổ biến như WinZip và WinRAR. Ví dụ về trò chơi điện tử sử dụng tệp PAK bao gồm Quake, Hexen, Crysis và Half-Life.

## Định dạng tệp PAK - Thông tin khác

Trong hầu hết các trường hợp, tệp PAK được lưu ở [định dạng tệp ZIP](/vi/compression/zip/). Nhưng các ứng dụng khác nhau có thể sử dụng định dạng tệp khác nhau để lưu trữ các tệp này.


## Làm cách nào để mở tệp PAK?

Bạn có thể mở tệp PAK bằng các ứng dụng như [PakExplorer](https://www.quaketerminus.com/tools.shtml) và [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- -----------------------**

## Định dạng tệp PAK - Tệp đối tượng Simutrans

Tệp có phần mở rộng .pak là định dạng tệp trò chơi mô phỏng giao thông [Simutrans](https://www.simutrans.com/en/). Nó chứa các đối tượng được sử dụng trong mô phỏng, chẳng hạn như nội dung dữ liệu và đồ họa do người dùng tạo. Nó có thể có một số đối tượng khác nhau, chẳng hạn như phương tiện trò chơi, tòa nhà, địa hình, v.v. Các tệp PAK được tạo bằng MakeObject, một tiện ích biên dịch các tệp .dat và ảnh .png để tạo các đối tượng mô phỏng này. Simutrans cho phép người chơi điều hành một hệ thống giao thông thành công bằng cách xây dựng và quản lý hệ thống vận chuyển hành khách, thư tín và hàng hóa bằng đường bộ

## Làm cách nào để tạo tệp PAK?

Simutrans đã liệt kê các ví dụ mẫu để tạo tệp PAK trên HĐH Windows và Linux.

### Hệ điều hành Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/HĐH

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Người giới thiệu

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)