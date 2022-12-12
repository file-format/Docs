{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "file", "extension", "format", "mod file format", "music", "mod file format", "mod vs MP3", "mod file format spec "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp MOD và API có thể tạo, chuyển đổi và mở tệp MOD.",
  "title" :"MOD - Tệp mô-đun âm nhạc",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Tệp MOD là gì?
Tệp có phần mở rộng .mod là tệp mô-đun nhạc được tạo bằng cách sử dụng định dạng mô-đun nhạc tiêu chuẩn, dựa trên **Định dạng mô-đun Amiga** do Karsten Obarski phát triển và được phát hành cùng với phần mềm **Ultimate Soundtracker** cho Commodore Hệ thống Amiga Tương tự như tệp [MIDI](/vi/audio/mid/), tệp này bao gồm các mẫu nốt và mẫu âm thanh, đại diện cho các nhạc cụ khác nhau được phát lại theo các nốt. Các tệp MOD được sử dụng đặc biệt trong các trò chơi điện tử làm nhạc nền và trong tiểu văn hóa nghệ thuật máy tính **demoscene**.

## Định dạng tệp MOD

MOD là một định dạng tệp máy tính được sử dụng chức năng cơ bản của nó là thể hiện âm nhạc và đó là định dạng tệp mô-đun đầu tiên. Các tệp MOD sử dụng phần mở rộng tệp .mod, ngoại trừ **Amiga** đọc tiêu đề của tệp để xác định loại tệp, do đó, nó không dựa vào phần mở rộng tên tệp. Tệp MOD bao gồm một tập hợp các nhạc cụ khác nhau ở dạng mẫu, một số mẫu chỉ định cách thức và thời điểm phát các mẫu cũng như danh sách các mẫu sẽ chơi theo thứ tự nào.

### Thông số định dạng tệp MOD

Mẫu tệp MOD thực sự được thiết kế trong giao diện người dùng trình sắp xếp thứ tự dưới dạng một bảng có một cột trên mỗi kênh, vì vậy bảng này có bốn cột (một cột cho mỗi kênh phần cứng Amiga. Mỗi cột có 64 hàng).

Một ô trong bảng có thể khiến một trong các hành động sau đây xảy ra trên kênh của cột khi đạt đến thời gian của hàng:

- Bắt đầu một nhạc cụ chơi một nốt mới trong kênh này ở một âm lượng nhất định, có thể với hiệu ứng đặc biệt được áp dụng trên đó
- Thay đổi âm lượng hoặc hiệu ứng đặc biệt đang được áp dụng cho ghi chú hiện tại
- Thay đổi luồng mẫu; chuyển đến một bài hát hoặc vị trí mẫu cụ thể hoặc lặp lại bên trong một mẫu
- Không làm gì cả; mọi ghi chú hiện có đang phát trong kênh này sẽ tiếp tục phát

Một nhạc cụ là một mẫu duy nhất cùng với thông số kỹ thuật tùy chọn trong đó phần nào của mẫu có thể được lặp lại để giữ một nốt chắc chắn.

### Thời gian
Khung thời gian tối thiểu là 0,02 giây trong tệp MOD gốc hoặc khoảng thời gian "dọc trống" (VSync), vì phần mềm gốc đã sử dụng thời gian VSync của màn hình chạy ở 50 Hz (đối với PAL) hoặc 60 Hz (đối với NTSC) cho thời gian.

## Người giới thiệu

* [MOD (định dạng tệp) - Theo Wikipedia](https://vi.wikipedia.org/wiki/MOD_(file_format))

