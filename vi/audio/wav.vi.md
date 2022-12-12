{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "tệp", "phần mở rộng", "định dạng", "định dạng tệp trao đổi âm thanh", "nhạc" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp WAV và API có thể tạo và mở tệp WAV.",
  "title" :"WAV - Định dạng tệp âm thanh dạng sóng",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Tệp WAV là gì?

WAV, được biết đến với tên WAVE (Định dạng tệp âm thanh dạng sóng), là một tập hợp con của đặc tả Định dạng tệp trao đổi tài nguyên (RIFF) của Microsoft để lưu trữ các tệp âm thanh kỹ thuật số. Định dạng này không áp dụng bất kỳ nén nào đối với dòng bit và lưu trữ các bản ghi âm với tốc độ lấy mẫu và tốc độ bit khác nhau. Nó đã và đang là một trong những định dạng tiêu chuẩn cho đĩa CD âm thanh. Các tệp wave có kích thước lớn hơn so với các định dạng tệp âm thanh mới, chẳng hạn như [MP3](/vi/audio/mp3/), định dạng này sử dụng tính năng nén mất dữ liệu để giảm kích thước tệp trong khi vẫn duy trì chất lượng âm thanh như nhau. Tuy nhiên, các tệp WAV có thể được nén bằng codec Trình quản lý nén âm thanh (ACM). Có sẵn một số API và ứng dụng có thể chuyển đổi tệp WAV sang các định dạng tệp âm thanh phổ biến khác.

**Bạn có biết không?**
Bạn có thể trở thành người đóng góp tại FileFormat.com để giữ cho cộng đồng định dạng tệp được cập nhật với những phát hiện của bạn. Nếu bạn phải chia sẻ bất kỳ điều gì về định dạng tệp WAV hoặc Âm thanh, bạn có thể đăng phát hiện của mình trong phần [Tin tức về định dạng tệp âm thanh](https://news.fileformat.com/t/audio) để mọi người luôn cập nhật.

## Định dạng tệp WAV ##

Định dạng tệp WAVE, là một tập hợp con của đặc tả RIFF của Microsoft, bắt đầu bằng tiêu đề tệp theo sau là một chuỗi các khối dữ liệu. Tệp WAVE có một đoạn "WAVE" duy nhất bao gồm hai đoạn phụ:

* đoạn "fmt" - chỉ định định dạng dữ liệu
* một đoạn "dữ liệu" - chứa dữ liệu mẫu thực tế

### Tiêu đề tệp WAV ###

Tiêu đề của tệp WAV (RIFF) dài 44 byte và có định dạng sau:


|Vị trí|Giá trị mẫu|Mô tả
---|---|---|
|1 - 4|"RIFF"|Đánh dấu tệp là tệp riff. Mỗi ký tự dài 1 byte.
|5 - 8|Kích thước tệp (số nguyên)|Kích thước của toàn bộ tệp - 8 byte, tính bằng byte (số nguyên 32 bit). Thông thường, bạn sẽ điền thông tin này sau khi tạo.
|9 -12|"WAVE"|Tiêu đề loại tệp. Đối với mục đích của chúng tôi, nó luôn bằng "WAVE".
|13-16|"fmt "|Định dạng đoạn đánh dấu. Bao gồm dấu null
|17-20|16|Độ dài của dữ liệu định dạng như được liệt kê ở trên
|21-22|1|Loại định dạng (1 là PCM) - 2 byte số nguyên
|23-24|2|Số kênh - Số nguyên 2 byte
|25-28|44100|Tốc độ mẫu - số nguyên 32 byte. Các giá trị phổ biến là 44100 (CD), 48000 (DAT). Tỷ lệ mẫu = Số lượng mẫu mỗi giây, hoặc Hertz.
|29-32|176400|(Tỷ lệ mẫu * BitsPerSample * Kênh) / 8.
|33-34|4|(BitsPerSample * Channels) / 8.1 - 8 bit mono2 - 8 bit stereo/16 bit mono4 - 16 bit stereo
|35-36|16|Số bit trên mỗi mẫu
|37-40|"dữ liệu"|"dữ liệu" tiêu đề chunk. Đánh dấu phần đầu của phần dữ liệu.
|41-44|Kích thước tệp (dữ liệu)|Kích thước của phần dữ liệu.
|Các giá trị mẫu được cung cấp ở trên cho nguồn âm thanh nổi 16 bit.

## Người giới thiệu ##

* [WAV - Theo Wikipedia](https://en.wikipedia.org/wiki/WAV)

