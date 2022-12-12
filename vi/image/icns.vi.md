{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "phần mở rộng", "tệp", "định dạng", "hình ảnh", "Hình ảnh biểu tượng Apple", "macOS", "Apple", "Biểu tượng" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Hình ảnh biểu tượng Apple",
  "description":"Tìm hiểu về định dạng tệp ICNS và API có thể tạo và mở tệp ICNS.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Tệp ICNS là gì? ##

Một định dạng biểu tượng được sử dụng bởi các chương trình macOS được gọi là tệp ICNS. Nó cho phép các dải alpha 1 bit và 8 bit và lưu một hoặc nhiều ảnh, thường được tạo từ tài liệu [PNG](/vi/image/png). Biểu tượng chương trình trong giao diện và trình duyệt macOS được hiển thị bằng các tệp ICNS.

Dựa trên vị trí, cùng một biểu tượng kiểu có thể có nhiều cài đặt. Định dạng ICNS đã trải qua nhiều lần thay đổi và đã phát triển đến mức giờ đây nó có thể được sử dụng làm nền tảng cho các định dạng tương thích khác nhau. Dưới đây là một số điểm quan trọng khác mà bạn cần biết:

* Tài nguyên IconFamily, Biểu tượng Macintosh, Biểu tượng Macintosh OS X, Biểu tượng Mac OS, Biểu tượng Apple, Tài nguyên biểu tượng Mac OS X và Tài nguyên biểu tượng Mac OS là một số tên khác.
* Đối với thông tin biểu tượng, một nguồn trong nhánh tài nguyên được sử dụng.
* Trong hầu hết các trường hợp, một tệp chứa nhiều hình ảnh. 1612 pixel vuông và 1024, 512, 256, 128, 48, 32 và 16 pixel vuông là các kích thước hình ảnh được hỗ trợ.


## Định dạng tệp ICNS ##

Định dạng dữ liệu ICNS là một viên nang cho một hoặc nhiều hình ảnh, hỗ trợ các dải 1 bit và nhiều trạng thái hình ảnh.
Hệ điều hành có thể thay đổi kích thước hình ảnh biểu tượng để phù hợp với kích thước hiển thị được yêu cầu. Ảnh biểu tượng lớn hơn thường được lưu dưới dạng tệp [JPEG](/vi/image/jpeg/) 2000 hoặc [PNG](/vi/image/png). Có thể có một loại tệp ICNS nén và không nén.

Dữ liệu tiêu đề và biểu tượng nhị phân tạo nên cấu trúc của tệp ICNS. Tiêu đề chứa 8 byte dữ liệu, bốn trong số đó là ký tự ma thuật và bốn trong số đó là độ dài của tệp. Loại và kích thước của mỗi ảnh biểu tượng được lưu trữ trong phần dữ liệu biểu tượng, theo sau là dữ liệu ảnh nhị phân. Kích thước ảnh xác định kích thước của phần nhị phân.

## Đặc điểm kỹ thuật ##

### Tiêu đề ###

|Bù đắp|Kích thước|Mục tiêu
---|---|---|
|0|4|Ma thuật theo nghĩa đen, phải là "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Độ dài của tệp, tính bằng byte, trước tiên là msb


### Dữ liệu biểu tượng ###

|Bù đắp|Kích thước|Mục tiêu
---|---|---|
|0|4|Loại biểu tượng
|4|4|Độ dài của dữ liệu, tính bằng byte (bao gồm loại và độ dài), trước tiên là msb
|8|Biến|Dữ liệu biểu tượng

### Nén ###

Dữ liệu pixel được nén ở một mức độ nào đó. Các pixel 32 bit ("is32", "il32", "ih32", "it32") và ARGB ("ic04", "ic05") thường được nén (trên mỗi kênh) theo cách tương tự như PackBits.

|Giá trị đầu mối|Bytes đuôi|Kết quả (không nén)
---|---|---|
|0 - 127|1 - 128|1 - 128 byte
|128 - 255|1 Byte|3 - 130 Bản sao

## Tài liệu tham khảo ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

