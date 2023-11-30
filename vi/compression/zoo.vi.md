{
"date" :  "2023-11-09",
   "keywords":[
"vườn bách thú",
"tệp sở thú",
"tệp nén sở thú",
"cách mở tệp sở thú",
"tài liệu",
"phần mở rộng tập tin sở thú",
"sự mở rộng",
"tài liệu"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"Tệp ZOO - Tệp .zoo là gì và làm cách nào để mở tệp?",
   "description":"Tìm hiểu về định dạng tệp nén ZOO và các API có thể tạo và mở tệp ZOO.",
"linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
         "parent":"compression"
}
},
"lastmod":"2023-11-09"
}

## Tập tin ZOO là gì?

Tệp `.zoo` là định dạng lưu trữ được sử dụng để nén và lưu trữ các tệp và thư mục; tương tự như các định dạng lưu trữ khác như `.zip`, `.tar`, và `.rar`. Định dạng `.zoo` phổ biến trong thời kỳ đầu của máy tính nhưng đã trở nên ít phổ biến hơn trong những năm gần đây. Ban đầu nó được phát triển bởi **Rahul Dhesi** và được sử dụng chủ yếu trên hệ thống Unix và DOS.

Tệp `.zoo` thường chứa một hoặc nhiều tệp và thư mục đã được nén và lưu trữ thành một tệp duy nhất. Bạn có thể tạo và trích xuất các tệp `.zoo` bằng nhiều công cụ phần mềm hỗ trợ định dạng này.

Kho lưu trữ ZOO có một tính năng độc đáo cho phép chúng lưu trữ nhiều phiên bản của cùng một tệp với điều kiện mỗi phiên bản được sửa đổi vào ngày khác nhau. Điều này có nghĩa là người dùng ZOO có thể lưu và truy cập các lần lặp lại trước đó của tệp trực tiếp từ kho lưu trữ ZOO. Tính năng này cho phép người dùng hoàn nguyên về phiên bản cũ hơn của tệp hoặc so sánh phiên bản cũ hơn với phiên bản mới hơn, cung cấp cách thuận tiện để quản lý các sửa đổi và thay đổi tệp theo thời gian.

## Các thao tác chung của file ZOO

Dưới đây là một số thao tác phổ biến được liên kết với tệp `.zoo`:

1. **Tạo tệp `.zoo`:** Bạn có thể sử dụng tiện ích dòng lệnh như "zoo" để tạo tệp `.zoo`. Ví dụ: lệnh sau sẽ tạo kho lưu trữ `.zoo` từ thư mục:
    








`zoo a -c archive.zoo thư mục/`
    








Trong lệnh này, "a" là viết tắt của "add", "-c" chỉ định nén và "archive.zoo" là tên của kho lưu trữ đầu ra.
    








2. **Trích xuất tệp từ tệp `.zoo`:** Để trích xuất nội dung của kho lưu trữ `.zoo`, bạn có thể sử dụng lệnh như sau:
    








`sở thú e archive.zoo`
    








Lệnh này sẽ trích xuất các tập tin từ tập tin `archive.zoo`.
    








3. **Liệt kê nội dung của tệp `.zoo`:** Bạn có thể liệt kê nội dung của kho lưu trữ `.zoo` mà không cần giải nén chúng bằng tùy chọn "l":
    








    








`sở thú l archive.zoo`

## Làm cách nào để mở tệp ZOO?

Các chương trình mở tệp ZOO bao gồm

- **zoo** (Miễn phí) cho (Windows, Linux)

## Người giới thiệu
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
