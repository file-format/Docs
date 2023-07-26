{
  "date" : "2019-10-11",
  "keywords" :[ "tệp tbz", "định dạng tệp tbz", "tệp tbz là gì", "tệp", "ví dụ tbz", "phần mở rộng tệp tbz","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Lưu trữ tar nén Bzip",
  "description":"Tìm hiểu về định dạng tệp TBZ và các API có thể tạo và mở tệp TBZ.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Tệp TBZ là gì?

Tệp có phần mở rộng .tbz là tệp lưu trữ nén sử dụng nén BZIP để giảm kích thước của tệp nội dung. Các tệp TBZ thực sự là các tệp lưu trữ UNIX [TAR](/vi/compression/tar/) sau đó được nén bằng BZIP. Nén cấp hai gần đây nhất là [BZIP2](/vi/compression/bz2/) đã thay thế BZIP. Định dạng tệp TBZ phù hợp để truyền các tệp lớn. Các tệp TBZ có thể được mở/giải nén bằng các ứng dụng phần mềm như 7-Zip, PeaZip và jZip. Người dùng Linux và macOS cũng có thể mở TBZ bằng lệnh BZIP2 từ cửa sổ đầu cuối.

## Định dạng tệp TBZ

Các tệp TBZ thực sự là các tệp lưu trữ nén được tạo bằng nén BZIP/[BZIP2](/vi/compression/bz2/). Không có thông số kỹ thuật chính thức có sẵn cho định dạng tệp này. Tuy nhiên, một [thông số kỹ thuật đảo ngược](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) không chính thức cho thấy rằng một luồng .bz2 bao gồm một tiêu đề 4 byte theo sau bằng 0 hoặc nhiều khối nén.

## Người giới thiệu ##

* [Thông số định dạng BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

