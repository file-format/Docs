{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp SHSH - Định dạng tệp SHSH Blob cho iPhone/iPod Touch",
  "description":"Tìm hiểu về tệp SHSH là gì.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Tập tin SHSH là gì?

Tệp SHSH, còn được gọi là Signature Hash, là chữ ký số được Apple sử dụng để xác thực và xác minh các bản cập nhật chương trình cơ sở cho các thiết bị iOS như iPhone, iPad và iPod.

## Sự khác biệt giữa định dạng tệp SHSH và SHSH2

Giống như tệp SHSH2, tệp SHSH chứa mã nhận dạng duy nhất cho thiết bị được gọi là "ECID" (ID chip độc quyền), cũng như thông tin về phiên bản chương trình cơ sở được cài đặt trên thiết bị. Tuy nhiên, các tệp SHSH đã được sử dụng trong các phiên bản iOS cũ hơn (trước iOS 10) và kể từ đó đã được thay thế bằng các tệp SHSH2.

## Định dạng tệp SHSH - Thông tin thêm

Các tệp SHSH được lưu vào đĩa ở định dạng tệp nhị phân. Chi tiết cấu trúc tệp nội bộ của định dạng tệp này không được cung cấp công khai.

Các tệp SHSH rất quan trọng đối với những người dùng muốn hạ cấp chương trình cơ sở của thiết bị của họ xuống phiên bản trước đó không còn được Apple ký nữa. Bằng cách lưu các tệp SHSH cho một phiên bản chương trình cơ sở cụ thể khi nó vẫn đang được Apple ký, sau này người dùng có thể sử dụng chúng để bỏ qua xác minh chữ ký của Apple và cài đặt phiên bản chương trình cơ sở đó trên thiết bị của họ. Quá trình này còn được gọi là `bẻ khóa`.

## Người giới thiệu

* [SHSH Blob - Bởi Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)

