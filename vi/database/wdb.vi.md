{
  "date" : "2021-08-24",
  "keywords" :[ "tệp wdb", "định dạng tệp wdb", "tệp wdb là gì", "tệp", "ví dụ wdb", "phần mở rộng tệp wdb","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp WDB và API có thể tạo và mở tệp WDB.",
  "title" :"WDB - Tệp theo dõi máy chủ SQL",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Tệp WDB là gì?
Một tệp có phần mở rộng .wdb thực sự là một tệp cơ sở dữ liệu được tạo bởi Microsoft Works, được sử dụng để thực hiện các chức năng giống như một hệ thống quản lý cơ sở dữ liệu. Tệp WDB tương tự như tệp Cơ sở dữ liệu Access ([MDB](/vi/database/mdb/)), nhưng kém hiệu quả hơn và có nhiều hạn chế hơn. Không thể mở tệp WDB bằng cách sử dụng Microsoft Access. Tuy nhiên, bạn có thể mở tệp WDB trong Microsoft Works và sau đó xuất nó sang tệp MDB, để mở tệp WDB trong MS Access.

## Định dạng tệp WDB
Cơ sở dữ liệu Microsoft Works là định dạng cơ sở dữ liệu gốc của bộ ứng dụng văn phòng Microsoft Works. Do tính chất độc quyền của định dạng và một số hạn chế. Không thể mở các tệp WDB trong bất kỳ phần mềm nào khác ngoài Microsoft Works. Ở định dạng tệp, có thể tìm thấy tiêu đề định kỳ, 10 byte trước mỗi chuỗi văn bản ASCII biểu thị giá trị của các trường được kết thúc bằng giá trị NULL. Tiêu đề thường bắt đầu bằng byte **\x0f** và NULL, theo sau là 4 byte dữ liệu xen kẽ với NULL.

### Cấu trúc tệp

Cấu trúc của tệp WDB được đưa ra dưới đây:
- **Tiêu đề đầu tiên**: từ đầu tệp, kết thúc bằng \x25\x00\xf2 và 244 byte NULL
- **Tiêu đề thứ 2**: bắt đầu bằng \xffT - tức là \xff\x54 và mở rộng cho 4096 byte, chứa tên cột/trường và những thứ khác, và dường như bắt đầu ở vị trí byte 6144.
- **Trường**: giá trị có tiêu đề 10 byte, có định dạng như sau: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , phần 2} {db 4} \x00. byte dữ liệu 2 là số trường, byte dữ liệu 3 là số bản ghi (thêm byte dữ liệu 3, phần 2 khi vượt quá 256 bản ghi).


## Người giới thiệu ##

* [Người dùng:JesseW/định dạng wdb](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

