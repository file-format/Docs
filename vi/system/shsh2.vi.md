{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp SHSH2 - Định dạng tệp SHSH Blob của iOS",
  "description":"Tìm hiểu về tệp SHSH2 là gì.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Tệp SHSH2 là gì?

Tệp SHSH2, còn được gọi là SHSH blob hoặc ECID SHSH, là chữ ký số được Apple sử dụng để xác thực và xác minh các bản cập nhật chương trình cơ sở cho các thiết bị iOS như iPhone, iPad và iPod. Nó chứa mã nhận dạng duy nhất cho thiết bị được gọi là ECID (ID chip độc quyền). Nó cũng chứa thông tin về phiên bản phần sụn được cài đặt trên thiết bị.

## Định dạng tệp SHSH2 - Thông tin thêm

Các tệp SHSH2 được lưu vào đĩa ở định dạng tệp nhị phân và chi tiết cấu trúc tệp bên trong của định dạng tệp này không được cung cấp công khai.

Khi phiên bản iOS mới được cài đặt trên thiết bị Apple như iPhone, iPad hoặc Mac, tệp SHSH2 sẽ được tạo. Tệp SHSH2 này được gửi đến máy chủ Apple để đọc và xác minh tệp chữ ký số này. Dựa trên thông tin này, máy chủ cho phép hoặc ngăn chặn việc cài đặt.

Điều tương tự cũng xảy ra khi yêu cầu cập nhật. Khi người dùng yêu cầu cập nhật hoặc khôi phục thiết bị của họ thông qua iTunes hoặc phần mềm khác, máy chủ của Apple sẽ kiểm tra xem tệp SHSH2 có khớp với ECID và phiên bản chương trình cơ sở của thiết bị hay không trước khi cho phép tiến hành cập nhật.

## Người giới thiệu

* [SHSH Blob - Bởi Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)

