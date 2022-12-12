{
  "date" : "2021-02-15",
  "keywords" :[ "tệp vp6", "định dạng tệp vp6", "tệp vp6 là gì", "tệp", "ví dụ vp6", "phần mở rộng tệp vp6","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - Tệp Video TrueMotion",
  "description":"Tìm hiểu về định dạng tệp VP6 và các API có thể tạo và mở tệp VP6.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Tệp VP6 là gì?

VP6 là định dạng video nén không mất dữ liệu được giới thiệu bởi công nghệ On2 vào tháng 5 năm 2003. Đây là một phần của loạt codec video do TrueMotion phát triển bao gồm V3, V4 và V5. Định dạng này đã được sử dụng trong thời gian ngắn trong lĩnh vực phát sóng chẳng hạn như với các báo cáo của BBC và phần mềm QuickLink. VP6 đã được VP7 Codec thành công vào tháng 1 năm 2005 với khả năng tương thích nén tốt hơn.

## Định dạng tệp VP6

Thông số kỹ thuật đầy đủ cho các tệp V6 không có sẵn công khai. On2 ban đầu công khai các thông số kỹ thuật nhưng ngay sau đó chúng không còn khả dụng cho người dùng phổ thông. Tài liệu không chính thức về định dạng tệp VP6 có sẵn tại [wiki đa phương tiện](https://wiki.multimedia.cx/index.php?title=On2_VP6) có thể được giới thiệu để nhà phát triển tham khảo.

### Macroblocks (MB)

Tương tự như MPEG-2, MPEG-4 phần 2 và 10, mỗi khung hình video của tệp VP6 bao gồm một mảng 16x16 macroblocks (MB). Mỗi MB có thể ở một trong các chế độ sau:

* Nội bộ MB
* Inter MB, null MV, khung tham chiếu trước đó
* Liên MB, MV vi sai, tham chiếu khung trước đó
* Inter MB, bốn MV, khung tham chiếu trước đó
* Inter MB, MV 1, khung tham chiếu trước đó
* Inter MB, MV 2, hệ quy chiếu trước đó
* Inter MB, MV null, tham chiếu khung được đánh dấu
* Liên MB, MV vi sai, tham chiếu khung được đánh dấu
* Liên MB, MV 1, tham chiếu khung được đánh dấu
* Liên MB, MV 2, tham chiếu khung được đánh dấu

### Tiêu đề khung

Tiêu đề khung của VP6 như được hiển thị bên dưới tuân theo việc đóng gói bit cuối lớn.

|Cú pháp|Số bit|Loại|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 biểu thị khung bên trong|
|qp |6 |Unsigned |Phạm vi hợp lệ của tham số lượng tử hóa 0..63|
|điểm đánh dấu| 1| Hằng| 0=VP61/62, 1=VP60|
|if (frame_mode == 0) { | 0 | |bằng INTRA_FRAME|
|phiên bản |5| Hằng| 6=VP60/61, 7=VP60(Điện tử nghệ thuật), 8=VP62|
|phiên bản2 |2| Hằng số |0=VP60, 3=VP61/62|
|xen kẽ |1| Boolean |true (1) có nghĩa là xen kẽ sẽ được sử dụng|
|if (điểm đánh dấu==1 hoặc phiên bản2==0) {||||
|offset |16 |Unsigned| bù đắp bộ đệm thứ cấp (byte liên quan đến đầu bộ đệm)|
|}||||
|dim_y |8| Chưa ký| Chiều cao macroblock của video |
|dim_x |8| Chưa ký| Chiều rộng macroblock của video|
|render_y |8 |Unsigned |Hiển thị chiều cao của video|
|render_x |8 |Unsigned |Chiều rộng hiển thị của video|
|}khác{||||
|if (điểm đánh dấu==1 hoặc phiên bản2==0) {||||
|offset |16 |Unsigned |Bù bộ đệm thứ cấp (byte liên quan đến đầu bộ đệm)|
|}||||
|}||||

## Người giới thiệu

* [Wikipedia VP6](https://vi.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

