{
  "date" : "2021-03-09",
  "keywords" :[ "TCR", "Psion", "phần mở rộng", "định dạng", "Sách điện tử" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp TCR cho sê-ri Psion 3 và các API có thể tạo và mở tệp tcr.",
  "title" :"TCR - Tệp sách điện tử Dòng Psion 3",
  "linktitle" : "TCR",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-09"
}

## Tệp TCR là gì?

Vào đầu những năm 90, định dạng tệp TCR đã được giới thiệu cho các thiết bị máy tính bảng **Psion Series 3** cổ xưa. Công ty đã sử dụng tính năng nén dành riêng cho nền tảng của mình và định dạng này hỗ trợ rất hạn chế cho định dạng văn bản. Đây là định dạng tệp dựa trên ZVR và cung cấp tốc độ nén tương đối tốt hơn so với PalmDOC. Nó cũng hoạt động rất tốt với FontMachine. Mặc dù định dạng tệp TCR thuộc về một thiết bị đã ngừng sản xuất, nhưng vẫn có thể đọc được định dạng tệp này bằng cách sử dụng một số thiết bị đọc sách điện tử. Định dạng tệp này cũng có thể được xem trên máy tính để bàn với Sumatra PDF và với ứng dụng Calibre trong Windows và Linux.

## chi tiết kỹ thuật

Vì định dạng tệp TCR dựa trên máy nén ZVR có khả năng giảm nhiều tệp khoảng 50% kích thước ban đầu của chúng. Lược đồ nén được over sử dụng hơi cũ. Tệp nén bắt đầu bằng một từ điển gồm 256 ký hiệu có thể có trong tệp nén. Từ điển chứa một chuỗi thay thế cố định cho mỗi ký hiệu này. Quá trình giải nén đã trở nên rất nhanh ngay cả trong OPL và nó có thể bắt đầu tại bất kỳ điểm nào trong tệp nén.

## Sự cố khi mở tệp TCR ##

Nếu bạn không thể mở và chạy tệp TCR; điều đó không có nghĩa là bạn chưa cài đặt phần mềm phù hợp trên thiết bị của mình. Có thể có một số vấn đề khác khiến tệp không hoạt động bình thường. Các vấn đề có thể xảy ra có thể là một trong những vấn đề sau:

- Tệp TCR bị hỏng.
- Liên kết sai đến tệp TCR trong các mục đăng ký.
- Đã xóa mô tả về TCR khỏi sổ đăng ký Windows
- Lỗi cài đặt ứng dụng hỗ trợ định dạng TCR
- Tệp TCR bị nhiễm phần mềm độc hại không mong muốn.
- Máy tính không có đủ tài nguyên phần cứng để vận hành tệp TCR.
- Trình điều khiển mà máy tính sử dụng để mở tệp TCR đã lỗi thời.




## Người giới thiệu

* [TCR - Bởi MobileRead](https://wiki.mobileread.com/wiki/TCR)
* [Trình đọc tệp văn bản nén ZVR](https://iay.org.uk/zvr/)

