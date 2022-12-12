{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp M4S - Tệp M4S là gì?",
  "description":"Tìm hiểu về định dạng tệp M4S và API có thể tạo và mở tệp M4S.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Tệp M4S là gì?

Tệp M4S là một đoạn nhỏ của video được phát trực tuyến qua internet bằng kỹ thuật phát trực tuyến **MPEG-DASH**. Nó chứa một đoạn video ở dạng dữ liệu nhị phân. Ứng dụng nhận (thường là trình duyệt web hoặc trình phát phương tiện) phát các phân đoạn này theo thứ tự chúng được nhận. Phân đoạn M4S đầu tiên được xác định bởi dữ liệu khởi tạo mà nó chứa. Trong **tóm tắt**, các tệp M4S là các phân đoạn phương tiện nhỏ riêng lẻ của một tệp hoàn chỉnh.

## Định dạng tệp M4S

Các tệp M4S dựa trên [định dạng tệp phương tiện cơ sở ISO (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Các phân đoạn nhỏ này của một tệp lớn có thể được tải xuống độc lập qua HTTP. Do đó, nếu bạn có một tệp phim [MP4](/vi/video/mp4/) lớn, tệp đó có thể được phát trực tuyến bằng kỹ thuật MPEG-DASH (Dynamic Adaptive Streaming over HTTP) bằng cách phân đoạn tệp thành các tệp phân đoạn M4S. Nếu tệp phim lớn này được tải xuống đĩa dưới dạng M4S, nhiều tệp M4S sẽ được tải xuống. Nếu tất cả các phân đoạn .m4s này được nối với nhau, thì một tệp hoàn chỉnh có thể phát được sẽ được tạo. Trình phát đa phương tiện không thể phát tệp trừ khi phân đoạn khởi tạo đầu tiên cũng có sẵn với tệp.

## Giới thiệu về truyền phát MPEG-DASH

MPEG-DASH sử dụng kỹ thuật truyền phát tốc độ bit thích ứng để có thể truyền phát nội dung đa phương tiện chất lượng cao qua internet. Điều này được thực hiện bằng cách chia nội dung thành một chuỗi các phân đoạn nhỏ được truyền trực tuyến qua HTTP. Các tệp phương tiện lớn như phim, podcast hoặc chương trình phát sóng trực tiếp sự kiện thể thao có thể được phát trực tuyến theo cách này. Các phân đoạn này được mã hóa ở các tốc độ bit khác nhau. Trình phát đa phương tiện hỗ trợ MPEG-DASH sẽ tự động chọn phân đoạn có tốc độ bit cao nhất bằng cách sử dụng thuật toán thích ứng tốc độ bit. Điều này tránh làm đình trệ hoặc tải lại các sự kiện trong quá trình phát lại.

### API mã nguồn mở cho tệp M4S

Có sẵn các API nguồn mở có thể được sử dụng để đọc và chuyển đổi các tệp M4S.

* [libdash](https://github.com/bitmovin/libdash) - .NET API cho tệp M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - Ứng dụng khách Javascript cho tệp M4S
* [Thư viện Go để tạo tệp Dash](https://github.com/zencoder/go-dash)

### API mã nguồn mở để chuyển đổi M4S sang MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Người giới thiệu ###

* [Định dạng tệp phương tiện cơ sở ISO (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Dynamic Adaptive Streaming qua HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

