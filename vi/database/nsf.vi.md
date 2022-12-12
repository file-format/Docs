{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp NSF và API có thể tạo và mở tệp NSF.",
  "title" :"Định dạng tệp NSF - Định dạng cơ sở dữ liệu Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Tệp NSF là gì?

Tệp có phần mở rộng .nsf (Thiết bị lưu trữ ghi chú) là định dạng tệp cơ sở dữ liệu được [phần mềm Ghi chú của IBM](https://en.wikipedia.org/wiki/HCL_Domino) sử dụng, trước đây được gọi là Lotus Notes. Nó xác định lược đồ để lưu trữ các loại đối tượng khác nhau như email, cuộc hẹn, tài liệu, biểu mẫu và dạng xem. Tất cả thông tin này được chứa trong một tệp NSF duy nhất để cộng tác kinh doanh tương tự như tệp PST/OST. Một số ứng dụng có thể mở tệp NSF bao gồm IBM Lotus Notes và IBM Domino.

## Thông số kỹ thuật định dạng tệp NSF

Các tệp NSF có bản chất là nhị phân và thông số kỹ thuật của chúng có sẵn bởi Joachim Metz trên [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database% 20file%20format.asciidoc). Theo các chi tiết này, một tệp NSF bao gồm:

* Tiêu đề tệp
* Tiêu đề cơ sở dữ liệu

Ngoài ra, nó bao gồm:

* Siêu khối
* Khối mô tả thùng
* Ảnh bitmap
* Ghi thùng Vector di dời
* Tóm tắt thùng
* Xô không tóm tắt


### Tiêu đề tệp NSF

Tiêu đề tệp NSF có kích thước 6 byte. Nó bao gồm:

|Độ lệch|Kích thước|Giá trị|Mô tả|
---|---|---|---|
0|2|0x1a 0x00|Chữ ký|
2|4| |Kích thước tiêu đề cơ sở dữ liệu|

### Tiêu đề cơ sở dữ liệu

Tiêu đề Cơ sở dữ liệu NSD chứa các giá trị được xác nhận sau đây.

* Thông tin cơ sở dữ liệu
* Định danh cơ sở dữ liệu (DBID)
* Thông tin sao chép
* Cờ đệm thông tin cơ sở dữ liệu
* Tiêu đề
* Thể loại
* Lớp
* Lớp thiết kế (tên mẫu)
* Số nhận dạng lưu ý đặc biệt
* Đệm
* Cơ sở dữ liệu thông tin 2
* Cơ sở dữ liệu thông tin 3
* Cơ sở dữ liệu thông tin 4
* Cơ sở dữ liệu thông tin 5
* Đệm
* Mã định danh phiên bản cơ sở dữ liệu (DBIID)
* Lịch sử sao chép

## Người giới thiệu

* [Định dạng NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

