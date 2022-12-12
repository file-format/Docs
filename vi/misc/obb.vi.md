{
  "date" : "2022-02-16",
  "keywords" :[ "tệp obb", "định dạng tệp obb", "tệp obb là gì", "tệp", "ví dụ obb", "phần mở rộng tệp obb","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp OBB - Tệp đốm nhị phân mờ trong Android",
  "description":"Tìm hiểu về định dạng tệp OBB và API có thể tạo và mở tệp OBB.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Tệp OBB là gì?

Tệp OBB là tệp mở rộng chứa dữ liệu bổ sung ngoài tệp [APK](/vi/compression/apk/) của Android. Cửa hàng Google Play không cho phép có tệp APK Android có kích thước lớn hơn 100 MB. Tuy nhiên, một số ứng dụng có thể yêu cầu đồ họa độ nét cao, tệp phương tiện hoặc nội dung lớn khác được lưu trữ ngoài tệp APK. Đó là nơi các loại tệp OBB xuất hiện. Google Play cho phép đính kèm các tệp mở rộng này dưới dạng phần bổ sung cho tệp APK.

## Định dạng tệp OBB

Tệp OBB được lưu dưới dạng tệp nhị phân cùng với tệp APK. Khi một APK đi kèm với các tệp OBB, Google Play sẽ lưu trữ các tệp mở rộng trên máy chủ của Google Play và nhà phát triển không phải trả thêm phí. Các tệp bổ sung này được lưu trữ trong bộ nhớ dùng chung của thiết bị trên thẻ SD hoặc phân vùng có thể gắn USB khi ứng dụng được tải xuống để cài đặt.

Các tệp OBB được tải xuống và cài đặt khi tải xuống. Nhưng trong một số trường hợp, chúng được tải xuống để cài đặt khi ứng dụng được chạy lần đầu tiên.

### Kích thước tệp tối đa của OBB

Cửa hàng Google Play cho phép bạn tải lên các tệp mở rộng OBB có kích thước lên tới 2 GB. Bạn nên tải lên các tệp có kích thước lớn dưới dạng tệp nén [ZIP](/vi/compression/zip/) để tải lên hiệu quả qua internet.

Các tệp mở rộng này có thể được lưu trữ dưới dạng tệp mở rộng chính **chính** cho các tài nguyên bổ sung mà ứng dụng yêu cầu hoặc tệp mở rộng bản vá tùy chọn dành cho các bản cập nhật nhỏ cho tệp mở rộng chính.

## Người giới thiệu

* [Nhà phát triển Android - Tệp mở rộng](https://developer.android.com/google/play/expansion-files)

