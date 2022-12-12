{
  "date" : "2022-01-23",
  "keywords" :[ "tệp xz", "định dạng tệp", "tệp xz là gì", "tệp", "ví dụ xz", "phần mở rộng tệp xz","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp XZ - Lưu trữ nén XZ",
  "description":"Tìm hiểu về định dạng tệp XZ và API có thể tạo và mở tệp XZ.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Tệp XZ là gì?

XZ là định dạng tệp nén sử dụng thuật toán nén LZMA2. Nó được thiết kế để thay thế cho các định dạng gzip và bzip2 phổ biến, đồng thời cung cấp một số lợi thế so với các tiêu chuẩn cũ hơn này. Các tệp XZ được hỗ trợ tốt trên nhiều nền tảng và có thể được giải nén nhanh chóng và dễ dàng. Mặc dù chúng không phổ biến như các tệp [ZIP](/vi/compression/zip/) hoặc [RAR](/vi/compression/rar/), nhưng tệp lưu trữ XZ có thể được sử dụng để lưu trữ lượng lớn dữ liệu mà không làm giảm chất lượng nén. Nếu bạn cần nén hoặc giải nén các tệp lớn, thì phần mở rộng tệp XZ rất đáng để xem xét.

## Định dạng tệp XZ

Tệp XZ được tạo và lưu dưới dạng tệp nhị phân vào đĩa. Nó sử dụng thuật toán LZMA để nén dữ liệu và có thể đạt được tỷ lệ nén lên tới 50%. Các tệp XZ thường được sử dụng để phân phối phần mềm và lưu trữ sao lưu. Chúng có thể được giải nén bằng tiện ích XZ, được bao gồm trong hầu hết các bản phân phối Linux.

## Giải nén tập tin XZ trên Linux/Unix

Để giải nén các tệp XZ, trước tiên hãy cài đặt gói `xz-utils`:
```
$ sudo apt-get install xz-utils
```

Sử dụng lệnh `unxz` để giải nén các tệp .xz:
```
$ unxz compressed_xz_file.xz
```

hoặc sử dụng tùy chọn --decompress của XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Người giới thiệu

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)

