{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "phần mở rộng", "tệp", "định dạng", "hệ thống", "Khởi tạo", "phần mở rộng thư mục", "chương trình", "máy tính", "ứng dụng" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Định dạng tệp khởi tạo",
  "description":"Tìm hiểu về định dạng tệp INI và API có thể tạo và mở tệp INI.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Tệp INI là gì? ##

Tệp INI là tài liệu cấu hình thông báo cho các chương trình máy tính có chứa khóa chung cho các đặc điểm và phần tổ chức các thuộc tính theo khung và ngữ pháp. Các tài liệu cấu hình định dạng tệp hệ thống này lấy tên từ phần mở rộng thư mục INI của hệ điều hành MS-DOS, viết tắt của từ khởi tạo. Nó đã phổ biến hình thức thiết lập phần mềm này. Nhiều chương trình trên các ứng dụng phần mềm khác sử dụng nhiều phần bổ sung tên tệp khác nhau, chẳng hạn như CONF và [CFG](/vi/system/cfg/), mặc dù định dạng này đã thiết lập một tiêu chuẩn không chính thức trong nhiều tình huống cấu hình.

## Tóm tắt lịch sử của tệp INI##

Ban đầu, kỹ thuật cấu hình chương trình chính của Windows là một định dạng tệp văn bản bao gồm các dòng văn bản với một cặp quan trọng trên mỗi dòng, được chia thành các phần. Trình điều khiển thiết bị, kiểu chữ và trình khởi chạy đều được lưu trữ ở định dạng này. Các cài đặt riêng lẻ cũng thường được ứng dụng lưu trữ trong các tệp INI.
Cho đến Windows 3.1x, định dạng này được hỗ trợ trên nền tảng Microsoft Windows 16-bit. Bắt đầu với Windows 95, Microsoft bắt đầu khuyến khích các nhà phát triển sử dụng Windows Registry thay vì các tệp INI để cấu hình.

## Tệp INI - Thông số kỹ thuật định dạng tệp

### Phím/Thuộc tính ###

Khóa/thuộc tính là thành phần cơ bản nhất của tệp INI. Ký hiệu bằng (=) phân tách tên và giá trị của từng khóa. Ở bên trái của dấu bằng là nơi hiển thị tên. Biểu tượng bằng và dấu chấm phẩy là các chữ cái kín đáo trong hệ thống Windows do đó không thể được sử dụng trong khóa. Bất kỳ ký tự nào cũng có thể được sử dụng trong giá trị.

```
name=value
```

### Phần ###

Phần chú thích xuất hiện trong dấu ngoặc vuông ([]) trên dòng riêng của nó. Sau phần định nghĩa, tất cả các phím được liên kết với phần đó. Các phần kết thúc ở phần chỉ định phần tiếp theo hoặc phần cuối của tài liệu; không có dấu phân cách "cuối phần" cụ thể. Các phần không thể được xếp chồng lên nhau; chúng chỉ có thể được đặt tên một lần và không bắt buộc phải được liên kết.

```
[section]
a=a
b=b
```

### Thay đổi tính năng ###

Định dạng tệp INI không có định nghĩa được chấp nhận trên toàn cầu. Nhiều ứng dụng máy tính bao gồm các chức năng ngoài những chức năng đã được đề cập. Danh sách dưới đây bao gồm một số đặc điểm chung có thể có hoặc không có trong bất kỳ chương trình riêng lẻ nào.

* Bình luận
* Nhân vật trốn thoát
* Tên trùng lặp


## Ví dụ INI ##

Tệp INI mẫu trông như sau:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Tài liệu tham khảo ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

