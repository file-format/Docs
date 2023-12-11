{
"date" :  "2023-10-18",
   "keywords":[
"gợi ý",
"tập tin gợi ý",
"tập tin bảng gợi ý Cue cdrwin",
"cách mở tập tin gợi ý",
"tài liệu",
"phần mở rộng tập tin tín hiệu",
"sự mở rộng",
"tài liệu"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"Định dạng tệp CUE - Bảng gợi ý CDRWIN",
   "description":"Tìm hiểu về định dạng tệp CUE CDRWIN Cue Sheet và các API có thể tạo và mở tệp CUE.",
   "linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
         "parent":"disc-and-media"
}
},
"lastmod":"2023-10-18"
}

## Tập tin CUE là gì?

Tệp **.CUE**, còn được gọi là **CDRWIN Cue Sheet**, là tệp văn bản thuần túy chứa thông tin về các bản nhạc và bố cục của đĩa CD âm thanh hoặc hình ảnh đĩa, thường ở định dạng BIN hoặc ISO. Các tệp này thường được sử dụng để mô tả cấu trúc và nội dung của đĩa, cho phép phần mềm ghi đĩa CD hoặc phần mềm ổ đĩa ảo tái tạo chính xác đĩa gốc.

## Ví dụ về tệp CUE

Đây là một ví dụ về tệp ".cue" có thể trông như thế nào:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## Bảng Cue CDRWIN

Bảng Cue CDRWIN là biến thể cụ thể của định dạng tệp ".cue" được phần mềm CDRWIN sử dụng. CDRWIN là phần mềm ghi và tạo CD/DVD và các trang ".cue" của nó được thiết kế để sử dụng với phần mềm này. Các trang ".cue" này chứa thông tin cần thiết để CDRWIN tạo hoặc ghi CD hoặc DVD một cách chính xác.

Dưới đây là một số chi tiết chính cụ thể cho Bảng Cue CDRWIN:

1. **Duy nhất cho CDRWIN**: Các trang ".cue" của CDRWIN là định dạng độc quyền dành riêng cho phần mềm CDRWIN. Mặc dù chúng có những điểm tương đồng với các tệp ".cue" tiêu chuẩn nhưng chúng được điều chỉnh để hoạt động với các tính năng và cài đặt của CDRWIN.
    






2. **Giao diện thân thiện với người dùng**: CDRWIN cung cấp giao diện dễ sử dụng để tạo và chỉnh sửa trang ".cue" của nó. Người dùng có thể thêm hoặc sửa đổi thông tin về bản nhạc, chỉ mục, khoảng trống và các thông số khác theo cách thân thiện với người dùng.
    






3. **Các loại đĩa tương thích**: Bảng Cue CDRWIN được sử dụng chủ yếu để tạo nhiều loại CD và DVD khác nhau, bao gồm đĩa dữ liệu, CD âm thanh, đĩa chế độ hỗn hợp, v.v. Định dạng này cho phép người dùng chỉ định loại và nội dung của đĩa mà họ muốn tạo.
    






4. **Kiểm soát bố cục đĩa**: Bảng Cue CDRWIN cung cấp khả năng kiểm soát chi tiết về bố cục và cấu trúc của đĩa, bao gồm thứ tự bản nhạc, cài đặt tạm dừng/khoảng trống và bất kỳ tùy chọn cụ thể nào khác mà người dùng có thể có.
    






5. **Hỗ trợ ISO và BIN**: CDRWIN có thể hoạt động với cả định dạng ảnh đĩa ISO và BIN. Bảng ".cue" chỉ định tệp hình ảnh nào được sử dụng cho đĩa, đảm bảo đồng bộ hóa thích hợp giữa tín hiệu và hình ảnh.
    






6. **Ghi và trích xuất**: Những tờ ".cue" này rất quan trọng khi ghi đĩa hoặc trích xuất các bản nhạc từ đĩa bằng CDRWIN. Chúng giúp đảm bảo rằng sản phẩm cuối cùng phù hợp với bố cục và nội dung dự kiến.
    






7. **Sao lưu và khôi phục**: Người dùng CDRWIN thường tạo các trang ".cue" khi tạo bản sao lưu đĩa CD hoặc DVD của họ. Những trang này sau này có thể được sử dụng để khôi phục nội dung của đĩa, bao gồm cả bố cục và thời gian của bản nhạc.

## Làm cách nào để mở tập tin CUE?

Bảng Cue CDRWIN được thiết kế đặc biệt cho phần mềm CDRWIN, vì vậy chúng thường được mở và sử dụng trong CDRWIN.

Các chương trình mở hoặc tham chiếu tệp CUE

- CDRWIN
- Dự án thông minh IsoBuster
- Hệ thống EZB UltraISO

## Các tập tin CUE khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.cue**.

**Đĩa và Phương tiện**
- [CUE - Tệp bảng Cue](/vi/disc-and-media/cue/)
- [CUE - Bảng Cue CDRWIN](/vi/disc-and-media/cue-cdrwin/)

## Người giới thiệu
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

