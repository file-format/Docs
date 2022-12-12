{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "file", "extension", "format", "Audio Coding", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp AAC và API có thể tạo và mở tệp AAC.",
  "title" :"AAC - Tệp mã hóa âm thanh nâng cao",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## Tệp AAC là gì?

AAC (Mã hóa âm thanh nâng cao) đề cập đến tiêu chuẩn mã hóa âm thanh kỹ thuật số đại diện cho các tệp âm thanh dựa trên nén âm thanh bị mất. Nó được ra mắt với tư cách là người kế nhiệm định dạng tệp **[MP3](/vi/audio/mp3/)** lưu ý rằng các vấn đề bên phải đối mặt với việc triển khai các ý tưởng mới trong quy trình mã hóa dựa trên sự phát triển của các phương pháp nén dữ liệu. AAC đạt được chất lượng âm thanh tốt hơn so với MP3 ở cùng tốc độ bit. Nó được định nghĩa trong MPEG-2 Phần 7 (ISO/IEC 13818-7) và ở dạng cập nhật trong MPEG-4 Phần 3 (ISO/IEC 14496-3).

Định dạng AAC đã được YouTube, iPhone, iPod, iPad, Apple iTunes và một số nền tảng khác sử dụng làm định dạng phương tiện mặc định. Một số ứng dụng và API có sẵn để chuyển đổi định dạng tệp AAC sang các định dạng khác như MP3, WMA, M4A, **[WAV](/vi/audio/wav/)** và các định dạng khác.

### Lịch sử tóm tắt của tệp AAC

Định dạng tệp AAC là phiên bản nâng cao của MP3 với một số cải tiến. Được đóng góp bởi một số công ty bao gồm Viện Fraunhofer (Fraunhofer IIS - nhà phát triển MP3), Nokia, Dolby, AT&T và Sony, định dạng này được Nhóm chuyên gia hình ảnh chuyển động (MPEG) tuyên bố là tiêu chuẩn quốc tế vào tháng 4 năm 1997. Sau đó vào năm 1999, MPEG-2 Phần 7 đã được cập nhật và đưa vào họ tiêu chuẩn MPEG-4. Nó được gọi là MPEG-4 Part 3, được xác định là ISO/IEC 14496-3: 1999 hoặc MPEG-4 Audio.

## Thông số kỹ thuật định dạng tệp AAC

Các thông số định dạng tệp AAC cho phép thiết kế codec linh hoạt hơn MP3, dẫn đến nhiều chiến lược mã hóa đồng thời hơn và nén hiệu quả hơn. Định dạng này đã được một số nền tảng phần cứng lựa chọn vì những cải tiến của nó so với MP3 về mặt cung cấp hỗ trợ cho nhiều tùy chọn hơn ngay cả ở tốc độ bit thấp hơn. Thông số kỹ thuật định dạng tệp AAC có sẵn ở [MPEG-2 Phần 7](https://www.iso.org/standard/43345.html) và [MPEG-4 Phần 3](https://www.iso.org /standard/53943.html) (tải xuống không miễn phí). Định dạng sử dụng các loại phương tiện sau:

* âm thanh/aac
* âm thanh/aacp
* âm thanh/3gpp
* âm thanh/3gpp2
* âm thanh/mp4
* âm thanh/mp4a-latm
* âm thanh/mpeg4-chung

## AAC so với MP3 - Cải tiến ##

Sự khác biệt chính giữa AAC và MP3 về các cải tiến như sau:

* AAC hỗ trợ phạm vi kênh rộng hơn (tối đa 48) và tốc độ lấy mẫu (từ 8 kHz đến 96 kHz)
* AAC có tần số mã hóa tốt hơn trên 16 kHz
* AAC có giới hạn biến thiên rộng hơn trong độ phân giải thời gian-tần số của một dãy bộ lọc dẫn đến việc mã hóa các phần chuyển tiếp và phần cố định của tín hiệu âm thanh được cải thiện
* Ngân hàng bộ lọc đơn giản và hiệu quả hơn: ngân hàng bộ lọc lai đã được thay thế bằng MDCT tiêu chuẩn (biến đổi cosine rời rạc đã sửa đổi)
* Hỗ trợ nâng cao hiệu quả nén bằng cách sử dụng Định hình tiếng ồn tạm thời (TNS), hệ số dự đoán thời gian MDCT (dự đoán dài hạn), âm thanh nổi tham số, thay thế tiếng ồn cảm nhận, sao chép dải quang phổ (SBR).
* âm thanh nổi chung linh hoạt hơn (các phương pháp khác nhau có thể được sử dụng trong các dải tần số khác nhau);

## Người giới thiệu ##

* [AAC - Theo Wikipedia](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

