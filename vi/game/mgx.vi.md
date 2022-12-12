{
  "date" : "2021-09-08",
  "keywords" :[ "tệp mgx", "định dạng tệp mgx", "tệp mgx là gì", "tệp", "ví dụ mgx", "phần mở rộng tệp mgx","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp MGX của Age of Empires 2 Expansion Replay và các API có thể tạo và mở tệp MGX.",
  "title" :"MGX - Phát lại bản mở rộng Age of Empires 2",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Tệp MGX là gì?

Tệp có phần mở rộng .mgx là tệp được ghi cho trò chơi Age of Empires II: The Conquerors có thể được phát lại trong chương trình Age of Empires II. Nó chứa bản ghi hoàn chỉnh của chiến dịch do người dùng chơi. Nó có thể được tải và phát lại trong chương trình Age of Empires II. Sau khi chơi lại, trò chơi sẽ hiển thị tất cả các sự kiện và kịch bản mà người dùng đã lên kế hoạch cho chiến dịch và đã chơi.

## Định dạng tệp MGX - Thông tin khác

Định dạng tệp nội bộ của tệp MGX đã được xử lý và có sẵn dưới dạng thông tin được xác thực một phần trên [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx- định dạng). Các thông số kỹ thuật phác thảo các chi tiết trong các phần sau.

### Định nghĩa cấu trúc

Định nghĩa cấu trúc của định dạng tệp GPX được cho là dựa trên [khai báo BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) cung cấp cách đọc và ghi dữ liệu nhị phân có cấu trúc. Điều này cho phép lập trình viên chỉ định định dạng của dữ liệu nhị phân mà sau đó BinData sẽ đọc và ghi.

### Tin nhắn MGX

Tin nhắn MGX dựa trên hai loại tin nhắn.

* GAMESTART - chỉ định các lệnh bắt đầu trò chơi và không được xác thực cho đến nay
* TRÒ CHUYỆN - mô tả tin nhắn trò chuyện trong trò chơi. Cả người chơi và bản thân trò chơi (Gaia) đều có thể phát ra thông báo trong trò chơi.

### HÀNH ĐỘNG TRÒ CHƠI

Có một số [Tác vụ TRÒ CHƠI](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) đã được truy xuất và có thông tin chi tiết.

## Người giới thiệu

* [Age of Empires 2: The Conquerors — Đặc tả định dạng tệp Savegame](https://github.com/stefan-kolb/aoc-mgx-format)

