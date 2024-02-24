{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Tệp WOFF2 - Tệp định dạng phông chữ mở trên web 2.0",
  "description": "Tìm hiểu về tệp WOFF2 là gì và các API có thể tạo và mở tệp WOFF2.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-vi2"
}
},
  "lastmod": "2023-01-10"
}

## Tập tin WOFF2 là gì?

WOFF2 là định dạng tệp phông chữ là phiên bản nén hơn của Định dạng Phông chữ Mở Web (WOFF). Nó được phát triển như một cách để giảm kích thước tệp phông chữ web, cho phép chúng tải nhanh hơn và sử dụng ít băng thông hơn. WOFF2 sử dụng thuật toán nén có tên Brotli để nén dữ liệu phông chữ, điều này có thể dẫn đến kích thước tệp nhỏ hơn đáng kể so với phông chữ [WOFF](/font/woff/) tương đương. Định dạng này được hỗ trợ bởi hầu hết các trình duyệt web hiện đại bao gồm Chrome, Firefox, Safari, Opera và Edge (phiên bản 14 trở đi).

## Định dạng tệp WOFF2 - Thông tin thêm

Cấu trúc tệp bên trong của tệp phông chữ WOFF2 bao gồm một số phần khác nhau, bao gồm tiêu đề, siêu dữ liệu, thư mục bảng và chính dữ liệu phông chữ.

 1. Tiêu đề chứa thông tin về định dạng tổng thể của tệp, bao gồm số phiên bản và số lượng bảng có trong tệp.

 1. Phần siêu dữ liệu chứa các thông tin như tên phông chữ, bản quyền và các thông tin khác liên quan đến phông chữ.

 1. Thư mục bảng chứa thông tin về các bảng khác nhau tạo nên phông chữ, bao gồm vị trí của chúng trong tệp và độ dài của chúng.

 1. Bản thân dữ liệu phông chữ được chia thành nhiều bảng khác nhau, mỗi bảng chứa thông tin cụ thể về phông chữ, chẳng hạn như các ký tự và glyph tương ứng của chúng. Các bảng này có thể bao gồm:

 * Bảng 'glyf' chứa các đường viền phông chữ thực tế, bao gồm hình dạng và kích thước của từng ký tự.
 * Bảng 'head' chứa thông tin chung về phông chữ, chẳng hạn như số phiên bản, kích thước thiết kế, v.v.
 * Bảng 'hmtx' chứa thông tin về số liệu của phông chữ, bao gồm độ rộng và vị trí của các ký tự.
 * Mỗi bảng được nén và lưu trữ ở định dạng tệp WOFF2 sau khi hoàn tất quá trình mã hóa.

Cấu trúc tổng thể được thiết kế để cho phép phân tích cú pháp và giải mã nhanh, để trình duyệt web có thể tải và hiển thị phông chữ trên trang web một cách nhanh chóng và hiệu quả.

### Tiêu đề WOFF2
Tiêu đề WOFF bao gồm một chữ ký nhận dạng cho biết loại dữ liệu có trong tệp. Tiêu đề WOFF cùng với các trường của nó như sau.

|Loại|Tên trường|Mô tả|
---|---|---|
|UInt32|chữ ký |0x774F4632 'wOF2' |
|UInt32| hương vị |Phiên bản sfnt của phông chữ đầu vào.|
|UInt32| length |Tổng kích thước của tệp WOFF.|
|UInt16| numTables |Số mục trong thư mục bảng phông chữ.|
|UInt16| dành riêng | Dành riêng; đặt về 0.|
|UInt32| TotalSfntSize |Tổng kích thước cần thiết cho dữ liệu phông chữ không nén, bao gồm tiêu đề sfnt, thư mục và bảng phông chữ (bao gồm cả phần đệm).|
|UInt32| TotalCompressionSize Tổng chiều dài của khối dữ liệu nén.|
|UInt16| MajorVersion |Phiên bản chính của tệp WOFF.|
|UInt16| MinorVersion |Phiên bản nhỏ của tệp WOFF.|
|UInt32| metaOffset |Bù đắp cho khối siêu dữ liệu, từ đầu tệp WOFF.|
|UInt32| metaLength |Độ dài của khối siêu dữ liệu được nén.|
|UInt32| metaOrigLength |Kích thước chưa nén của khối siêu dữ liệu.|
|UInt32| privOffset |Offset cho khối dữ liệu riêng tư, từ đầu tệp WOFF.|
|UInt32| privLength |Độ dài của khối dữ liệu riêng tư.|


## Người giới thiệu
 * [Định dạng tệp w3 WOFF2](https://www.w3.org/TR/WOFF2/)

