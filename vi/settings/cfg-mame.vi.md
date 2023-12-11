{
"ngày": "27-09-2023",
  "keywords": [
"cfg",
"tệp cfg",
"tệp cấu hình cfg mame",
"tập tin cfg là gì",
"cách mở tệp cfg",
"tài liệu",
"phần mở rộng tập tin cfg",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp CFG - Tệp cấu hình MAME",
  "description":"Tìm hiểu về định dạng tệp cấu hình CFG MAME và các API có thể tạo và mở tệp CFG.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
      "parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## Tập tin CFG là gì?

Tệp CFG là tệp cấu hình bàn phím XML được sử dụng bởi trình giả lập trò chơi điện tử arcade MAME. Nó là thành phần quan trọng để tùy chỉnh điều khiển bàn phím và phím nóng cho phù hợp với sở thích của người chơi. Các tệp này lưu trữ ánh xạ và cài đặt xác định cách bàn phím tương tác với trình mô phỏng khi chơi trò chơi. Bằng cách chỉnh sửa tệp này, người dùng có thể điều chỉnh trải nghiệm chơi trò chơi của mình bằng cách gán các phím bàn phím cụ thể cho các hành động trong trò chơi, chẳng hạn như chèn xu, bắt đầu, di chuyển và nhiều chức năng khác.

## Tệp cấu hình MAME

MAME, viết tắt của **Multiple Arcade Machine Emulator**, là ứng dụng phần mềm cho phép bạn mô phỏng và chơi các trò chơi arcade trên máy tính của mình. MAME sử dụng các tệp cấu hình để tùy chỉnh hành vi và cài đặt của nó. Các tệp cấu hình này thường nằm trong thư mục `cfg` trong thư mục MAME của bạn.

Dưới đây là các tệp cấu hình chính bạn có thể gặp khi thiết lập và định cấu hình MAME:

1. **mame.ini:** Đây là tệp cấu hình chính cho MAME. Nó chứa các cài đặt chung áp dụng cho tất cả các trò chơi. Bạn có thể tìm thấy tệp này trong thư mục gốc của bản cài đặt MAME.

1. **default.cfg:** Tệp này lưu trữ cài đặt mặc định cho tất cả các trò chơi không có tệp cấu hình riêng. Nó được sử dụng làm dự phòng cho các cài đặt dành riêng cho trò chơi.

1. **game-cụ thể.cfg:** Những tệp này được sử dụng để lưu trữ cài đặt cho từng trò chơi. Chúng thường được đặt tên theo tệp ROM của trò chơi mà chúng tương ứng. Ví dụ: nếu bạn có trò chơi có tên "pacman.zip", tệp cấu hình cho trò chơi đó sẽ là "pacman.cfg."

Dưới đây là một số cài đặt phổ biến bạn có thể tìm thấy trong tệp cấu hình MAME.

1. **rompath:** Chỉ định thư mục chứa ROM trò chơi arcade của bạn.

1. **cfg_directory:** Chỉ định thư mục lưu trữ các tệp cấu hình dành riêng cho trò chơi.

1. **nvram_directory:** Chỉ định thư mục lưu trữ các tệp RAM cố định (NVRAM). NVRAM lưu trữ điểm cao và dữ liệu cụ thể khác của trò chơi.

1. **artwork_directory:** Chỉ định thư mục lưu trữ các tệp tác phẩm nghệ thuật (chẳng hạn như bezels, marquees và tờ rơi).

1. **samplepath:** Chỉ định thư mục chứa các tệp âm thanh mẫu.

1. **cheatpath:** Chỉ định thư mục chứa các tệp cheat.

Bạn cũng có thể định cấu hình nhiều cài đặt khác như tùy chọn video và âm thanh, điều khiển và thiết bị đầu vào. Để sửa đổi các cài đặt này, bạn có thể mở tệp cấu hình trong trình soạn thảo văn bản và thực hiện các thay đổi cần thiết.

## MAME

MAME, viết tắt của **"Trình mô phỏng nhiều máy trò chơi điện tử"** là ứng dụng phần mềm được thiết kế để mô phỏng và tái tạo phần cứng của máy trò chơi điện tử cổ điển và bảng điều khiển trò chơi điện tử. Nó cho phép người dùng chơi thư viện trò chơi arcade cổ điển khổng lồ trên máy tính hiện đại và các thiết bị tương thích khác. MAME là một dự án nguồn mở và đã trở thành trình giả lập phù hợp để bảo tồn và tận hưởng lịch sử phong phú của trò chơi arcade.

1. **Giả lập:** Mục đích chính của MAME là mô phỏng chính xác phần cứng của máy arcade, bao gồm bộ xử lý trung tâm (CPU), chip âm thanh, chip đồ họa và thiết bị đầu vào. Mức độ chính xác này đảm bảo rằng trò chơi hoạt động gần với trải nghiệm arcade gốc nhất có thể.

1. **Khả năng tương thích:** MAME hỗ trợ nhiều loại ROM trò chơi arcade, khiến nó trở thành một trong những trình giả lập arcade toàn diện nhất hiện có. Nó có thể chạy các trò chơi từ nhiều nền tảng arcade khác nhau, bao gồm các trò chơi cổ điển từ thập niên 70, 80, 90 và thậm chí một số tựa game arcade gần đây hơn.

1. **Bảo quản:** Một trong những nhiệm vụ chính của MAME là bảo tồn lịch sử trò chơi điện tử. Bằng cách mô phỏng chính xác phần cứng arcade, MAME giúp ngăn chặn tình trạng mất các trò chơi cổ điển và đảm bảo rằng các thế hệ tương lai có thể trải nghiệm chúng như dự định ban đầu.

1. **Giao diện người dùng:** Nhiều người dùng sử dụng các ứng dụng giao diện người dùng cung cấp giao diện đồ họa để quản lý và khởi chạy trò chơi thông qua MAME. Những giao diện người dùng này giúp điều hướng thư viện trò chơi phong phú của MAME dễ dàng hơn.

## Làm cách nào để mở tập tin CFG?

Các chương trình mở hoặc tham chiếu tệp CFG

- MAME (Miễn phí) (Windows)
- ExtraMAME (Bản dùng thử)
- MacMAME (MAC)

## Các tập tin CFG khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.cfg**.

**Cài đặt**
- [CFG - Tệp cấu hình Celestia](/vi/settings/cfg-celestia/)
- [CFG - Tệp kết nối máy chủ Citrix](/vi/settings/cfg-citrix/)
- [CFG - Tệp cấu hình MAME](/vi/settings/cfg-mame/)
- [CFG - Tệp cấu hình LightWave](/vi/settings/cfg-lightwave/)

**Trò chơi**
- [CFG - Tệp ngôn ngữ đánh dấu Wesnoth](/vi/game/cfg-wesnoth/)
- [CFG - Tệp cấu hình MUGEN](/vi/game/cfg-mugen/)
- [CFG - Tệp cấu hình công cụ nguồn](/vi/game/cfg-sourceengine/)

**Hệ thống & Linh tinh**
- [Tệp CFG - CFG](/vi/system/cfg/)
- [CFG - Tệp cấu hình mô hình Cal3D](/vi/misc/cfg-cal3d/)

## Người giới thiệu
* [MAME](https://en.wikipedia.org/wiki/MAME)

