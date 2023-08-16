{
  "date" : "2021-08-30",
  "keywords" :[ "tệp ipa", "định dạng tệp ipa", "tệp ipa là gì", "tệp", "ví dụ về ipa", "phần mở rộng tệp ipa","tiện ích mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp IPA và các API có thể tạo và mở tệp IPA.",
  "title" :"IPA - Tệp gói ứng dụng iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Tệp IPA là gì?
Tệp có phần mở rộng .ipa thuộc về iOS và được gọi là tệp gói ứng dụng. Đây là tệp lưu trữ (được nén bằng cách sử dụng nén [ZIP](/vi/compression/zip/) lưu trữ ứng dụng iOS, nhưng ứng dụng đó chỉ có thể được cài đặt trên thiết bị MacOS chạy iOS hoặc ARM, chẳng hạn như iPad, iPhone hoặc iPod Touch. Về cơ bản, iTunes, Apple Configurator 2 hoặc bất kỳ phần mềm bên thứ ba nào có thể được sử dụng để cài đặt các tệp IPA.

## Định dạng tệp IPA
Các nhà phát triển iOS đang phát triển ứng dụng bằng Apple Xcode đã quen thuộc với các tệp IPA vì họ cần đóng gói các ứng dụng đã phát triển của mình dưới dạng tệp IPA để thử nghiệm các mục đích triển khai cửa hàng ứng dụng. Mặc dù, các tệp IPA được biết là được cài đặt dưới dạng ứng dụng iOS, tuy nhiên, bạn cũng có thể giải nén chúng để xem dữ liệu ứng dụng chứa trong đó. Do tệp IPA chỉ chứa một tệp nhị phân cho kiến trúc ARM của điện thoại di động và không chứa tệp nhị phân cho kiến trúc x86 nên không thể cài đặt nhiều tệp .ipa trên Trình mô phỏng iPhone.
### Cấu trúc của tệp .ipa
Ví dụ sau đây cho thấy cấu trúc của một IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Trên đây là cấu trúc có sẵn để iTunes và App Store nhận diện. Theo cấu trúc này:
- Thư mục Payload chứa tất cả dữ liệu ứng dụng.
- Tệp Tác phẩm nghệ thuật iTunes là hình ảnh PNG có kích thước 512×512 pixel, chứa biểu tượng của ứng dụng để hiển thị trong iTunes và ứng dụng App Store trên iPad.
- iTunesMetadata.plist chứa nhiều thông tin khác nhau, từ tên và ID của nhà phát triển, thông tin bản quyền, mã định danh gói, tên của ứng dụng, thể loại, ngày phát hành, ngày mua, v.v.
- Thư mục META-INF chỉ chứa siêu dữ liệu về chương trình nào đã được sử dụng để tạo IPA.


## Người giới thiệu

* [.ipa - theo Wikipedia](https://en.wikipedia.org/wiki/.ipa)


