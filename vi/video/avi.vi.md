{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Video âm thanh nén", "Tệp", "Phần mở rộng", "Định dạng tệp", "Bộ chứa đa phương tiện", "XVid", "DivX", "Codec", "Định dạng tệp trao đổi tài nguyên", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp AVI - Tệp xen kẽ video âm thanh",
  "description":"Tìm hiểu về định dạng tệp AVI và API có thể tạo và mở tệp AVI.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Tập tin AVI là gì? ##

Định dạng tệp **AVI** là định dạng tệp chứa đa phương tiện Audio Video được giới thiệu bởi Microsoft. Nó chứa dữ liệu âm thanh và video được tạo và nén bằng cách sử dụng một số codec (Bộ giải mã/Bộ giải mã) chẳng hạn như **XVid** và **DivX**. Vì các codec khác nhau có thể được sử dụng để mã hóa nội dung AVI, nên các ứng dụng đang truy xuất, tức là trình phát AVI, chỉ có thể mở các ứng dụng này nếu chúng đã cài đặt các codec cần thiết để tạo nội dung AVI. Định dạng này được hỗ trợ theo mặc định trên tất cả các nền tảng **Microsoft Windows** cũng như trên hầu hết các nền tảng chính khác. Một số ứng dụng và API cung cấp khả năng tạo/lưu, đọc và chuyển đổi AVI sang các định dạng phổ biến khác như MP4, MOV, WMV, v.v.

## Định dạng tệp AVI ##

Tệp có phần mở rộng .avi là tệp AVI. Đó là định dạng phụ của Định dạng tệp trao đổi tài nguyên (RIFF). RIFF tổ chức dữ liệu thành các khối hoặc "khối" được xác định bằng thẻ FourCC. Tệp AVI chỉ đơn giản là một "khối" trong tệp có định dạng RIFF.

Trong đoạn con đầu tiên, tiêu đề của tệp được xác định bằng thẻ "hdrl"; nội dung của nó bao gồm chiều rộng, chiều cao và tốc độ khung hình của video. Trong đoạn phụ thứ hai, thẻ chuyển động biểu thị tốc độ khung hình của video. Video AVI bao gồm dữ liệu âm thanh/hình ảnh thực tế trong đoạn này. Ngoài ra còn có một phần con tùy chọn thứ ba với thẻ "idx1", cho biết vị trí trong tệp của các khối dữ liệu riêng lẻ thuộc về tệp.

### Hạn chế ###

* Thông tin tỷ lệ khung hình không thể được mã hóa trong đặc tả AVI ban đầu, mặc dù đặc tả OpenDML sau này (AVI 2.0) cung cấp một phương pháp chuẩn hóa
* Mặc dù các tệp AVI được sử dụng rộng rãi trong quá trình hậu sản xuất phim và truyền hình, nhiều cách tiếp cận khác nhau để thêm mã thời gian vào chúng đang cạnh tranh nhau, ảnh hưởng đến khả năng sử dụng của định dạng.
* Tệp video được mã hóa bằng AVI không thể sử dụng kỹ thuật nén yêu cầu dữ liệu khung trong tương lai ngoài khung được mã hóa (khung B)
* Có vấn đề khi sử dụng các tệp AVI có tốc độ bit thay đổi (VBR) (chẳng hạn như âm thanh MP3 ở tốc độ mẫu dưới 32 kHz)
* Phim truyện độ nét tiêu chuẩn mã hóa tệp AVI như thường được sử dụng có khả năng phát sinh chi phí khoảng 5 MB mỗi giờ, tùy thuộc vào cách sử dụng tệp
* Phụ đề phải được mã hóa cứng vào luồng video hoặc được phân phối trong một tệp riêng trong trường hợp tệp AVI không thể chứa các tệp đính kèm như phông chữ và phụ đề

## Lược Sử ##

AVI được Microsoft giới thiệu vào năm 1992 với mục đích cung cấp định dạng tệp âm thanh và video mạnh mẽ và tiên tiến hơn. Định dạng này nhanh chóng trở nên phổ biến với việc sử dụng internet, cho phép các cá nhân chia sẻ tệp video trực tiếp và gián tiếp thông qua bộ lưu trữ phương tiện dựa trên đám mây.

## Người giới thiệu ##

* [AVI - Theo Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

