{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - Định dạng tệp bộ sưu tập TrueType",
  "description":"Tệp Bộ sưu tập TrueType (TTC) kết hợp nhiều phông chữ thành một tệp duy nhất. Cả Apple và Microsoft đều sử dụng TTF trên hệ điều hành Mac và Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Tệp TTC là gì?
TTC được viết tắt là TrueType Collection là phần mở rộng của định dạng True Type. Một tệp TTC có thể kết hợp nhiều tệp phông chữ vào đó. Các tệp này có lợi cho việc kết hợp nhiều phông chữ có chung nhiều nét chữ. Trước Windows 2000, các tệp TTC đã được sử dụng trong các phiên bản cửa sổ tiếng Trung, tiếng Nhật và tiếng Hàn nhưng sau này hỗ trợ đã có sẵn cho tất cả các vùng.


## Cấu trúc của tệp bộ sưu tập phông chữ
Tệp TTC bao gồm bảng Tiêu đề TTC, Thư mục bảng và nhiều bảng OpenType. Tiêu đề TTC phải được tìm thấy ở đầu tệp. Phải tồn tại một thư mục bảng hoàn chỉnh cho mỗi phông chữ. Định dạng TableDirectory phải tương tự như đã tồn tại trong tệp không phải bộ sưu tập. Số lượng bảng trong tất cả các thư mục trong tệp TTC được tính từ đầu tệp TTC.
Các bảng trong tệp TTC được tham chiếu thông qua thư mục bảng của các phông chữ tương ứng của chúng. Một số bảng OpenType phải xuất hiện nhiều lần, một lần cho mỗi phông chữ được thêm vào TTC. Trong khi các bảng khác có thể được chia sẻ bởi nhiều phông chữ trong tệp TTC.

### Tiêu đề TTC
Cho đến nay, có hai phiên bản của bảng Tiêu đề TTC:
- Phiên bản 1.0 dùng cho các file TTC không có chữ ký số.
- Phiên bản 2.0 có thể được sử dụng cho các tệp TTC có hoặc không có chữ ký số.
Dưới đây là các bảng Tiêu đề TTC của cả hai phiên bản:

**Tiêu đề TTC Phiên bản 1.0:**

|Loại|Tên|Mô tả|
---|---|---|
|TAG|ttcTag|Chuỗi ID Bộ sưu tập Phông chữ: 'ttcf' (được sử dụng cho các phông chữ có đường viền CFF hoặc CFF2 cũng như đường viền TrueType)|
|uint16|majorVersion|Phiên bản chính của Tiêu đề TTC, = 1.|
|uint16|minorVersion|Phiên bản phụ của Tiêu đề TTC, = 0.|
|uint32|numFonts|Số phông chữ trong TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Mảng bù đắp cho TableDirectory cho mỗi phông chữ từ đầu tệp|

**Tiêu đề TTC Phiên bản 2.0:**

|Loại|Tên|Mô tả|
---|---|---|
|TAG|ttcTag |Chuỗi ID bộ sưu tập phông chữ: 'ttcf'|
|uint16| majorVersion |Phiên bản chính của Tiêu đề TTC, = 2.|
|uint16| phiên bản phụ |Phiên bản phụ của Tiêu đề TTC, = 0.|
|uint32| numFonts |Số phông chữ trong TTC|
|bù đắp32| tableDirectoryOffsets[numFonts] |Mảng bù đắp cho TableDirectory cho mỗi phông chữ từ đầu tệp|
|uint32| dsigTag |Thẻ cho biết bảng DSIG tồn tại, 0x44534947 ('DSIG') (null nếu không có chữ ký)|
|uint32| dsigLength |Độ dài (tính bằng byte) của bảng DSIG (null nếu không có chữ ký)|
|uint32| dsigOffset |Phần bù (tính bằng byte) của bảng DSIG từ đầu tệp TTC (không có giá trị nếu không có chữ ký)|

## Người giới thiệu
* [Tệp Phông chữ OpenType](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://vi.wikipedia.org/wiki/TrueType)

