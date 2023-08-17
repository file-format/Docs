{
  "date" : "2021-01-21",
  "keywords" :[ "tệp otp", "định dạng tệp otp", "tệp otp là gì", "tệp", "ví dụ otp", "phần mở rộng tệp otp","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - Mẫu bản trình bày OpenDocument",
  "description":"Tìm hiểu về định dạng tệp OTP và API có thể tạo và mở tệp OTP.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## Tệp OTP là gì?

Các tệp có phần mở rộng .otp đại diện cho các tệp mẫu bản trình bày được tạo bởi các ứng dụng ở định dạng chuẩn OASIS OpenDocument. Nội dung của một tệp như vậy bao gồm thông tin trình bày dưới dạng trang chiếu với văn bản, hình ảnh, hình dạng, nội dung đa phương tiện, hiệu ứng chuyển tiếp và các yếu tố trang chiếu khác. Các tệp mẫu này được sử dụng để tạo bản trình bày mới một cách nhanh chóng dựa trên thông tin kiểu dáng được lưu trữ trong chính mẫu đó. Các tệp OTP có thể được tạo và lưu bằng một số ứng dụng khác nhau, chẳng hạn như Ấn tượng đi kèm với bộ OpenOffice và Microsoft PowerPoint. Định dạng tệp OTP tương tự như các tệp mẫu Microsoft PowerPoint [.pot](/vi/presentation/pot/) và [.potx](/vi/presentation/potx/).

## Định dạng tệp OTP

Định dạng tệp OTP dựa trên tiêu chuẩn OpenDocument hỗ trợ biểu diễn tài liệu dưới dạng một tài liệu XML duy nhất cũng như tập hợp một số tài liệu phụ trong một gói nén duy nhất ở định dạng [ZIP](/vi/compression/zip/). Nội dung của tệp được phân phối trong nhiều tệp xml được đóng gói cùng nhau. Nhiều tệp [XML](/vi/web/xml/) này chứa thông tin về kiểu, nội dung, thông tin meta và cài đặt của tài liệu như được đề cập bên dưới.

* `content.xml` – Nội dung tài liệu và kiểu tự động được sử dụng trong nội dung.
* `styles.xml` – Các kiểu được sử dụng trong nội dung tài liệu và các kiểu tự động được sử dụng trong chính các kiểu đó.
* `meta.xml` – Thông tin meta tài liệu, chẳng hạn như tác giả hoặc thời gian của hành động lưu cuối cùng.
* `settings.xml` – Cài đặt dành riêng cho ứng dụng, chẳng hạn như kích thước cửa sổ hoặc thông tin máy in.

## Người giới thiệu

* [OpenDocument - Bởi Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

