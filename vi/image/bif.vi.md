{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp BIF - Định dạng hình ảnh toàn bộ slide Ventana",
  "description":"Tìm hiểu về định dạng tệp BIF và các API có thể tạo và mở tệp BIF.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Tệp BIF là gì?

Tệp BIF là tệp hình ảnh raster có chứa hình ảnh mẫu vật chiếu. Nó bao gồm nhiều hình ảnh TIFF được kết hợp bởi các ứng dụng xem slide thành một hình ảnh tổng hợp duy nhất. Các tệp BIF được tạo bởi máy quét slide kỹ thuật số của Hệ thống y tế Ventana và hoàn toàn tuân thủ biến thể BigTIFF của định nghĩa [TIFF](/vi/image/tiff/) v 6.0.

## Định dạng tệp BIF

Tệp BIF được lưu dưới dạng tệp hình ảnh nhị phân và bao gồm tối đa 200.000 x 200.000 pixel. Điều này có thể dẫn đến kích thước tệp lớn, phá vỡ giới hạn kích thước 4 GB do con trỏ tệp 32 bit được xác định bởi tiêu chuẩn TIF áp đặt. Tuy nhiên, với các con trỏ tệp 64 bit, rào cản về kích thước tệp này được khắc phục bằng biến thể BigTIFF của tiêu chuẩn TIFF.

### Ai sử dụng tệp BIF?

Các tệp BIF được sử dụng bởi máy quét slide kỹ thuật số để quét và tạo các bản sao kỹ thuật số của các mẫu slide. Nếu bạn là Nhà nghiên cứu bệnh học, bạn có thể mở các tệp BIF này trong các ứng dụng xem trang trình bày. Với mức độ chi tiết tuyệt vời và dữ liệu có độ phân giải cao, bạn có thể phóng to và thu nhỏ hình ảnh trang trình bày để xem các phần mẫu vật chi tiết hơn hoặc ít hơn. Tệp siêu dữ liệu [XML](/vi/web/xml/) có trong các tệp này xác định cách kết hợp các hình ảnh và hình ảnh sẽ được sử dụng làm hình thu nhỏ của tệp.

## Làm cách nào để mở tệp BIF?

Bạn có thể mở tệp BIF bằng:

* OpenSlide (đa nền tảng)
* ImageJ (đa nền tảng)
* Trình xem NetScope (Windows)

## Người giới thiệu ##

* [Báo cáo chính thức về BIF của Roche Digital Pathology](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

