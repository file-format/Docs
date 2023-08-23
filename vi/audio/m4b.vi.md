{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "tệp", "phần mở rộng", "định dạng", "định dạng tệp m4b là gì", "nhạc", "định dạng tệp m4b", "M4b so với MP3", "đặc tả định dạng tệp m4b "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp M4B và các API có thể tạo, chuyển đổi và mở tệp M4B.",
  "title" :"M4B - Định dạng tệp sách nói MPEG-4",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Tệp M4B là gì?

Tệp có phần mở rộng .m4b là sách nói thường được sử dụng bởi sách Apple và iTunes. Âm thanh được sử dụng ở định dạng này được lưu trữ ở định dạng MPEG-4 và được nén bằng mã hóa AAC. Tệp M4B rất giống với M4A nhưng có hỗ trợ các tính năng liên quan đến sách nói, chẳng hạn như đánh dấu trang và ngắt chương. Các tệp M4B có sẵn ở cả phiên bản hỗ trợ DRM và phiên bản không có DRM. Sách nói mã hóa DRM thường là sách nói trả phí từ iTunes Store. Trong khi đó, DRM miễn phí có thể được tìm thấy dễ dàng qua internet.

## Định dạng tệp M4B

Các tệp sách nói chứa siêu dữ liệu, hình ảnh, dấu trang và siêu liên kết có thể được lưu bằng phần mở rộng .m4a nhưng nhìn chung, phần mở rộng .m4b được sử dụng trong khi lưu, chỉ để xác định rằng tệp có định dạng tệp sách nói. Fairplay DRM (Quản lý quyền kỹ thuật số) được áp dụng để bảo vệ các tệp M4B của họ. Vì vậy, các tệp được tải xuống từ iTunes chỉ có thể được phát trên các thiết bị hoặc máy tính được ủy quyền.


## M4B so với M4A

Cả M4B và [MP3](/audio/mp3/) đều là định dạng tệp chỉ có âm thanh.

**M4B**: Thắng khi so sánh với MP3 về chất lượng nếu mã hóa cả hai ở cùng tốc độ bit. M4B là một tệp sách nói được nén bằng mã hóa AAC. Về cơ bản, nó được liên kết với “Lớp âm thanh MPEG-4”, các tệp có phần mở rộng .m4b là lớp âm thanh của phim MPEG-4 nhưng có thêm các tính năng liên quan đến sách nói. Mục tiêu của nó là vượt qua MP3 và trở thành tiêu chuẩn mới trong nén âm thanh. Nó rất gần với MP3 theo nhiều cách nhưng được phát triển để có chất lượng tốt hơn với cùng kích thước tệp hoặc thậm chí nhỏ hơn. Định dạng M4B lần đầu tiên được giới thiệu bởi Apple. Loại định dạng cũng được nhận ra là Bộ mã hóa không mất dữ liệu của Apple (ALE).

Do đó, hiện tại M4B không thể đạt được thành công chủ đạo của MP3 vì định dạng âm thanh này vẫn chưa thể phát được phổ biến.

**Mp3**: Một định dạng âm thanh kỹ thuật số rất quen thuộc với mọi người. Định dạng nén đầu tiên xuất hiện và trở nên rất nổi tiếng đối với những người nghe nhạc. Thành công chính của nó nhanh đến mức loại tệp này có thể được phát phổ biến và tương thích với hầu hết mọi thứ, phần cứng hoặc phần mềm. Nhìn chung, M4A sẽ tạo ra chất lượng âm thanh tốt hơn, nhưng nhiều người sẽ tranh luận rằng, dù đúng hay sai thì sự khác biệt về âm thanh cũng không thể so sánh được và sẽ rất lãng phí thời gian khi cố gắng chuyển đổi tệp MP3 thành tệp M4A. Cuối cùng, việc chuyển đổi sẽ chỉ khiến bạn mất đi chất lượng âm thanh ban đầu.

## Thông số định dạng tệp M4B

Tương tự như [M4A](/vi/audio/m4a/), các tệp M4B cũng bao gồm các đoạn liên tiếp. Mỗi đoạn có tiêu đề 8 byte và được chia thành:
- Kích thước chunk 4 byte (big-endian, byte cao trước)
- Loại khối 4 byte - một trong các chữ ký được xác định trước: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "skip", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT ", "scpt", "ssrc".

Tương tự như M4A, đoạn đầu tiên trong M4B sẽ thuộc loại "ftype" và có loại phụ ở độ lệch 8. M4B được xác định bởi loại phụ phải là "M4B_".

Lặp lại các đoạn, cho đến khi phát hiện thấy đoạn không xác định, Nó sẽ soạn tệp M4B (âm thanh MPEG-4).

## Người giới thiệu

* [MPEG-4 Phần 14 - Theo Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Ví dụ khôi phục và định dạng âm thanh MPEG-4 Phần 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

