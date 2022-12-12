{
  "date" : "2021-04-08",
  "keywords" :[ "tệp lz", "định dạng tệp lz", "tệp lz là gì", "tệp", "ví dụ lz", "phần mở rộng tệp lz","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Định dạng tệp nén Lzip",
  "description":"Tìm hiểu về định dạng tệp LZ và API có thể tạo và mở tệp LZ.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Tệp LZ là gì?

Tệp có phần mở rộng .lz là tệp lưu trữ nén được tạo bằng Lzip, đây là một công cụ nén dòng lệnh miễn phí. Nó hỗ trợ nối để nén các tập tin hỗ trợ. Các tệp LZ có loại phương tiện application/lzip và hỗ trợ tỷ lệ nén cao hơn [BZ2](/vi/compression/bz2). LZ dựa trên thuật toán LZMA (chuỗi Lempel-Ziv-Markov) và bao gồm tổng kiểm tra CRC 32 bit và các byte nhận dạng để kiểm tra tính toàn vẹn của tệp.

## Định dạng nén LZMA

Định dạng nén LZMA bao gồm một luồng bit nén được mã hóa bằng bộ mã hóa phạm vi nhị phân thích ứng. Luồng được chia thành các gói. Mỗi gói mô tả một byte đơn hoặc một chuỗi LZ77. Độ dài và khoảng cách của mỗi gói được mã hóa ngầm hoặc rõ ràng.

Bảy loại gói như sau ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Mã gói (chuỗi bit) |Tên gói |Mô tả gói|
---|---|---|
|0 + mã byte| LIT| Một byte đơn được mã hóa bằng bộ mã hóa phạm vi nhị phân thích ứng.|
|1+0 + len + xa| TRẬN ĐẤU| Trình tự LZ77 điển hình mô tả độ dài và khoảng cách của trình tự.|
|1+1+0+0| RÚT GỌN| Chuỗi LZ77 một byte. Khoảng cách bằng với khoảng cách LZ77 được sử dụng gần đây nhất.|
|1+1+0+1 + len| DÀI HƠN[0]| Một trình tự LZ77. Khoảng cách bằng với khoảng cách LZ77 được sử dụng gần đây nhất.|
|1+1+1+0 + len| LONGREP[1]| Một trình tự LZ77. Khoảng cách bằng với khoảng cách LZ77 được sử dụng lần cuối thứ hai.|
|1+1+1+1+0 + len| DÀI HƠN[2]| Một trình tự LZ77. Khoảng cách bằng với khoảng cách LZ77 được sử dụng lần thứ ba gần đây nhất.|
|1+1+1+1+1 + len| LONGREP[3]| Một trình tự LZ77. Khoảng cách bằng với khoảng cách LZ77 được sử dụng lần cuối thứ tư.|


## Người giới thiệu

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://vi.wikipedia.org/wiki/Lzip)

