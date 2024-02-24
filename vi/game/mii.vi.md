{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp MGX mở rộng của Age of Empires 2 và các API có thể tạo và mở tệp MGX.",
  "title" : "Tệp MII - Định dạng tệp Avatar ảo của Wii",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-vi",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Tập tin MII là gì?

Tệp MII là định dạng tệp hình đại diện ảo được sử dụng để lưu trữ hình đại diện ảo trên bảng điều khiển trò chơi Nintendo Wii. Các tệp này chứa thông tin như diện mạo, chuyển động và hoạt ảnh của hình đại diện. Chúng có thể được sử dụng trong trò chơi, ứng dụng mạng xã hội và phần mềm khác trên Wii. Tệp MII cũng chứa các đặc điểm khác về hình đại diện như giới tính, màu tóc, màu da, đặc điểm khuôn mặt và kiểu mắt.

Bạn có thể mở tệp MII bằng cách sử dụng [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## Định dạng tệp MII

Định dạng tệp MII được xác định chi tiết trên [Wii Brew](https://wiibrew.org/wiki/Mii_data). Các chuỗi trong tệp MII được lưu trữ ở định dạng Unicode (UTF-16), big-endian.

### Khối MI

Dữ liệu tệp MII được lưu trữ trên Wiimote thành hai khối. Mỗi khối có chiều dài 750 byte, với 2 byte CRC, tạo thành tổng cộng 752 byte. Mỗi khối bắt đầu bằng một giá trị 4 byte ('RNCD') dường như là con số kỳ diệu cho định dạng tệp MII.

## Làm cách nào để tạo tập tin MII?

Có một số cách khác nhau để tạo hình đại diện cho Nintendo Wii:

1. `Sử dụng kênh Mii tích hợp trên Wii:` Kênh này cho phép bạn tạo hình đại diện tùy chỉnh bằng nhiều công cụ khác nhau, bao gồm đặc điểm khuôn mặt, hình dáng cơ thể và quần áo. Sau khi tạo hình đại diện của mình, bạn có thể lưu nó dưới dạng tệp Mii và sử dụng nó trong trò chơi cũng như phần mềm khác trên Wii.

1. `Sử dụng ứng dụng Mii Maker trên Nintendo 3DS:` Ứng dụng Mii Maker cho phép bạn tạo hình đại diện tùy chỉnh bằng màn hình cảm ứng và máy ảnh trên Nintendo 3DS của bạn. Sau khi tạo hình đại diện của mình, bạn có thể lưu nó dưới dạng tệp Mii và chuyển nó sang Wii thông qua kết nối không dây.

1. `Sử dụng phần mềm của bên thứ ba:` Một số nhà phát triển đã tạo phần mềm cho phép bạn tạo hình đại diện tùy chỉnh cho Wii. Phần mềm này thường được thiết kế để sử dụng trên máy tính và có thể yêu cầu các bước bổ sung để chuyển hình đại diện sang Wii của bạn.

1. `Sử dụng hình đại diện được tạo sẵn:` Một số trò chơi và phần mềm khác trên Wii có thể đi kèm với hình đại diện được tạo sẵn mà bạn có thể sử dụng.

Trong mọi trường hợp, bạn cần có tài khoản Nintendo để tạo và lưu hình đại diện của mình trên Wii.

## Người giới thiệu

* [Trình chỉnh sửa Avatar của tôi](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


