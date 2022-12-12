{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp TS - Tệp luồng truyền tải video",
  "keywords" :[ "ts", "fly", "extension", "extension", ".ts", "format" ],
  "description":"Tìm hiểu về tệp TS là gì và các API có thể tạo và mở tệp TS.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Tệp TS là gì?

Tệp có phần mở rộng .ts là luồng video lưu trữ dữ liệu trên đĩa DVD. Nó sử dụng thuật toán nén MPEG-2 ([.mpeg](/vi/video/mpg/)) để đạt được hiệu quả tối đa và khả năng tương thích trên các loại phương tiện khác nhau như phát trực tuyến và phát sóng internet. Định dạng tệp TS được tạo để có thể phát trên các thiết bị có kết nối internet kém, chẳng hạn như TV thông minh.

## Định dạng tệp TS - Thông tin khác

Dữ liệu trong tệp TS tương tự như tệp [MP4](/vi/video/mp4/), nhưng được chia thành nhiều phần nhỏ. Mỗi đoạn bao gồm một đoạn video nhỏ, theo sau là một đoạn âm thanh và chú thích tùy chọn. Một tệp TS duy nhất bao gồm nhiều khối như vậy. Ngoài video, âm thanh và chú thích, mỗi đoạn cũng bao gồm một số dữ liệu bổ sung để phát hiện lỗi trong đoạn. Do đó, các tệp TS có kích thước lớn hơn một chút.

### Tại sao nên sử dụng Định dạng tệp TS?

Vì vậy, nếu các tệp TS có kích thước hơi lớn, thì nó mang lại lợi thế gì khi sử dụng chúng thay vì các định dạng tệp khác? Chà, trong phát sóng, các đoạn video và âm thanh nhỏ có thể được gửi qua phương tiện liên lạc (có dây hoặc radio) trong thời gian thực. Dữ liệu bổ sung trong các khối được người nhận sử dụng để bỏ qua các khối dễ bị lỗi.

Ngoài ra, các tệp TS được sử dụng vì hệ thống phát sóng không cần toàn bộ luồng để phát. Việc truyền tải có thể được chọn và có thể được sử dụng trong thời gian thực bằng cách lắp ráp âm thanh và video.

## Làm cách nào để phát tệp TS?

Chà, các tệp TS có thể được mở và phát trong [Trình phát đa phương tiện VideoLAN VLC](https://www.videolan.org/vlc/features.html) phổ biến, có sẵn miễn phí để tải xuống.

## Người giới thiệu ##

* [Luồng truyền tải MPEG - Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

