{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Bộ giải mã video hiệu quả cao",
  "description":"Tìm hiểu về định dạng tệp IDX và các API có thể tạo và mở tệp IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Tệp IDX là gì?

Tệp IDX là tệp chỉ mục phụ đề trỏ đến danh sách thông tin siêu dữ liệu cho phụ đề bên trong tệp .sub (Phụ đề VobSub). Nó được tạo và sử dụng bởi ứng dụng phần mềm VobSub cho phép người dùng trích xuất phụ đề từ DVD và kết xuất thành tệp SUB. Các tệp IDX chứa dấu thời gian và độ lệch byte được sử dụng để trỏ đến từng phụ đề. VobSub luôn tạo tệp IDX cùng với tệp SUB tương ứng.

## Định dạng tệp IDX - Thông tin khác

Các tệp IDX được tạo và lưu dưới dạng tệp văn bản thuần túy có thể được mở trong bất kỳ trình soạn thảo văn bản nào. Tệp IDX chứa thông tin được trình phát phương tiện đọc để đọc các tham số như màu của văn bản phụ đề sẽ hiển thị trên màn hình, vị trí của văn bản phụ đề trên màn hình.

### Cài đặt phụ đề IDX

Tệp IDX điển hình lưu trữ thông tin siêu dữ liệu này ở đầu tệp. Cài đặt phụ đề bắt đầu bằng **#**. Dấu thời gian và tham chiếu hình ảnh được thêm sau tất cả các cài đặt phụ đề này và bắt đầu bằng **dấu thời gian:**.

## Ví dụ về định dạng tệp IDX

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## Làm cách nào để sử dụng tệp IDX?

Nếu bạn có các tệp Sub và IDX cho một bộ phim, bạn có thể phát lại các phụ đề này cùng với bộ phim mà chúng được tạo. Nhiều ứng dụng như VLC, GOM Player, PotPlayer hoặc PowerDVD có khả năng tải các tệp SUB và IDX này và phát các tệp này cùng với phim. Các ứng dụng phần mềm cũng có thể nhúng tệp phụ đề SUB và IDX vào tệp [.mkv](/vi/video/mkv/).

## Chuyển đổi IDX sang SRT

[SRT](/vi/video/srt/) (Định dạng tệp SubRip) là một tệp phụ đề đơn giản được lưu ở định dạng tệp SubRip. Nó được sử dụng phổ biến hơn so với định dạng tệp VobSub. Do đó, nếu bạn muốn chuyển đổi tệp SUB/IDX sang định dạng tệp SRT, có sẵn các công cụ của bên thứ 3 có thể được sử dụng để đạt được điều này. Trình chuyển đổi SUB/IDX sang SRT, có sẵn trên SubtitleTools.com là một trong những công cụ lấy tệp SUB và IDX làm đầu vào và chuyển đổi các phụ đề VobSub này thành tệp SRT.

## Người giới thiệu

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki đa phương tiện](https://wiki.multimedia.cx/index.php?title=VOBsub)

