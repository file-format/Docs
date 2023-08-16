{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp MPG",
  "keywords" :[ "MPG", "tệp", "phần mở rộng", "định dạng", "định dạng video","định dạng tệp mpg là gì", "định dạng tệp mpg", "trình phát tệp mpg","nén mpeg", "video ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Tìm hiểu về định dạng tệp MPG và API có thể tạo và chỉ ra cách mở tệp MPG.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Định dạng tệp MPG là gì? ##

Tệp có phần mở rộng .mpg thuộc nhóm các phần mở rộng tệp để nén âm thanh và video MPEG-1 hoặc MPEG-2. Video MPEG-1 Phần 2 không dễ có sẵn và phần mở rộng này (định dạng tệp MPG) thường trỏ đến luồng chương trình MPEG được xác định trong MPEG-1 và MPEG-2 hoặc luồng truyền tải MPEG được xác định trong MPEG-2 . Các phần mở rộng khác như .m2ts cũng tồn tại chỉ định vùng chứa chính xác, trong trường hợp này là MPEG-2 TS, nhưng phần mở rộng này ít liên quan đến phương tiện MPEG-1. [.mp3](https://docs.fileformat.com/audio/mp3/) là phần mở rộng phổ biến nhất cho các tệp chứa âm thanh MP3. Tệp MP3 là một luồng âm thanh thô điển hình; cách truyền thống để gắn thẻ các tệp MP3 là ghi dữ liệu luồng vào các phân đoạn "rác" của mỗi khung, phân đoạn này lưu thông tin phương tiện nhưng bị **trình phát tệp **mpg loại bỏ. Đây là một kỹ thuật tương tự được sử dụng để gắn thẻ các tệp AAC, nhưng ngày nay ít được hỗ trợ hơn.

## Nén MPEG ##

Tên MPEG là viết tắt của Nhóm chuyên gia hình ảnh chuyển động. MPEG là một công cụ nén video, bao gồm nén hình ảnh và âm thanh, cũng như đồng bộ hóa cả hai.
Hiện tại có một số tiêu chuẩn MPEG.

- MPEG-1 được đề xuất cho tốc độ dữ liệu trung gian, theo thứ tự 1,5 Mbit/giây.
- MPEG-2 được đề xuất cho tốc độ dữ liệu cao ít nhất là 10 Mbit/giây.
- MPEG-3 được đề xuất cho việc nén HDTV nhưng được cho là không cần thiết và đã được hợp nhất với MPEG-2.
- MPEG-4 được đề xuất cho tốc độ dữ liệu rất thấp dưới 64 Kbit/giây.


## Luồng chương trình định dạng tệp MPG ##

Luồng chương trình là một vùng chứa để ghép kênh âm thanh kỹ thuật số, video, v.v. Định dạng Luồng chương trình được chỉ định trong phần 1 của MPEG-1 (ISO/IEC 11172-1) và phần 1 của MPEG-2, Hệ thống (tiêu chuẩn ISO/IEC 13818-1/ITU-T H.222.0). Luồng chương trình MPEG-2 dựa trên analog và tương tự như lớp Hệ thống ISO/IEC 11172 và tương thích chuyển tiếp.

### Chi tiết mã hóa ###

Dưới đây là chi tiết mã hóa của một phần định dạng tiêu đề gói Luồng chương trình MPEG-2:

| Tên | Số bit | Mô tả |
---|---|---|
| đồng bộ byte | 32 | 0x000001BA |
| bit đánh dấu | 2 | 01b cho phiên bản MPEG-2. Các bit đánh dấu cho phiên bản MPEG-1 là 4 bit với giá trị 0010b. |
| Đồng hồ hệ thống [32..30] | 3 | Các bit Tham chiếu Đồng hồ Hệ thống (SCR) 32 đến 30 |
| bit đánh dấu | 1 | 1 Bit luôn được đặt. |
| Đồng hồ hệ thống [29..15] | 15 | Bit đồng hồ hệ thống 29 đến 15 |
| bit đánh dấu | 1 | 1 Bit luôn được đặt. |
| Đồng hồ hệ thống [14..0] | 15 | Bit đồng hồ hệ thống từ 14 đến 0 |
| bit đánh dấu | 1 | 1 Bit luôn được đặt. |
| mở rộng SCR | 9 | |
| bit đánh dấu | 1 | 1 Bit luôn được đặt. |
| tốc độ bit | 22 | Trong đơn vị 50 byte mỗi giây. |
| bit đánh dấu | 2 | 11 bit luôn được đặt. |
| dành riêng | 5 | dành để sử dụng trong tương lai |
| nhồi chiều dài | 3 | |
| nhồi byte | Chiều dài nhồi 8 * | |
| tiêu đề hệ thống (tùy chọn) | 0 trở lên | nếu mã bắt đầu tiêu đề hệ thống sau: 0x000001BB |

Bảng sau đây hiển thị định dạng tiêu đề một phần hệ thống:

| Tên | Số byte | Mô tả |
---|---|---|
| đồng bộ byte | 4 | 0x000001BB |
| chiều dài tiêu đề | 2 | |
| tốc độ bị ràng buộc và bit đánh dấu | 3 | |
| ràng buộc âm thanh và cờ | 1 | |
| cờ, bit đánh dấu và liên kết video | 1 | |
| Hạn chế tốc độ gói và byte dành riêng | 1 | |


## Người giới thiệu ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



