{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp CR3 - Tệp ảnh Canon Raw 3",
  "description":"Tìm hiểu về định dạng tệp CR3 và các API có thể tạo và mở tệp CR3.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Tệp CR3 là gì?

Tệp CR3 là định dạng tệp hình ảnh RAW của Canon được tạo bởi các máy ảnh kỹ thuật số Canon đã chọn. Nó được Canon giới thiệu để thay thế định dạng tệp CR2 và được sử dụng bởi một số thiết bị kỹ thuật số của Canon. Các tệp CR3 lưu trữ dữ liệu hình ảnh không mất dữ liệu gốc chưa được xử lý do máy ảnh chụp. Việc sử dụng những hình ảnh thô này cung cấp hình ảnh chất lượng cao và cho phép các nhiếp ảnh gia có nhiều chỗ để chỉnh sửa. Ngoài dữ liệu hình ảnh chính, các tệp CR3 còn lưu trữ thông tin siêu dữ liệu về hình ảnh.

## Định dạng tệp CR3

Các tệp CR3 được lưu vào đĩa dưới dạng tệp nhị phân ở Định dạng tệp phương tiện cơ sở ISO (ISO/IEC 14496-12) và cũng bao gồm [thẻ Canon] tùy chỉnh (https://exiftool.org/TagNames/Canon.html#uuid). Nó cũng bao gồm [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) là sự kết hợp của JPEG-LS (Rice-Golomb + RLE mã hóa) và JPEG-2000 (LeGall 5/3 DWT + định lượng).

## Thẻ tùy chỉnh CR3

Các tệp CR3 chứa các thẻ tùy chỉnh cho các mục đích khác nhau. Một số thẻ này như sau.

|ID thẻ| Tên thẻ| Có thể ghi |Giá trị / Ghi chú|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Thẻ CCTP của Canon|
|'CMT1' |IFD0| - |--> Thẻ EXIF|
|'CMT2' |ExifIFD| - |--> Thẻ EXIF|
|'CMT3' |MakerNoteCanon| - |--> Thẻ Canon|
|'CMT4' |Thông tin GPS| - |--> Thẻ GPS|
|'CNV' |CompressorVersion| không| |
|'CNOP' |CanonCNOP| - |--> Thẻ Canon CNOP|
|'CNTH' |CanonCNTH| - |--> Thẻ CNTH của Canon|
|'THMB' |Hình thu nhỏ| không| |

## Người giới thiệu

* [Định dạng tệp CR2](http://lclevy.free.fr/cr2/)
* [Thẻ Canon](https://exiftool.org/TagNames/Canon.html#uuid)

