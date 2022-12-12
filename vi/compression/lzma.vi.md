{
  "date" : "2021-04-08",
  "keywords" :[ "tệp lzma", "định dạng tệp lzma", "tệp lzma là gì", "tệp", "ví dụ lzma", "phần mở rộng tệp lzma","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - Định dạng tệp nén LZMA",
  "description":"Tệp LZMA là gì và các API có thể tạo và mở tệp LZMA.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Tệp LZMA là gì?

Tệp có phần mở rộng .lzma là tệp lưu trữ nén được tạo bằng phương pháp nén LZMA (Thuật toán chuỗi Lempel-Ziv-Markov). Chúng chủ yếu được tìm thấy/sử dụng trên hệ điều hành Unix và tương tự như các thuật toán nén khác như [ZIP](/vi/compression/zip/) để giảm thiểu kích thước tệp. LZMA là định dạng tệp kế thừa, đang hoặc đã được thay thế bằng định dạng .xz. Loại MIME của định dạng .lzma là \`application/x-lzma'. Định dạng tệp này được thiết kế bởi Igor Pavlov để sử dụng trong LZMA SDK.

## Định dạng tệp LZMA

Tệp LZMA bao gồm hai phần chính:

1. Tiêu đề
1. Dữ liệu nén


### Tiêu đề LZMA

Các tệp LZMA có tiêu đề 13 byte theo sau là dữ liệu nén LZMA. Tiêu đề LZMA bao gồm:

* Đặc tính
* Kích cỡ từ điển
* Kích thước không nén

#### Thuộc tính tiêu đề LZMA

Trường Thuộc tính chứa ba thuộc tính. Một chữ viết tắt được đưa ra trong ngoặc đơn, theo sau là phạm vi giá trị của thuộc tính. trường bao gồm

1) số bit ngữ cảnh bằng chữ (lc, [0, 8]);
2) số bit vị trí chữ (lp, [0, 4]); và
3) số bit vị trí (pb, [0, 4]).

#### Kích thước từ điển LZMA

Điều này được lưu trữ dưới dạng một số nguyên cuối nhỏ 32 bit không dấu với các giá trị nằm trong khoảng từ 2^n và 2^n + 2^(n-1). LZMA Utils có thể giải nén các tệp với bất kỳ kích thước từ điển nào.

#### Kích thước không nén
Kích thước không nén được lưu trữ dưới dạng số nguyên cuối nhỏ 64 bit không dấu. Giá trị đặc biệt của 0xFFFF_FFFF_FFFF_FFFF cho biết rằng Kích thước không nén không xác định. Giá trị được biểu thị bằng Điểm đánh dấu kết thúc tải trọng (\*) khi và chỉ khi Kích thước không nén không xác định.

## Người giới thiệu

* [Định dạng tệp LZMA](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)
* [Thuật toán chuỗi Lempel–Ziv–Markov](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

