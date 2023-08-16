{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "file", "extension", "format", "eBook", "Digital book" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp LRF và API có thể tạo và mở tệp LRF.",
  "title" :"Định dạng tệp LRF - Tệp Sony Portable Reader",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Tập tin LRF là gì?

Tệp có phần mở rộng .lrf là tệp Sách điện tử băng thông rộng (BBeB) chứa dữ liệu cho BBeB của Sony, bao gồm văn bản, hình ảnh và dữ liệu phân trang. Tệp được lưu ở định dạng nhị phân nén chứa tiêu đề, một số đối tượng được chỉ định và chỉ mục đối tượng. Các tệp LRF và LRX bao gồm hai định dạng sách BBeB có sẵn. Các tệp LRF không được mã hóa và có thể được biên dịch từ các tệp [LRX](/vi/ebook/lrf/). Các tệp LRF có thể được chuyển đổi từ một số loại tệp khác bao gồm PDF và HTML. Nếu máy tính của bạn không thể mở tệp LRF, thì có thể bạn chưa cài đặt phần mềm để mở hoặc chỉnh sửa tệp LRF. Các chương trình có thể mở tệp LRF là Calibre, BookDesigner, Makelrf và Canon Book Creator cho Windows, Calibre cho Linux, Calibre và Sony Reader cho Macintosh.

## Tóm tắt lịch sử

Loại tệp LRF được liên kết đầu tiên và quan trọng nhất với Line Rider bởi [inXile Entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Line Rider là một đồ chơi vật lý trên internet và được phát minh vào tháng 9 năm 2006 bởi một sinh viên đại học người Slovenia, Boštjan Čadež. Máy đọc sách điện tử thương hiệu Sony (chẳng hạn như đầu đọc Sony PRS-500 và Sony Librie) sử dụng phần mở rộng tệp LRF cho tài liệu và văn bản của họ. Loại tệp độc quyền này hiện đã lỗi thời, cũng như các tệp LRS và LRX có liên quan. Ba loại tệp đó đã tạo nên Sách điện tử BroadBand (BBeB) đã bị ngừng sản xuất vào năm 2010 khi Sony bắt đầu bán sách điện tử của họ ở định dạng EPUB.

## Định dạng tệp LRF

Thông số kỹ thuật chi tiết của định dạng tệp LRF có sẵn tại [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Một tệp LRF bao gồm:
* một tiêu đề
* một số đối tượng
* một chỉ mục đối tượng.

Tất cả các giá trị này đều theo thứ tự Intel (LSB trước).

### Tiêu đề LRF

|Độ lệch (hex) |Kích thước (byte) |Tên/ý nghĩa| Giá trị ví dụ|
---|---|---|---|
|0 |8| Chữ ký LRF| 4C 00 52 00 46 00 00 00 = "LRF" trong Unicode|
|8 |2| phiên bản?| 999 trong hầu hết các tệp|
|A|2| "Mã hóa giả" |byte chính 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| NumberOfObjects |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| không biết| 0|
|24 |1| Cờ| (16 - từ sau ra trước, 1 = từ trước ra sau) 16|
|25 |1| không rõ |(phần đệm?) 0|
|26 |2| không biết| 1600|
|28 |2| không biết| (đệm?) 0|
|2A |2| Chiều cao?| 600|
|2C |2| Chiều rộng?| 800|
|2E |1| không biết| 24|
|2F |1| không rõ |(phần đệm?) 0|
|30 |0x14| không biết| số không|
|44 |4| ID đối tượng của đối tượng PlaneStream (0x1E) duy nhất| 0x0042|
|48 |4| không xác định |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Người giới thiệu

* [Định dạng tệp LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - Theo Wikipedia](https://en.wikipedia.org/wiki/BBeB)

