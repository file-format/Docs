{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "file", "extension", "format", "tệp cue là gì", "nhạc", "định dạng tệp cue", "đặc tả định dạng tệp cue", "bảng cue", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp CUE và các API có thể tạo, chuyển đổi và mở tệp CUE.",
  "title" :"CUE - Tệp trang tính Cue",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Tệp CUE là gì?

Tệp có phần mở rộng .cue, còn được gọi là tệp bảng gợi ý, là tệp siêu dữ liệu chứa thông tin về bố cục của các bản nhạc trên đĩa CD hoặc DVD. Chúng được hỗ trợ bởi các trình phát đa phương tiện và các ứng dụng tạo đĩa quang. Dữ liệu âm thanh chính được lưu trữ trên đĩa CD được tham chiếu bởi tệp cue, cùng với các thông số kỹ thuật về độ dài bản nhạc, tiêu đề đĩa và người biểu diễn. Do đó, nếu một tệp âm thanh chứa nhiều bản nhạc, thì tệp cue có thể được sử dụng để chia âm thanh thành nhiều tệp hoặc tham chiếu các bản nhạc khác nhau.

## Định dạng tệp CUE

Các tệp CUE hoặc bảng gợi ý được lưu trữ ở định dạng văn bản thuần túy mà con người có thể đọc được. Thông tin trong tệp cue là các lệnh có một hoặc nhiều tham số. Các lệnh này áp dụng cho toàn bộ tệp hoặc cho một rãnh riêng lẻ, tùy thuộc vào lệnh cụ thể và ngữ cảnh. Hướng dẫn sử dụng CDRWIN mô tả các thông số kỹ thuật cho cú pháp và ngữ nghĩa của bảng gợi ý.

## Bảng CUE Các lệnh cơ bản

|Lệnh|Mô tả|
---|---|
|TỆP| Đề cập đến tệp chứa dữ liệu và định dạng của nó, chẳng hạn như [MP3](/vi/audio/mp3/), [WAV](/vi/audio/wav/), hoặc hình ảnh đĩa nhị phân đơn giản)|
|THEO DÕI| Xác định thông tin ngữ cảnh của rãnh như số và loại hoặc chế độ của rãnh.|
|INDEX| Thể hiện vị trí dưới dạng chỉ mục trong TẬP TIN. Định dạng là mm:ss:ff (khung phút-giây).|
|PREGAP và POSTGAP|Điều này cho biết khoảng cách trước hoặc sau khoảng cách của một bản nhạc, không được lưu trữ trong bất kỳ tệp dữ liệu nào. Độ dài được chỉ định ở cùng định dạng khung phút-giây như đối với INDEX.|

### Ví dụ về Trang tính CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Người giới thiệu

* [tệp .cda - Theo Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

