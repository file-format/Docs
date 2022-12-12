{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp VPK - Định dạng tệp gói ứng dụng PlayStation Vita",
  "description":"Tìm hiểu về định dạng tệp VPK và các API có thể tạo và mở tệp VPK.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Tệp VPK là gì?

Tệp có phần mở rộng .vpk là tệp gói lưu trữ nén được sử dụng để cài đặt ứng dụng của bên thứ ba trên bảng điều khiển trò chơi Sony PlayStation Vita. Các tệp này chỉ có thể được cài đặt trên PlayStation Vita đã bẻ khóa bởi HENkaku đã cho phép PS Vita và PSTV sử dụng nội dung do người dùng tạo tùy chỉnh. Tệp lưu trữ VPK chứa tất cả nội dung tạo nên trò chơi, bao gồm cả hình ảnh như tệp [PNG](/vi/image/png/), cài đặt tệp như [.bin](/vi/disc-and-media/bin/) và bất kỳ cấu hình nào ở định dạng tệp [XML](/vi/web/xml/).

## Định dạng tệp VPK

Các tệp VPK được lưu vào đĩa dưới dạng lưu trữ nén [ZIP](/vi/compression/zip/) tiêu chuẩn. Các tệp này có thể chứa nhiều thư mục và các tệp liên quan khác dành cho ứng dụng của bên thứ ba được cài đặt trên Bảng điều khiển trò chơi Vita. Để xem nội dung của tệp gói VPK, hãy đổi tên phần mở rộng của nó từ .vpu thành .zip và giải nén nội dung bằng các tiện ích giải nén tiêu chuẩn như WinZip hoặc WinRAR.

Valvesoftware có thông tin chi tiết về [định dạng tệp VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) mà nhà phát triển có thể tham khảo.

## Làm cách nào để cài đặt tệp VPK?

Các tệp VPK có thể được cài đặt từ tiện ích dòng lệnh VPK.exe. Trên HĐH Windows, các tệp có thể được thả vào tệp vpk.exe, tệp này trả về \*.vpk chứa tất cả các tệp được đóng gói. Ngoài ra, công cụ dòng lệnh có thể được sử dụng như sau.

### Tạo VPK và thêm tệp

```
vpk <dirname>
```

### Giải nén tập tin VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## Trình xem VPK

* [Trình xem VRF VPK](https://github.com/SteamDatabase/ValveResourceFormat)

## Người giới thiệu

* [Định dạng tệp VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [Tệp VPK](https://developer.valvesoftware.com/wiki/VPK)

