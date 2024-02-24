{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp VPK của Unreal Static Meshes và các API có thể tạo và mở tệp VPK.",
  "title" : "Tệp VPK - Tệp lưới tĩnh không thực",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-vi",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Một tập tin VPK là gì?

Tệp .vpk là định dạng tệp được **Source Engine**, một công cụ trò chơi được phát triển bởi Valve Corporation, sử dụng. Các tệp VPK được sử dụng để đóng gói nội dung trò chơi, chẳng hạn như mô hình, kết cấu và âm thanh, đồng thời thường được sử dụng trong các trò chơi như Team Fortress 2, Left 4 Dead và Counter-Strike: Global Offensive. Các tệp có thể được mở và giải nén bằng nhiều công cụ khác nhau, chẳng hạn như GCFScape và VPK Tool.

## Định dạng tệp VPK - Thông tin thêm

Các tệp VPK được lưu vào đĩa dưới dạng tệp nhị phân. Một tệp vpk có thể là một phần của gói VPK hoặc có thể hoạt động như một tệp VPK thô độc lập. Thông tin có thể được lưu trữ bên trong tệp VPK bao gồm bản đồ, tài liệu, nội dung trò chơi và cảnh vũ đạo.

### Làm cách nào để tạo tệp VPK?

Có một số cách để tạo tệp .vpk, tùy thuộc vào các công cụ có sẵn.

1. `Sử dụng công cụ VPK:` Đây là một công cụ dòng lệnh có thể được sử dụng để tạo và giải nén các tệp VPK. Một tệp VPK có thể được tạo bằng lệnh sau:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Thao tác này sẽ tạo tệp VPK từ thư mục đã chỉ định và lưu nó dưới dạng tệp đầu ra được chỉ định.

1. `Sử dụng Hammer Editor:` Hammer Editor là một công cụ đi kèm với Source SDK có thể được sử dụng để tạo và chỉnh sửa cấp độ cho các trò chơi sử dụng Source engine. Nó cũng bao gồm khả năng tạo tệp VPK, bằng cách nhấp chuột phải vào thư mục trong tab Hệ thống tệp và chọn Tạo VPK

1. `Sử dụng VPK Creator của Valve:` Đây là một công cụ do Valve phát triển, dùng để đóng gói và phân phối nội dung trò chơi. Công cụ này có thể được sử dụng để tạo tệp VPK và đây cũng là công cụ chính thức để tạo tệp VPK.

## Người giới thiệu

 * [Phần mềm Valve](https://www.valvesoftware.com/en/)
 * [Tài nguyên dành cho nhà phát triển VPK](https://developer.valvesoftware.com/wiki/GCF)

