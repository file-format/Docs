{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp P7S - Thư điện tử được ký điện tử",
  "description":"Tìm hiểu về định dạng tệp P7S và các API có thể tạo và mở tệp P7S.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Tệp P7S là gì?

Tệp P7S là chữ ký điện tử được nhận bằng email được ký điện tử. Sự hiện diện của tệp này dưới dạng tệp đính kèm với email xác minh rằng email được gửi từ một nguồn xác thực. Điều này đảm bảo rằng người gửi đã cài đặt chứng chỉ Ký email trên máy tính của họ. Khi một email đã ký như vậy được gửi từ máy tính của người dùng, tệp P7S được đính kèm với nó có chứa tên của người gửi. Ứng dụng email hỗ trợ email đã ký có thể xem thông tin của người gửi.

## Định dạng tệp P7S - Thông tin khác

Các tệp S/MIME (Tiện ích mở rộng thư Internet an toàn/đa mục đích) P7S chứa thông tin ở định dạng văn bản thuần túy mà con người có thể đọc được. Các ứng dụng email như Microsoft Outlook, Apple Mail và Mozilla Thunderbird hỗ trợ đọc thông tin được ký điện tử từ email S/MIME. Việc ký email xác minh danh tính của người gửi và cho người nhận biết tin nhắn là xác thực. Khi email được tải xuống từ ứng dụng email (dưới dạng [EML](/vi/email/eml/) hoặc [MSG](/vi/email/msg/)), các tệp P7S này được tìm thấy đính kèm với các email này.

Tệp P7S chứa thông tin sau:

* Nguồn gốc của email
* Ngày và thời gian khi nó được gửi,
* Cho dù nó đã được sửa đổi trong quá trình truyền tải

Thông tin này được nhúng bằng công nghệ Tiêu chuẩn mã hóa khóa công khai số 7 (PKCS7) để đính kèm kỹ thuật số chữ ký được mã hóa vào email.

## Người giới thiệu ##

* [Công cụ Microsoft Sign](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

