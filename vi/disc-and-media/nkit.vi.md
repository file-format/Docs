{
  "date" : "2022-04-01",
  "keywords" :[ "tệp nkit", "định dạng tệp nkit", "tệp nkit là gì", "tệp", "ví dụ nkit", "phần mở rộng tệp nkit","tiện ích mở rộng", "định dạng", "chân trang nkit", "tệp định dạng của nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp NKIT và các API có thể tạo và mở tệp NKIT.",
  "title" :"NKIT - Định dạng tệp ảnh đĩa",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Tệp NKIT là gì?

Tệp NKIT là hình ảnh đĩa chứa dữ liệu được trích xuất từ các trò chơi NintendoWii và GameCube. NKIT dành cho định dạng Bộ công cụ Nintendo. Tập tin nén [ISO](/vi/compression/iso/) kết quả sử dụng dữ liệu chính của các trò chơi này để chạy với các chương trình giả lập như Dolphin, Swiss và Nintendont. NKit có các định dạng tệp thô (iso) và nén (gcz), cả hai đều được thiết kế để phù hợp với khả năng chơi và kích thước.

## Định dạng tệp NKIT

Định dạng tệp NKit là định dạng không mất dữ liệu và được sử dụng để thu nhỏ và khôi phục hình ảnh Nintendo Wii và GameCube. Các định dạng có sẵn ở định dạng tệp ISO và GCZ cho từng trò chơi GameCube và Wii.

|Hệ thống |Định dạng |Phần cứng được hỗ trợ |Hỗ trợ cá heo |Có thể khôi phục 1:1 |Ghi chú|
---|---|---|---|---|---|
|GameCube| nkit.iso| Có |Có| Có |Tương tự như GameCube iso nén|
|GameCube| nkit.gcz| Không| Có| Có |GCZ là định dạng nén có thể tìm kiếm theo khối riêng của Dolphin|
|wii| nkit.iso| Không Có| Có| Định dạng RVT-H chỉ có thể chơi được trong Dolphin|
|wii| nkit.gcz| Không Có| Có| RVT-H trong GCZ chỉ có thể chơi được trong Dolphin|

### Tiêu đề NKIT

Tiêu đề định dạng tệp NKIT như sau.

|Chênh lệch |Chiều dài |Tên|
---|---|---|
|0x200 |0x4 |NKit Header 'NKIT'|
|0x204 |0x4 |Phiên bản NKit ' v01'|
|0x208 |0x4 |Ảnh nguồn gốc CRC32|
|0x20C |0x4 |NKit CRC - làm cho tệp NKit CRC32 bằng với CRC nguồn ở 0x208 (ở 0x4 trong GCZ)|
|0x210 |0x4 |Độ dài hình ảnh nguồn|
|0x214 |0x4 |ID rác bắt buộc (Khi ID đĩa khác - hiếm - chỉ dành cho GameCube)|
|0x218 |0x4 |Wii Cập nhật phân vùng CRC32 nếu bị xóa khi chuyển đổi|

## Người giới thiệu ##

* [Định dạng tệp NKit - theo gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

