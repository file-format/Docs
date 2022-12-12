{
  "date" : "2019-10-11",
  "keywords" :[ "tệp fodg", "định dạng tệp fodg", "tệp fodg là gì", "tệp", "ví dụ fodg", "phần mở rộng tệp fodg","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - Định dạng tệp bản vẽ OpenDocument",
  "description":"Tìm hiểu về định dạng tệp FODG và các API có thể tạo và mở tệp FODG.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp FODG là gì?

Tệp có phần mở rộng .fodg là định dạng tệp Bản vẽ Apache OpenOffice để lưu trữ các thành phần bản vẽ. Nó dựa trên các thông số định dạng tệp được nêu bởi Sự tiến bộ của các tiêu chuẩn thông tin kết cấu (OASIS). Một định dạng tệp tương tự khác dành cho đồ họa OpenOffice là [ODG](/vi/image/odg/) lưu trữ các thành phần bản vẽ dưới dạng hình ảnh véc-tơ. Các tệp FODG có thể được mở bằng OpenOffice cũng như LibreOffice. Ví dụ, các định dạng tệp khác được OpenOffice hỗ trợ bao gồm [ODT](/vi/word-processing/odt/), ODF, [ODP](/vi/presentation/odp/) và [ODS](/vi/spreadsheet/ods/).

## Định dạng tệp FODG

FODG dựa trên định dạng tệp XML của OpenDocument tuân theo Định dạng Tài liệu Mở OASIS ISO/IEC 26300. Nó có Loại Phương tiện Internet application/vnd.oasis.opendocument.graphics và cũng tuân thủ org.oasis-open.opendocument public.composite-content . Cấu trúc XML phổ biến cho tất cả các loại tài liệu như bảng tính, tệp bản vẽ và tài liệu văn bản. Các tài liệu OpenOffice tận dụng lợi thế của việc tách các mối quan tâm bằng cách tách nội dung, kiểu, siêu dữ liệu và cài đặt ứng dụng thành bốn tệp XML riêng biệt.

`<office:document-content> ` - Nội dung tài liệu và các kiểu tự động được sử dụng trong nội dung.
`<office:document-styles> ` - Các kiểu được sử dụng trong nội dung tài liệu và các kiểu tự động được sử dụng trong chính các kiểu đó.
`<office:document-meta> ` - Thông tin meta tài liệu, chẳng hạn như tác giả hoặc thời gian của hành động lưu cuối cùng.
`<office:document-settings> ` - Cài đặt dành riêng cho ứng dụng, chẳng hạn như kích thước cửa sổ hoặc thông tin máy in.

## Người giới thiệu ##
* [Thông số kỹ thuật trong tương lai cho tiêu chuẩn hóa v 1.3 ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [Định dạng Tài liệu Mở OASIS dành cho Ứng dụng Office](https://www.oasis-open.org/committees/tc_home.php?wg_abrev=office)
* [Định dạng Tài liệu Mở - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

