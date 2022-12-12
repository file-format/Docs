{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "file", "extension", "format", "MPEG-4", "Digital Rights Management", "DRM", "Apple", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Tìm hiểu về định dạng tệp M4V và các API có thể tạo và mở tệp M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Tệp M4V là gì?

Định dạng tệp **M4V**, do Apple phát triển, là vùng chứa video được bảo vệ tùy chọn bằng tính năng bảo vệ bản sao Quản lý quyền kỹ thuật số (DRM) để bảo vệ quyền riêng tư hoặc bản sao. Các video và bản âm thanh được bao quanh bởi các tệp chứa để lập chỉ mục và sắp xếp các luồng phát lại. Ngoài ra, các thùng chứa cũng cung cấp tính năng của các chương tương tự như trên DVD. Apple sử dụng M4V để mã hóa video trong iTunes Store của mình. Nó bảo vệ việc sao chép trái phép thông qua bảo vệ bản sao FairPlay của Apple bằng cách cho phép các tệp M4V chỉ được phát trên các máy tính được ủy quyền có tài khoản được sử dụng để mua video. Tuy nhiên, nếu tính năng bảo vệ DRM bị xóa khỏi các tệp M4V, các tệp này có thể được phát trong các trình phát video khác bằng cách thay đổi phần mở rộng từ .m4v thành .mp4, đó là lý do tại sao các tệp M4V được liên kết với MPEG-4. M4V sử dụng H.264 cho video và **[AAC](/vi/audio/aac/)** và Dolby Digital để mã hóa và giải mã âm thanh.

## Cấu trúc tệp M4V ##

Các tệp M4V có các đoạn liên tục với tiêu đề 8 byte, kích thước đoạn 4 byte và loại đoạn 4 byte trong mỗi đoạn. Đoạn đầu tiên là “ftype” và có một loại phụ ở độ lệch 8. M4V được xác định bởi loại phụ phải là "M4V_". Loại khối khác là chữ ký được xác định trước: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " HÌNH". Lặp lại các đoạn, cho đến khi phát hiện loại không xác định, chúng tôi soạn tệp M4V.

Dưới đây là kiểm tra mẫu: Dữ liệu nhị phân của tệp m4v mẫu được kiểm tra thông qua Trình xem Hex và có thể quan sát thấy rằng nó bắt đầu bằng chữ ký **ftyp** (hex: 66 74 79 70) ở offset 4, định nghĩa QuickTime Loại tệp vùng chứa. Loại phụ của tệp là **M4V_** (hex: 4D 34 56 20) trỏ đến loại tệp M4V (MPEG-4). Kích thước khối đầu tiên là 32 (hex: 00 00 00 20, big-endian, byte cao đầu tiên), kích thước nằm ở offset 0. Tại offset 32 (hex: 20) là chunk thứ hai, có kích thước 30.322 (hex : 00 00 76 72, big-endian, byte thấp hơn trước) và nhập **moov** (hex: 6D 6F 6F 76). Đoạn tiếp theo nằm ở offset 32+30,322#30,354 (hex: 00 00 76 92) và có kích thước 8 (hex: 00 00 00 08) và gõ **free** (hex: 66 72 65 65).
### Codec được sử dụng trong M4V ###

#### Bộ giải mã video H.264 ####

H.264 là một tiêu chuẩn nén video giúp chuyển đổi video kỹ thuật số thành định dạng cần ít dung lượng hơn khi cần truyền hoặc lưu trữ. M4V sử dụng H.264 để nén video. Ứng dụng của nó bao gồm DVD, TV, Hội nghị truyền hình và truyền phát video qua internet. H.264 bao gồm hai phần chính: Bộ mã hóa – Bộ nén video, Bộ giải mã – Giải nén video đã nén trở lại. Trong hình bên dưới, các quy trình mã hóa và giải mã được đánh dấu và các quy trình khác được đề cập trong tiêu chuẩn H.264.

##### Quá trình mã hóa và giải mã video trong H.264 #####

Đối với dòng bit H.264 được nén, bộ mã hóa video tiến hành quá trình dự đoán, chuyển đổi và mã hóa. Đồng thời, bộ giải mã thực hiện quá trình giải mã ngược, biến đổi ngược và tái cấu trúc để tạo lại tệp video. H.264 chiếm một nửa kích thước của MPEG.

#### Audio codec ####

Mã hóa âm thanh nâng cao (AAC) là một bộ giải mã âm thanh để nén âm thanh kỹ thuật số bị mất dữ liệu và được sử dụng trong bộ chứa M4V. AAC là phiên bản kế thừa của định dạng [MP3](/vi/audio/mp3/) và đạt được chất lượng tốt hơn MP3 với cùng tốc độ bit. Định dạng AAC loại bỏ một số thông tin trong quá trình nén, điều này ít quan trọng hơn. AAC là một codec dựa trên khối có tốc độ bit thay đổi (VBR), trong đó mỗi khối giải mã thành 1024 mẫu trong miền thời gian.

### Người giới thiệu ###

* [Wikipedia - M4V](https://vi.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://vi.wikipedia.org/wiki/H.264/MPEG-4_AVC)

