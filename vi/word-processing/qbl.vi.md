{
  "date" : "2021-07-28",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QBL - Tệp giấy phép QuickBooks",
  "description":"Tìm hiểu về định dạng tệp QBL và các API có thể tạo và mở tệp QBL.",
  "linktitle" : "QBL",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-28"
}

## Tệp QBL là gì?

Tệp có phần mở rộng .qbl là tệp giấy phép QuickBooks chứa thông tin cấp phép cho bản sao đã mua của người dùng. Nó thường được lưu trữ trong hệ thống cục bộ với tên `license.qbl` sau khi QuickBooks được cài đặt và người dùng nhập thông tin cấp phép vào phần mềm khi phần mềm được chạy lần đầu tiên. QBL là định dạng tệp trước đó được sử dụng để lưu trữ thông tin cấp phép QuickBooks. Tệp này hiện đã được thay thế bằng tệp `qbregisteration.dat` của QuickBooks và được điền thông tin từ email xác nhận của người dùng, DVD đã mua hoặc thông qua các phương tiện mua khác. Các tệp QBL có thể được mở trong bất kỳ trình soạn thảo văn bản nào, chẳng hạn như Windows Notepad, Apple TextEdit, Notepad ++, trình soạn thảo Github Atom, v.v.

## Định dạng tệp QBL - Thông tin khác

Các tệp QBL được tạo và lưu trữ dưới dạng tệp văn bản thuần túy. Thông tin trong các tệp này con người có thể đọc được và có thể được chỉnh sửa/cập nhật khi các tệp này được mở trong trình soạn thảo văn bản. Sau đó, thông tin đăng ký người dùng và giấy phép có thể được sao chép trong tệp này để bắt đầu với phần mềm QuickBooks. Các tệp QBL thường được lưu trữ trong thư mục Program Files\Intuit\QuickBooks\INET trên Hệ điều hành Windows.

Tệp QBL chứa hai loại thông tin.

* `Thông tin Phiên bản QuickBooks:` Được gọi là phiên bản QuickBooks đã cài đặt và có định dạng như xx.x
* `Khóa cấp phép:` Văn bản ở định dạng 000-000 0000-0000-0000-000 000073adbf3f trong đó 000-000 0000-0000-0000-000 được thay thế bằng Khóa qbregisteration của người dùng

## Người giới thiệu

* [QuickBooks của Intuit](https://quickbooks.intuit.com/)
* [QuickBooks - Tạo tệp qbregistration.dat](https://quickbooks.intuit.com/learn-support/en-us/help-article/license-information/create-create-qbregistration-dat-file/L7S5BwSst_US_en_US)

