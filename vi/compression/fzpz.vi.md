{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp FZPZ - Tệp phần Fritzing",
  "description":"Tìm hiểu về tệp FZPZ là gì và các API có thể tạo và mở tệp FZPZ.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Tệp FZPZ là gì?

Tệp FZPZ là một thành phần/bộ phận được sử dụng trong thiết kế mạch điện tử được tạo bằng ứng dụng thiết kế và tạo nguyên mẫu mạch **Fritzing**. Nó là một kho lưu trữ nén chứa tệp [FZP](/vi/cad/fzp/) và bốn hình ảnh [SVG](/vi/image/svg/) mô tả phần tổng thể trong Fritzing. Ưu điểm của việc sử dụng các tệp này là người dùng có thể chia sẻ các tệp FZPZ của họ với nhau từ quan điểm sử dụng lại. Việc chia sẻ các bộ phận FZPZ giúp tích hợp các bộ phận mạch để tạo ra các thiết kế PCB lớn hơn một cách nhanh chóng.

## Định dạng tệp FZPZ - Thông tin khác

Các tệp FZPZ được lưu vào đĩa dưới dạng lưu trữ nén [ZIP](/vi/compression/zip/). Bạn có thể đổi tên phần mở rộng từ .fzpz thành .zip và sử dụng bất kỳ tiện ích giải nén tiêu chuẩn nào chẳng hạn như WinZIP để giải nén các tệp từ kho lưu trữ.

### Thông tin cấu trúc tệp FZPZ

Như đã đề cập, tệp FZPZ là một tệp lưu trữ chứa nhiều tệp để biểu diễn một bộ phận được sử dụng trong bảng mạch in. FZPZ chứa các tệp sau:

* `Bốn tệp SVG` - đại diện cho hình ảnh breadboard, sơ đồ, PCB và biểu tượng của một phần
* `Tệp FZP` - Một tệp XML chứa thông tin về các thuộc tính, trình kết nối và bus của bộ phận

Các tập tin thường được đặt tên như sau.

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## Người giới thiệu ##

* [Phần mới với phần mở rộng fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

