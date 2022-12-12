{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp CR2 - Tệp ảnh Canon Raw 2",
  "description":"Tìm hiểu về định dạng tệp CR2 và các API có thể tạo và mở tệp CR2.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Tệp CR2 là gì?

Tệp CR2 (Camera RAW 2) là tệp ảnh RAW được tạo bởi máy ảnh kỹ thuật số Canon. Nó lưu trữ dữ liệu hình ảnh không mất dữ liệu gốc chưa được xử lý do máy ảnh chụp. Định dạng tệp CR2 được Canon phát triển cho máy ảnh kỹ thuật số của mình và có thể ghi lại hình ảnh chất lượng cao lên đến 14 bit RGB. Điều này tạo ra hình ảnh chất lượng cao với đủ chỗ xử lý hậu kỳ. Định dạng ảnh CR2 đã được Canon sử dụng trong các mẫu máy ảnh 350D, 20D và 1D của họ. Tệp CR2 là tệp RAW và chứa thông tin siêu dữ liệu bổ sung như thông tin máy ảnh, thông tin ống kính, thông tin bù trừ, cân bằng trắng và các cài đặt khác.

## Định dạng tệp CR2

Các tệp CR2 được lưu vào thẻ nhớ máy ảnh dưới dạng tệp nhị phân ở định dạng tệp độc quyền của Canon. Định dạng tệp CR2 đã thay thế định dạng tệp CRW được sử dụng ban đầu và được thay thế bằng định dạng tệp Canon RAW 3 sau này. Định dạng tệp CR2 dựa trên thông số kỹ thuật [TIFF](/vi/image/tiff/) có 4 Thư mục tệp ảnh (IFD).

|Bù đắp |Nội dung |Nhận xét|
---|---|---|
|0x0000 |Header |chứa thứ tự byte, phiên bản và phần bù cho ảnh RAW|
|computed |IFD#0 |phần này chứa phần Exif, chứa phần Makernotes.
Thông tin về bức tranh#0|
|computed |picture#0 |phiên bản nhỏ của ảnh (bằng một phần tư kích thước của ảnh gốc), được nén ở định dạng Jpeg|
|đã tính toán |IFD#1 |Thông tin về hình ảnh#1.|
|được tính toán |hình ảnh số 1 |phiên bản nhỏ của hình ảnh, được nén ở định dạng Jpeg|
|đã tính toán |IFD#2 |Thông tin về hình ảnh#2.|
|được tính toán |hình ảnh#2 |phiên bản nhỏ của hình ảnh, không được nén|
|trong tiêu đề| IFD#3| Thông tin về ảnh số 3, ảnh RAW kích thước đầy đủ |
|computed |picture#3 |Dữ liệu hình ảnh RAW, được nén không mất dữ liệu ở định dạng Jpeg (không phải dữ liệu RGB!)|

## Ưu điểm của định dạng tệp CR2

Lưu trữ ảnh ở định dạng RAW cho phép thực hiện nhiều thao tác xử lý hậu kỳ đối với ảnh chẳng hạn như điều chỉnh Cân bằng trắng. Điều này khó khăn hơn nhiều và làm giảm chất lượng nghiêm trọng với các định dạng tệp hình ảnh khác, chẳng hạn như [JPEG](/vi/image/jpeg/).

## CR2 có tốt hơn JPEG không?

Tệp CR2 là tệp thô không bị mất dữ liệu và do đó không làm giảm chất lượng. Mặt khác, JPEG là định dạng tệp hình ảnh bị mất dữ liệu vì nó mất một số dữ liệu để giảm tệp. Do đó, các tệp CR2 có chất lượng cao và phù hợp hơn để chỉnh sửa và cải tiến.

## Người giới thiệu

* [Định dạng tệp CR2](http://lclevy.free.fr/cr2/)

