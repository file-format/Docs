{
  "date" : "2021-09-02", 
  "keywords" :[ "TCL", "file", "extension", "file format", "tickle", "Programming Guide", "tcl example", "TCL language", "initiаlism", "Tооl Соmmаnd Language" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCL - Tооl Соmmаnd Language File",
  "description":"Tìm hiểu về định dạng tệp TCL và các API có thể tạo và mở tệp TCL.",
  "linktitle" : "TCL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-02"
}

## Tệp TCL là gì?

TCL (được phát âm là "tickle" hoặc như một chủ nghĩa khởi tạo) là một ngôn ngữ lập trình cấp cao, có mục đích chung, được diễn giải, động. Nó được thiết kế với mục tiêu rất đơn giản nhưng mạnh mẽ. TCL truyền mọi thứ vào khuôn của một lệnh, thậm chí cả các cấu trúc lập trình như phép gán biến và định nghĩa thủ tục. Ngôn ngữ TCL hỗ trợ nhiều mô hình lập trình, bao gồm các kiểu lập trình hoặc phong cách lập trình theo hướng đối tượng, mệnh lệnh và chức năng.

## Định dạng tệp TCL ##

TCL thường được sử dụng để nhúng vào các ứng dụng С, dành cho quá trình tạo mẫu nhanh, các ứng dụng được lập kịch bản, GUI và thử nghiệm. Trình thông dịch TCL có sẵn cho nhiều hệ thống đang hoạt động, cho phép mã TCL chạy trên nhiều hệ thống khác nhau. Bởi vì TCL là một ngôn ngữ rất linh hoạt, nó được sử dụng trên các nền tảng hệ thống nhúng, cả ở dạng đầy đủ và trong một số phiên bản nền tảng nhỏ khác.

Sự kết hợp phổ biến của TCL với tiện ích mở rộng Tk được gọi là TCL/TK và cho phép xây dựng giao diện người dùng đồ họa (GUI) nguyên bản trong TCL. TCL/TK được bao gồm trong cài đặt Рythоn tiêu chuẩn ở dạng Tkinter. TCL giao tiếp tự nhiên với ngôn ngữ С. Điều này là do ban đầu nó được viết để trở thành một khung cung cấp một giao diện người dùng tổng hợp cho các câu lệnh được viết bằng С và tất cả các câu lệnh trong ngôn ngữ (bao gồm cả những thứ có thể là từ khóa, chẳng hạn như nếu trong khi đó) được sử dụng theo cách này.

Ngôn ngữ TCL luôn được phép sử dụng cho các gói mở rộng, cung cấp chức năng bổ sung, chẳng hạn như GUI, tự động hóa ứng dụng dựa trên thiết bị đầu cuối, cơ sở dữ liệu, v.v. TCL là một ngôn ngữ lập trình được diễn giải bằng nguồn mở hoàn toàn đơn giản cung cấp các tiện ích thông thường như biến, thủ tục và cấu trúc kiểm soát giao diện cũng như nhiều tính năng hữu ích không có sẵn.


## Lược Sử ##

Ngôn ngữ lập trình TCL được tạo ra vào mùa xuân năm 1988. Ban đầu "sinh ra từ sự thất vọng", tùy thuộc vào tác giả, với các lập trình viên nghĩ ra ngôn ngữ riêng của họ nhằm mục đích nhúng vào các ứng dụng, Tаwnable. Оusterhout đã được trao giải thưởng vào năm 1997 cho TCL/TK. Tên ban đầu bắt nguồn từ Ngôn ngữ ngôn ngữ công cụ, nhưng được đánh vần theo cách thông thường là "TCL" thay vì "TСL". Keo đơn giản hơn giúp công việc dễ dàng hơn.


## Đặc điểm kỹ thuật ##

Tất cả các hoạt động đều là mệnh lệnh, bao gồm cả cấu trúc ngôn ngữ. Chúng được viết bằng ký hiệu tiền tố. Các lệnh thường chỉ chấp nhận một số đối số có thể thay đổi. Mọi thứ có thể được xác định lại một cách linh hoạt và vượt qua. Thực tế, không có từ khóa nào, vì vậy thậm chí các cấu trúc điều khiển có thể được thêm hoặc thay đổi, mặc dù điều này không được khuyến khích. Tất cả các loại dữ liệu có thể được thao tác dưới dạng các chuỗi, bao gồm cả mã nguồn.

Về nội bộ, các biến có các loại như số nguyên và gấp đôi, nhưng việc chuyển đổi hoàn toàn là tự động. Các biến không được khai báo, nhưng được gán cho. Việc sử dụng một biến không xác định sẽ dẫn đến lỗi. Hệ thống đối tượng dựa trên lớp hoàn toàn năng động, TсlОО, bao gồm các tính năng nâng cao như siêu lớp, bộ lọc và mixin. Giao diện hướng sự kiện đến ổ cắm và tệp. Các sự kiện dựa trên thời gian và do người dùng xác định cũng có thể thực hiện được. Theo mặc định, khả năng hiển thị có thể thay đổi bị hạn chế đối với phạm vi từ vựng (tĩnh) nhưng cấp độ cao hơn và nâng cấp cho phép các chương trình tương tác với các phạm vi chức năng kèm theo.

Tất cả các lệnh do chính TCL xác định đều tạo ra thông báo lỗi khi sử dụng không chính xác. Khả năng mở rộng, thông qua С, С++, Jаvа, Рythоn và TCL. Ngôn ngữ được giải thích bằng cách sử dụng mã byte. Full Uniсоde (3.1 ngay từ đầu, được cập nhật thường xuyên) hỗ trợ được phát hành lần đầu tiên vào năm 1999.

Safe-Tcl là một tập hợp con của TCL có các tính năng bị hạn chế để các tập lệnh TCL không thể gây hại cho máy chủ hoặc ứng dụng của họ. Safe-Tcl có thể được bao gồm trong e-mail khi ứng dụng/safe-tсl và nhiều tác phẩm/enabled-mail được hỗ trợ. Kể từ đó, tính năng của Safe-Tсl đã được tích hợp như một phần của các bản phát hành TCL/TK tiêu chuẩn.


## Ví dụ về định dạng tệp TCL ##

```
puts "Hello, World!"

oo::class create fruit {
    method eat {} {
        puts "yummy!"
}
}
oo::class create banana {
    superclass fruit
    constructor {} {
        my variable peeled
        set peeled 0
}
    method peel {} {
        my variable peeled
        set peeled 1
        puts "skin now off"
}
    method edible? {} {
        my variable peeled
        return $peeled
}
    method eat {} {
        if {![my edible?]} {
            my peel
    }
        next
}
}
set b [banana new]
$b eat               → prints "skin now off" and "yummy!"
fruit destroy
$b eat               → error "unknown command"
```

## Tài liệu tham khảo ##

* [TCL - theo Wikipedia](https://vi.wikipedia.org/wiki/Tcl)



