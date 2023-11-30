{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp RMT - Định dạng tệp chương trình cơ sở của bộ định tuyến",
  "description":"Tìm hiểu về định dạng tệp RMT và các API có thể tạo và mở tệp RMT.",
  "linktitle" : "RMT",
  "menu" : {
    "docs" : {
      "identifier":"system-rmt",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Một tập tin RMT là gì?

Tệp RMT là tệp chương trình cơ sở bao gồm phần mềm chạy trên phần cứng của bộ định tuyến. Nó dành riêng cho chế độ hoặc dòng của bộ định tuyến và chứa các hướng dẫn cần thiết để khởi động và hoạt động bình thường. Khi bộ định tuyến được BẬT nguồn, chương trình cơ sở sẽ khởi động và thực hiện các hướng dẫn khởi động thiết bị. Hầu hết các bộ định tuyến đều có tập tin chương trình cơ sở được cài đặt sẵn.

Các tệp RMT thường có thể được cập nhật bằng cách kết nối với bộ định tuyến trong trình duyệt web và cập nhật tệp chương trình cơ sở.

## Định dạng tệp RMT - Thông tin thêm

Các tệp RMT được lưu ở định dạng tệp nhị phân và có thể được cập nhật qua trình duyệt web.

### Thành phần bên trong của File RMT

Một số thành phần cụ thể có thể có trong tệp rmt có thể bao gồm:

`Bootloader:` Đây là phần mềm chạy trên bộ định tuyến khi nó được bật lần đầu tiên. Nó chịu trách nhiệm tải firmware và bắt đầu quá trình khởi động.

`Kernel:` Kernel là thành phần cốt lõi của phần sụn quản lý tài nguyên phần cứng của bộ định tuyến và cung cấp một bộ dịch vụ cơ bản mà các phần khác của phần sụn có thể xây dựng trên đó.

`Trình điều khiển thiết bị:` Đây là các thành phần phần mềm cho phép chương trình cơ sở giao tiếp với các thành phần phần cứng cụ thể trong bộ định tuyến, chẳng hạn như giao diện mạng, radio không dây hoặc thiết bị lưu trữ.

`Giao diện người dùng:` Nhiều chương trình cơ sở của bộ định tuyến bao gồm giao diện web cho phép người dùng định cấu hình cài đặt bộ định tuyến và quản lý mạng. Tệp .rmt có thể chứa phần mềm cung cấp giao diện này.

`Giao thức mạng:` Phần sụn có thể bao gồm nhiều giao thức mạng khác nhau, chẳng hạn như TCP/IP, DHCP, DNS và các giao thức khác, cho phép bộ định tuyến giao tiếp với các thiết bị khác trên mạng và với Internet.

`Tính năng bảo mật:` Phần sụn có thể bao gồm nhiều tính năng bảo mật khác nhau, chẳng hạn như tường lửa, hỗ trợ VPN hoặc hệ thống phát hiện xâm nhập, giúp bảo vệ bộ định tuyến và mạng khỏi bị truy cập hoặc tấn công trái phép.

## Thẩm quyền giải quyết

* [Bộ định tuyến là gì?](https://en.wikipedia.org/wiki/Router_(computing))

