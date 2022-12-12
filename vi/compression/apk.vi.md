{
  "date" : "2019-10-11",
  "keywords" :[ "tệp apk", "định dạng tệp apk", "tệp apk là gì", "tệp", "ví dụ apk", "phần mở rộng tệp apk","tiện ích mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Tệp APK là gì?",
  "description":"Tìm hiểu để biết tệp APK là gì và các API có thể tạo và mở tệp APK.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Tệp APK là gì?

Tệp có phần mở rộng .apk là tệp ứng dụng Google Android được sử dụng để cài đặt ứng dụng (ứng dụng) trên thiết bị Android. Nó được tạo dưới dạng tệp thực thi bằng IDE chính thức của Google Android Studio và được tải lên cửa hàng Google Play để người dùng cuối tải xuống và cài đặt. Các tệp APK có thể được tạo và cung cấp để cài đặt thủ công cũng như trước khi xuất bản lên cửa hàng Google Play. Điều này giúp kiểm tra chức năng và hành vi của tệp gói APK đã tạo. Do đó, người ta cần đảm bảo rằng tệp APK đến từ một nguồn đáng tin cậy và không chứa bất kỳ phần mềm độc hại nào.

## Định dạng tệp APK

Các tệp APK được đóng gói dưới dạng nén ở định dạng tệp [ZIP](/vi/compression/zip/) có thể mở bằng bất kỳ phần mềm mở tệp ZIP nào. Phần mở rộng .apk của tệp như vậy có thể được đổi tên thành .zip và mở tệp trong bất kỳ ứng dụng ZIP nào hoặc trích xuất nội dung của tệp.

## Nội dung gói APK

Một tệp APK duy nhất chứa tất cả các tệp cần thiết để cài đặt và thực thi. Tệp APK, khi được giải nén bằng ứng dụng ZIP, chứa các tệp và thư mục sau.

* `META-INF/`: Thư mục chứa tệp kê khai, chữ ký và danh sách tài nguyên trong kho lưu trữ
* `lib/`: Thư mục chứa mã được biên dịch liên quan đến các nền tảng cụ thể như armeabi-v7a, x86, arm64-v8a, v.v.
* `res/`: Thư mục chứa tài nguyên không được biên dịch như hình ảnh
* `assets/`: Thư mục chứa các tài sản của ứng dụng, có thể được truy xuất bởi AssetManager.
* `androidManifest.xml`: Chứa tên, thông tin phiên bản và nội dung của tệp APK
* `classes.dex`: Đây là các lớp Java được biên dịch có thể chạy trên máy ảo Dalvik và bởi Android Runtime
* `resources.arsc`: Tệp tài nguyên được biên dịch như chuỗi

## Làm cách nào để cài đặt tệp APK trên Thiết bị Android?

Để cài đặt tệp APK trên thiết bị Android của bạn, có thể sử dụng các bước sau.

1. Tải xuống APK bằng trình duyệt web
2. Nhấn vào nó – sau đó bạn sẽ có thể thấy nó đang tải xuống trên thanh trên cùng của thiết bị
3. Sau khi tải xuống, hãy mở Tải xuống, nhấn vào tệp APK và nhấn Có khi được nhắc.

Thực hiện theo các bước này sẽ bắt đầu cài đặt ứng dụng trên thiết bị của bạn.

## Người giới thiệu

* [Định dạng tệp APK](https://en.wikipedia.org/wiki/Android_application_package)

