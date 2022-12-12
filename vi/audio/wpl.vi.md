{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "tệp wpl", "tiện ích mở rộng", "định dạng", "tệp wpl là gì", "nhạc", "định dạng tệp wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp WPL và API có thể tạo, chuyển đổi và mở tệp WPL.",
  "title" :"WPL - Tệp danh sách phát Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Tệp WPL là gì?

Một tệp có phần mở rộng .wpl chứa danh sách bài hát sẽ chạy trên Microsoft Windows Media Player. Những tệp này thường được tạo bởi người dùng cho bộ sưu tập video và âm thanh của họ. Nội dung được ghi trong tệp WPL, chỉ là các đường dẫn thư mục hoặc vị trí cho các tệp đa phương tiện do người tạo tệp .wpl chọn, vì vậy ứng dụng trình phát đa phương tiện có thể nhanh chóng tìm và phát nội dung đa phương tiện từ các vị trí thư mục của chúng.

## Định dạng tệp WPL

WPL (Windows Media Player Playlist) là định dạng tệp độc quyền được sử dụng trong Microsoft Windows Media Player phiên bản 9 trở lên. Nó là một định dạng tệp máy tính lưu trữ danh sách phát đa phương tiện. Theo mặc định, danh sách phát được lưu với phần mở rộng .wpl(Windows Media Player Playlist). Thay vào đó, bạn có thể sử dụng tiện ích mở rộng [.m3u](/vi/audio/m3u) nếu bạn muốn phát đĩa dữ liệu của mình trên một thiết bị không hỗ trợ tiện ích mở rộng này. Các thành phần của tệp WPL được thể hiện ở định dạng XML.

Phần tử cấp cao nhất "smil" chỉ định rằng các phần tử của tệp tuân theo cấu trúc Ngôn ngữ tích hợp đa phương tiện được đồng bộ hóa (SMIL). Tệp được tạo và lưu với phần mở rộng .wpl và kiểu MIME của nó là application/vnd.ms-wpl.

### Ví dụ WPL

Đây là một ví dụ về tệp wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Người giới thiệu ##

* [Lớp âm thanh MPEG-1 II - Theo Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

