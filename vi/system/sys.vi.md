{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "phần mở rộng", "tệp", "định dạng", "hệ thống", "Trình điều khiển", "Tệp hệ thống", "chương trình", "máy tính", "ứng dụng" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Định dạng tệp hệ thống",
  "description":"Tìm hiểu về định dạng tệp SYS và API có thể tạo và mở tệp SYS.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Tệp SYS là gì? ##

Các tệp SYS là "Tệp hệ thống" được sử dụng trong các ứng dụng Windows OS và MS-DOS. Không thể mở trực tiếp các tệp này và bao gồm trình điều khiển cũng như cấu hình của thiết bị. Các tệp SYS chịu trách nhiệm chứa các tệp chức năng cốt lõi của hệ điều hành. Đây được coi là các tệp quan trọng của trình điều khiển thiết bị và cũng có thể được sử dụng khi cần giải quyết bất kỳ sự cố nào của trình điều khiển cuộc đua. Chúng chịu trách nhiệm cho hoạt động bình thường của hệ thống máy tính và các tệp .sys phải chính xác và đầy đủ.


## Đặc điểm kỹ thuật ##

Các tệp .sys thực sự là tập hợp con của định dạng [BMP](/vi/image/bmp) vì nó chỉ cho phép các kết hợp cụ thể. Định dạng thông thường của các tệp này là LOGOS.SYS, LOGOW.SYS và LOGO.SYS. Bất kỳ tệp nào khác không có định dạng này.

Các tệp này chủ yếu được sử dụng trong thư mục *C* của Windows tại thời điểm cài đặt. Hầu hết các sự cố xoay quanh trình điều khiển thiết bị đều được giải quyết bằng cách cập nhật HĐH Windows. Có thể xem chi tiết và thông tin của các tệp này bằng cách sử dụng các chương trình tích hợp sẵn của HĐH Windows. Chúng cũng bao gồm các tham chiếu đến các mô-đun khác nhau trong một hệ điều hành.
Một số ví dụ về tệp hệ thống là:

* IO.SYS (Những trình điều khiển thiết bị lưu trữ của hệ điều hành đĩa)
* MSDOS.SYS (Chúng chứa nhân hoặc mã lõi của hệ điều hành)
* CONFIG.SYS (Chúng chứa các tùy chọn cấu hình khác nhau)
* KEYBOARD.SYS (Chúng chứa thông tin liên quan đến bố cục bàn phím)
* COUNTRY.SYS (Những thông tin liên quan đến quốc gia và trang mã này)

## Định dạng tệp SYS ##

Microsoft đã phát triển các tệp có phần mở rộng .sys. Các biến và chức năng được bao gồm trong các tệp SYS. Chúng hầu hết được sử dụng bởi hệ điều hành Microsoft. Các tệp này chủ yếu nằm trong thư mục gốc của đĩa:

* C:\Windows\system32\trình điều khiển
* C:\Windows\WinSxS

Một số cảnh báo phổ biến về các tệp SYS như sau:

* Tên của các tệp này không nên thay đổi vì các tệp này chịu trách nhiệm về các chức năng và biến cốt lõi của hệ điều hành
* Không nên xóa các tệp này vì sự vắng mặt của các tệp này có thể gây ra lỗi
* Không nên tải xuống các tệp .sys từ internet cho đến khi bạn chắc chắn về tính hợp pháp của nguồn
* Người ta không nên gây rối với các tệp này vì việc thay đổi chúng hoặc gây rối với các tệp này sẽ gây ra lỗi hệ thống nghiêm trọng
* Nếu các tệp này bị hỏng do một số vi-rút hoặc phần mềm độc hại, chúng nên được cài đặt lại

## Ví dụ SYS ##

Sau đây là một ví dụ về tệp cấu hình hệ thống SYS đơn giản:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
