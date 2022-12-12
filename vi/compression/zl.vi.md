{
  "date" : "2019-12-09",
  "keywords" :[ "tệp zl", "định dạng tệp zl", "tệp zl là gì", "tệp", "ví dụ zl", "phần mở rộng tệp zl","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - Định dạng tệp nén ZLIP",
  "description":"Tìm hiểu về định dạng tệp ZL và các API có thể tạo và mở tệp ZL.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Tệp ZL là gì?

Tệp có phần mở rộng .zl là định dạng tệp nén ZLIP sử dụng một biến thể của thuật toán nén DEFLATE để nén tệp. Nó độc lập với loại CPU, hệ điều hành, hệ thống tệp và bộ ký tự và do đó có thể được sử dụng để trao đổi thông tin. Thông số kỹ thuật của nén ZLIP có sẵn trên [trang web IETF](https://tools.ietf.org/html/rfc1950) và có thể được giới thiệu từ quan điểm của nhà phát triển.

## Định dạng tệp ZL

Một luồng zlib có cấu trúc như sau:

* `CMF (Compression Method and flags)` - Byte này được chia thành phương pháp nén 4 bit và trường thông tin 4 bit tùy thuộc vào phương pháp nén.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Phương pháp nén)` - Nó xác định phương pháp nén được sử dụng trong tệp. Giá trị của nó và phương pháp nén tương ứng như sau.

| Giá trị CM| Nén|
|---|---|
|CM = 8|DEFLATE với kích thước cửa sổ lên tới 32K|
|CM = 15|Dự trữ|

* `CINFO (Thông tin nén)` - Với CM = 8, CINFO là logarit cơ số 2 của kích thước cửa sổ LZ77, trừ đi 8 (CINFO=7 biểu thị kích thước cửa sổ 32K).

* `FLG (FLaGs)` - Byte cờ này được chia như sau:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Người giới thiệu ##

* [Thông số định dạng tệp Zlib](https://tools.ietf.org/html/rfc1950)

