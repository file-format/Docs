{
  "date" : "2020-01-11",
  "keywords" :[ "tệp x", "định dạng tệp x", "tệp x là gì", "tệp", "ví dụ x", "phần mở rộng tệp x","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp X - DirectX 2.0",
  "description":"Tìm hiểu về định dạng tệp DirectX X và API có thể mở và tạo tệp DirectX X.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Tệp X là gì?

Tệp có phần mở rộng .x đề cập đến [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) định dạng tệp Đồ họa 3D cũ được giới thiệu với Microsoft DirectX 2.0. Nó được sử dụng để hiển thị đồ họa 3D trong trò chơi và chỉ định cấu trúc cho mắt lưới, kết cấu, hoạt ảnh và các đối tượng do người dùng xác định. Nó không còn được dùng nữa kể từ năm 2014 vì định dạng tệp FBX của Autodesk hoạt động tốt hơn dưới dạng định dạng hiện đại hơn. X được định hướng theo mẫu và không có bất kỳ kiến thức sử dụng nào.

Bạn có thể mở các tệp DirectX X bằng Microsoft DirectX và các trình soạn thảo văn bản phổ biến.

## Định dạng tệp X

[Tham chiếu tệp X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) chứa thông tin tham chiếu cho các phần tử API được sử dụng để làm việc với các tệp DirectX .x. Định dạng này cung cấp các nguyên hàm dữ liệu cấp thấp được các ứng dụng khác sử dụng để xác định các nguyên hàm cấp cao hơn thông qua các mẫu dữ liệu. DirectX 6.0 đã giới thiệu các giao diện và phương thức cho phép đọc và ghi vào tệp .x. DirectX 3.0 đã giới thiệu phiên bản nhị phân của định dạng tệp này.

[Tham chiếu định dạng tệp X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) do DirectX 9 xác định chứa thông tin tham chiếu cho .x các tệp ở dạng nhị phân cũng như Mã hóa văn bản.

### Mã hóa nhị phân

[Định dạng nhị phân](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) xác định định dạng DirectX X dưới dạng đại diện được mã hóa của định dạng văn bản. Các mã thông báo này có thể độc lập để cung cấp cấu trúc ngữ pháp hoặc có thể là mã thông báo mang bản ghi cung cấp dữ liệu cần thiết.

#### Tiêu đề

Tiêu đề nhị phân có thể được đọc và ghi bằng các định nghĩa sau.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Mã hóa văn bản

Các tệp DirectX .x không phụ thuộc vào cách tệp được sử dụng và không dành riêng cho bất kỳ ứng dụng nào. Cách tiếp cận dựa trên mẫu này cho phép bất kỳ ứng dụng khách nào sử dụng định dạng tệp .x.


#### Tiêu đề

Tiêu đề có độ dài thay đổi là bắt buộc và phải ở đầu luồng dữ liệu. Tiêu đề chứa dữ liệu sau.

|Loại |Loại phụ |Kích thước |Nội dung |Ý nghĩa nội dung|
---|---|---|---|---|
|Số ma thuật (bắt buộc)| | 4 byte |xof |
|Số phiên bản (bắt buộc) |Số chính |2 byte |03 |Phiên bản chính 3|
| |Số phụ |2 byte |02 |Phiên bản phụ 2|
|Kiểu định dạng (bắt buộc)| |4 byte |"txt " |Tệp văn bản|
| | | |"thùng rác" | Tệp nhị phân|
| | | |"tzip"| Tệp văn bản nén MSZip |
| | | |"bzip"| Tệp nhị phân nén MSZip |
|Kích thước float (bắt buộc)| |4 byte| 0064| Phao 64-bit|
| | | |0032 |32-bit float|


## Người giới thiệu

* [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [Tham chiếu định dạng tệp DirectX 9](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

