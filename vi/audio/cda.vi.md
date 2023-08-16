{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "tệp", "phần mở rộng", "định dạng", "tệp cda là gì", "nhạc", "định dạng tệp cda", "đặc tả định dạng tệp cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp CDA và API có thể tạo, chuyển đổi và mở tệp CDA.",
  "title" :"Tệp tắt bản nhạc CDA - CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Tệp CDA là gì?

Một tệp có phần mở rộng .cda là một tệp sơ khai nhỏ do Microsoft Windows tạo cho mỗi rãnh âm thanh trên đĩa CD âm thanh. Các tệp này chứa thông tin điển hình như thời gian theo dõi và phím tắt Windows cho phép người dùng truy cập vào các bản âm thanh cụ thể. Các tệp CDA không phải là nhạc, nhưng chúng trỏ đến một tệp nhạc tồn tại ở đâu đó trên bộ lưu trữ. Chúng ta có thể nói nó như một lối tắt của tệp âm thanh nằm trên đĩa CD.

## Định dạng tệp CDA

Định dạng tệp CDA được sử dụng để báo cho máy tính biết tệp âm thanh nào sẽ phát trên đĩa CD. Vì vậy, các tệp CDA trở nên vô dụng khi tách khỏi đĩa CD mà chúng đại diện. Các tệp CDA thường được coi là tài nguyên RIFF. Chỉ có một đoạn có tên là "CDDA" và chỉ chứa một khối dữ liệu có tên là "FMT " trong phiên bản hiện tại của tệp .cda. Khối này dài 24 byte. Mã định danh do Windows tạo được sử dụng bởi ổ đĩa CD liên quan đến Windows 95 và Windows 98 và trình phát của nó không thể kết nối với FreeDB hoặc CDDB. Để nó có thể hiển thị tên bài hát và tên nghệ sĩ, bạn phải nhập thông tin này theo cách thủ công vào tệp cdplayer.ini.

### Tổ chức tệp CDA

Bảng sau đây hiển thị thông tin về độ lệch chuẩn:
| bù đắp | chiều dài | nội dung |
---|---|---|
| 0x00 | 4 | 4 ký tự ASCII "RIFF" |
| 0x04 | 4 | kích thước của đoạn sau: luôn là 36 (44 - 8), trên 4 byte (thứ tự Intel) |
| 0x08 | 4 | mã định danh chunk: 4 ký tự ASCII "CDDA" |
| 0x0C | 4 | 3 ký tự ASCII "fmt" theo sau là dấu cách |
| 0x10 | 4 | độ dài của đoạn: luôn là 24, trên 4 byte (thứ tự Intel) |
| 0x14 | 2 | phiên bản của định dạng CD, trên 2 byte (thứ tự Intel). Tháng 5/2006 luôn bằng 1. |
| 0x016 | 2 | số của phạm vi, trên 2 byte (thứ tự Intel). Ca khúc đầu tiên có số 1. |
| 0x18 | 4 | định danh do Windows tính toán cho cdplayer.exe. |
| 0x1c | 4 | khoảng bù, theo số lượng khung hình (thứ tự Intel) |
| 0x20 | 4 | thời lượng của bản nhạc, tổng số khung hình (thứ tự Intel) |
| 0x24 | 1 | vị trí phạm vi: khung |
| 0x25 | 1 | vị trí phạm vi: giây |
| 0x26 | 1 | vị trí phạm vi: phút |
| 0x27 | 1 | một byte rỗng (giá trị nhị phân 0) |
| 0x28 | 1 | thời lượng của bản nhạc: khung |
| 0x29 | 1 | thời lượng của bản nhạc: giây |
| 0x2a | 1 | thời lượng của bản nhạc: phút |
| 0x2b | 1 | một byte rỗng (giá trị nhị phân 0) |

## Người giới thiệu

* [tệp .cda - Theo Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

