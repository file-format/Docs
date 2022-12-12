{
  "date" : "2019-10-11",
  "keywords" :[ "tệp bz2", "định dạng tệp bz2", "tệp bz2 là gì", "tệp", "ví dụ bz2", "phần mở rộng tệp bz2","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Định dạng tệp nén",
  "description":"Tìm hiểu để biết tệp BZ2 là gì và các API có thể tạo và mở tệp BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Tệp BZ2 là gì?

BZ2 là các tệp nén được tạo bằng phương pháp nén mã nguồn mở [BZIP2](http://www.bzip.org/), chủ yếu trên hệ thống UNIX hoặc Linux. Nó được sử dụng để nén một tệp và không dùng để lưu trữ nhiều tệp. Điều này trái ngược với định dạng tệp TAR trên cùng một nền tảng lưu trữ nhiều tệp vào một tệp duy nhất nhưng không nén. Các tệp được nén dưới dạng BZ2 có thể được giải nén bằng các ứng dụng như [WinZip](https://www.winzip.com/win/en/). BZIP2 sử dụng thuật toán nén Run-Length Encoding (RLE) hoặc [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) để đạt được mức độ nén cao.

## Định dạng tệp BZ2

Không có thông số kỹ thuật chính thức có sẵn cho định dạng tệp này. Tuy nhiên, một [thông số kỹ thuật đảo ngược](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) không chính thức cho thấy rằng một luồng .bz2 bao gồm một tiêu đề 4 byte theo sau bằng 0 hoặc nhiều khối nén. Nó ngay lập tức được theo sau bởi một điểm đánh dấu cuối luồng chứa CRC 32 bit cho toàn bộ luồng văn bản thuần túy được xử lý. Không có khoảng đệm giữa các khối được nén và tất cả các khối đều được căn chỉnh theo bit.

## Giải nén/Trích xuất tệp BZ2

Bạn có thể giải nén tệp BZ2 trên Windows và Mac OS bằng phần mềm như WinZip. Trên linux, lệnh sau trong terminal.

```
bzip2 -d filename.bz2
```

## Người giới thiệu

* [Thông số định dạng BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

