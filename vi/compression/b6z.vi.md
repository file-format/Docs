{
  "date" : "2019-10-11",
  "keywords" :[ "tệp b6z", "định dạng tệp b6z", "tệp b6z là gì", "tệp", "ví dụ b6z", "phần mở rộng tệp b6z","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - Định dạng tệp lưu trữ B6ZIP",
  "description":"Tìm hiểu về định dạng tệp B6Z và API có thể tạo và mở tệp B6Z.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Tệp B6Z là gì?

Tệp có phần mở rộng .b6z là tệp lưu trữ nén được tạo ứng dụng phần mềm macOS [B6Zip](http://b6zip.com) được sử dụng để nén và giải nén tệp. Đây là định dạng lưu trữ tương đối mới cho phép tỷ lệ nén cao hơn. B6Z có kiến trúc mở và hỗ trợ kích thước tệp lên tới 900000 PB. Nó hỗ trợ nén dữ liệu, khôi phục lỗi và mở rộng tệp. Phần mềm tiện ích B6Zip có sẵn miễn phí trên MacOS để mở các loại tệp nén khác nhau bao gồm cả B6Z.

## Định dạng tệp B6Z

Định dạng tệp B6Z dựa trên kiến trúc mở và cung cấp khả năng nén ổn định với thuật toán mã hóa AES-256. Nó sử dụng LZMA2 làm phương pháp nén mặc định, nhưng cũng hỗ trợ các phương pháp nén khác như sau.

|Phương pháp|Mô tả|
---|---|
|LZMA |Phiên bản tối ưu của thuật toán LZ77|
|LZMA2| Phiên bản cải tiến của LZMA|
|Xả hơi| Thuật toán LZ77 thông thường|
|BZip2| Thuật toán BWT tiêu chuẩn|
|PPMD| PPMdH của Dmitry Shkarin|

Tiện ích B6Zip hỗ trợ tất cả các tiêu chuẩn nén này và được tối ưu hóa cao dẫn đến tốc độ cao. Nó hỗ trợ làm việc với các định dạng tệp [ZIP](/vi/compression/zip/), [TAR](/vi/compression/tar/) và [RAR](/vi/compression/rar/). Các tệp B6Z có loại MIME application/x-b6z-compressed.

## Người giới thiệu

* [B6Zip](http://b6zip.com)

