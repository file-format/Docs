{
  "date" : "2021-07-12",
  "keywords" :[ "tệp cmd", "tệp cmd là gì", "tệp", "ví dụ cmd", "phần mở rộng tệp cmd","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp CMD và các API có thể tạo và mở tệp CMD.",
  "title" :"CMD - Định dạng tệp lệnh Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Tệp CMD là gì?
Tệp CMD bao gồm một tập lệnh chứa một hoặc nhiều lệnh ở dạng văn bản thuần túy được chạy để thực thi các tác vụ khác nhau. Nó tương tự như tệp [BAT](/vi/executable/bat/), cũng thường được sử dụng để lưu trữ một loạt các lệnh thực thi. Các tệp CMD được sử dụng rộng rãi trong hệ điều hành Microsoft Windows. Các tệp này đã được giới thiệu gần như vào những năm 90 nhưng vẫn được sử dụng trong hệ điều hành Windows mới nhất. Các tệp này thường được viết để thực thi nhiều hơn một lệnh trong một trình tự.

## Định dạng tệp CMD
CMD là định dạng tệp được sử dụng bởi các chương trình thực thi kiểu CP/M. Nó thường được so sánh với [COM](/vi/executable/com/) trong CP/M-80 và [EXE](/vi/executable/exe/) trong DOS. Tệp CMD chứa 1 đến 8 nhóm mã hoặc dữ liệu và tiêu đề 128 byte. Mỗi nhóm có thể có kích thước lên tới 1 mb. Các tệp CMD cũng có thể chứa thông tin di chuyển và Phần mở rộng hệ thống thường trú (RSX) trong các phiên bản mới hơn của nó. CMD là một tệp mới so với tệp [BAT](/vi/executable/bat/); được sử dụng cho MS-DOS trước khi phát hành windows Trong MS-DOS. Mặc dù ngày nay bạn vẫn có thể lưu các tệp có phần mở rộng .bat nhưng nhiều người sử dụng phần mở rộng .cmd để lưu các tập lệnh thực thi của họ.

### Đặc tả định dạng CMD

Phần đầu của tiêu đề chứa danh sách các nhóm có trong tệp cùng với các loại của chúng. Mỗi loại chỉ được sử dụng tối đa một lần. Những loại này là:

- Mã số
- Dữ liệu
- Thêm
- Cây rơm
- Người dùng 1
- Người dùng 2
- Người dùng 3
- Người dùng 4
- Mã chia sẻ

Tương tự như vậy, Tiền tố phân đoạn chương trình trong DOS, 256 byte đầu tiên của nhóm dữ liệu bằng không. Chúng sẽ được điền bởi CP/M-86 với trang số không. Nếu không có nhóm dữ liệu, thì 256 byte đầu tiên của nhóm mã sẽ được sử dụng để thay thế.
## Ví dụ về tệp CMD
Sau đây là một ví dụ về tập lệnh CMD để hiển thị thông tin hệ thống.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Người giới thiệu

* [Cách viết tập lệnh CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [Tệp CMD (CP/M) - theo Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

