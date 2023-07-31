{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp SY_ - Tệp SYS được nén",
  "description":"Tìm hiểu về định dạng tệp SY_ và các API có thể tạo và mở tệp SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Tệp SY_ là gì?

Tệp SY_ là tệp .sys nén được trình cài đặt phần mềm sử dụng để giảm kích thước tệp cài đặt được đóng gói bên trong trình cài đặt. Điều này làm giảm kích thước tổng thể của trình cài đặt. Các tệp SY_ có thể được mở rộng bằng tiện ích dòng lệnh Microsoft Expand để mở rộng một hoặc nhiều tệp nén.

## Định dạng tệp SY_ - Thông tin khác

Các tệp SY_ được lưu vào đĩa dưới dạng tệp nhị phân được nén. Tuy nhiên, định dạng tệp nội bộ của chúng không có sẵn công khai. Tiện ích dòng lệnh Microsoft Expand có thể mở rộng các tệp SY_ bằng một trong các dòng lệnh sau.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Khi được mở rộng, các tệp SY_ được chuyển đổi thành tệp [SYS](https://docs.fileformat.com/system/sys/).

Tệp SY_ tương tự như tệp EX_ và DL_.

## Người giới thiệu

* [StuffIt - Theo Wikipedia](https://vi.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

