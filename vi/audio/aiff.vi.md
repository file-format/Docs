{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "file", "extension", "format", "audio exchange file format", "music", "aiff file format", "aiff to mp3", "aiff vs wav", "convert aiff to mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp AIFF và API có thể tạo, chuyển đổi và mở tệp AIFF.",
  "title" :"AIFF - Định dạng tệp trao đổi âm thanh",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Tệp AIFF là gì?
AIFF (Định dạng tệp trao đổi âm thanh) là định dạng tệp âm thanh không nén do Apple phát triển vào năm 1998, nhưng dựa trên **EA IFF 85** (Tiêu chuẩn cho các tệp định dạng trao đổi do Electronic Arts phát triển), một định dạng trình bao được sử dụng trên các hệ thống Amiga . Định dạng tệp này đưa ra một tiêu chuẩn để lưu trữ các âm thanh được lấy mẫu. Định dạng này đủ linh hoạt và cho phép lưu trữ âm thanh được lấy mẫu đơn kênh hoặc đa kênh ở các tốc độ lấy mẫu và độ rộng mẫu khác nhau. Vì các tệp AIFF không được nén nên điều này làm cho chúng có kích thước lớn hơn so với các định dạng mất dữ liệu khác như [MP3](https://docs.fileformat.com/audio/mp3/).

Các tệp AIFF bao gồm 2 kênh âm thanh nổi không nén với kích thước mẫu 16 bit, được ghi ở 44,1 khz. Do chất lượng âm thanh cao nên âm thanh 5 phút có thể chiếm tới 50 MB dung lượng ổ đĩa, tương tự như định dạng tệp [WAV](https://docs.fileformat.com/audio/wav/).

## AIFF so với WAV

AIFF và WAV gần như giống nhau về chất lượng. Cả hai đều sử dụng cùng một mã hóa PCM (điều biến mã xung), giúp chúng có kích thước lớn hơn so với các định dạng mất dữ liệu khác, chẳng hạn như [MP3](https://docs.fileformat.com/audio/mp3/), [M4A](). Một số khác biệt chung được viết trong bảng dưới đây:

|AIFF|WAV|
---|---|
|Được sử dụng chủ yếu cho MAC|Được sử dụng chủ yếu cho PC|
|Cho phép metadeta| Không cho phép metadeta|

## Cấu trúc tệp AIFF

**EA IFF 85** đặt ra một cấu trúc tổng thể để lưu trữ dữ liệu trong các tệp. Tệp **EA IFF 85** bao gồm một số khối dữ liệu. Một khối đang bắt nạt khối của tệp AIFF bao gồm một số thông tin tiêu đề theo sau là dữ liệu:
{{< figure src="../chunk.png" alt="Đoạn AIFF" >}}

Tệp AIFF là tập hợp của một số loại khối khác nhau. Có hai loại khối chung quan trọng để tạo thành một khối tệp AIFF:
- **Khối chung**: Chứa các tham số quan trọng mô tả âm thanh được lấy mẫu, chẳng hạn như độ dài và tốc độ lấy mẫu.
- **Khối dữ liệu âm thanh**: Chứa các mẫu âm thanh thực tế.
Có nhiều khối tùy chọn khác liệt kê các thông số của thiết bị, xác định điểm đánh dấu, lưu trữ thông tin ứng dụng cụ thể, v.v.

### Các loại chunk cục bộ

Các loại chunk để tạo thành AIFF được đưa ra trong bảng dưới đây:

|Loại đoạn| Mô tả|
---|---|
|Khối chung|Khối chung mô tả các thông số cơ bản của âm thanh được lấy mẫu|
|Khối dữ liệu âm thanh|Khối dữ liệu âm thanh chứa các khung mẫu thực tế|
|Đoạn đánh dấu|Đoạn đánh dấu chứa các điểm đánh dấu trỏ đến các vị trí trong dữ liệu âm thanh|
|Khối nhạc cụ|Khối nhạc cụ xác định các tham số cơ bản mà một nhạc cụ, chẳng hạn như bộ lấy mẫu, có thể sử dụng để phát lại dữ liệu âm thanh|
|Khối dữ liệu MIDI|Khối dữ liệu MIDI có thể được sử dụng để lưu trữ dữ liệu MIDI|
|Phân đoạn ghi âm thanh|Phân đoạn ghi âm thanh chứa thông tin liên quan đến thiết bị ghi âm thanh|
|Khối dành riêng cho ứng dụng|Khối dành riêng cho ứng dụng có thể được nhà sản xuất ứng dụng sử dụng cho bất kỳ mục đích nào|
|Phần bình luận|Phần bình luận được sử dụng để lưu trữ các bình luận trong MẪU AIFF|
|Đoạn văn bản - Tên, Tác giả, Bản quyền, Chú thích| Tất cả đều là đoạn văn bản|

## Người giới thiệu ##

* [Định dạng tệp trao đổi âm thanh - Theo Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

