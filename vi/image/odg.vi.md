{
  "date" : "2019-10-11",
  "keywords" :[ "tệp odg", "định dạng tệp odg", "tệp odg là gì", "tệp", "ví dụ odg", "phần mở rộng tệp odg","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp ODG",
  "description":"Tìm hiểu về định dạng tệp ODG và API có thể tạo và mở tệp ODG.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp ODG là gì?

Định dạng tệp ODG được ứng dụng Draw của Apache OpenOffice sử dụng để lưu trữ các thành phần bản vẽ dưới dạng hình ảnh véc-tơ. Nó tuân theo các đặc tả định dạng tệp dựa trên XML được nêu bởi Sự tiến bộ của các tiêu chuẩn thông tin cấu trúc (OASIS). ODG thể hiện các bản vẽ dưới dạng ảnh vector sử dụng các điểm, đường thẳng và đường cong. Bên cạnh OpenOffice, LibreOffice và các ứng dụng khác cũng hỗ trợ làm việc với định dạng tệp ODG. Ví dụ, các định dạng khác được OpenOffice hỗ trợ bao gồm [ODT](/vi/word-processing/odt/), ODF, [ODP](/vi/presentation/odp/) và [ODS](/vi/spreadsheet/ods/).


## Định dạng tệp ODG Thông số kỹ thuật

Định dạng tệp ODG dựa trên định dạng OpenDocument là định dạng tài liệu XML có cấu trúc với lược đồ được xác định rõ.
Mỗi thành phần cấu trúc của một định dạng OpenDocument được đại diện bởi một phần tử có các thuộc tính được liên kết. Cấu trúc dựa trên XML là phổ biến cho tất cả các loại tài liệu như tài liệu văn bản, bảng tính hoặc tệp bản vẽ. Một tài liệu có thể chứa các phong cách khác nhau. Cấu trúc tệp OpenDocument bao gồm các thành phần sau.
* Gốc tài liệu
* Siêu dữ liệu tài liệu
* Phần tử cơ thể và các loại tài liệu
* Cài đặt ứng dụng
* Kịch bản
* Khai báo mặt chữ
* Phong cách
* Kiểu trang và bố cục

## Rễ tài liệu ##

Phần tử gốc của tài liệu chứa toàn bộ tài liệu và là phần tử chính của tệp ở định dạng OpenDocument. Các loại phần tử gốc tài liệu giống nhau được áp dụng cho tất cả các loại tài liệu như văn bản, tài liệu, bảng tính và tài liệu vẽ.

### Phần tử gốc ###
Một tài liệu XML duy nhất được đại diện bởi phần tử gốc của chính nó. Năm phần tử gốc được hỗ trợ khác nhau như sau.

`<office:document> ` - Hoàn thành tài liệu văn phòng trong một tài liệu XML đơn.
`<office:document-content> ` - Nội dung tài liệu và các kiểu tự động được sử dụng trong nội dung.
`<office:document-styles> ` - Các kiểu được sử dụng trong nội dung tài liệu và các kiểu tự động được sử dụng trong chính các kiểu đó.
`<office:document-meta> ` - Thông tin meta tài liệu, chẳng hạn như tác giả hoặc thời gian của hành động lưu cuối cùng.
`<office:document-settings> ` - Cài đặt dành riêng cho ứng dụng, chẳng hạn như kích thước cửa sổ hoặc thông tin máy in.

### Siêu dữ liệu tài liệu ODG ###
OpenDocument chứa tất cả các thành phần siêu dữ liệu trong \<office:meta> yếu tố. Thông tin chung về tài liệu này được chứa ở phần đầu của tài liệu và các ứng dụng có thể cập nhật nhiều phiên bản của cùng một phần tử.

### Phần tử nội dung và các loại tài liệu ###
Nội dung tài liệu cho biết loại nội dung chứa trong tài liệu bằng cách sử dụng phần tử loại tài liệu. Các loại tài liệu này là:
* tài liệu văn bản
* tài liệu vẽ
* tài liệu trình bày
* tài liệu bảng tính
* tài liệu biểu đồ
* tài liệu hình ảnh

### Cài đặt ứng dụng ###
Cài đặt cho các ứng dụng văn phòng đại diện cho các cài đặt khác nhau có liên quan đến cấu hình tài liệu hoặc giao diện trực quan của tài liệu. Mỗi danh mục được đại diện bởi một `<config:config-item-set> `. Ví dụ về các danh mục cài đặt như vậy bao gồm:
* Cài đặt tài liệu, ví dụ như máy in mặc định
* Xem Cài đặt, ví dụ: mức thu phóng

### Tập lệnh ###
Thông thường, một tài liệu có chứa một số tập lệnh. Mỗi tập lệnh trong tệp OpenDocument được biểu thị bằng dấu `<office:script> ` phần tử. Các phần tử tập lệnh này được chứa trong một `<office:scripts> ` phần tử. Tập lệnh không cập nhật tài liệu trong khi tài liệu đang tải.
### Font Face Khai báo ###

Một khai báo về mặt phông chữ chứa thông tin về các phông chữ được tác giả của tài liệu sử dụng. Thông tin này giúp định vị các phông chữ này trên các hệ thống khác.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Phong cách ###
Các kiểu sau đây được định dạng OpenDocument hỗ trợ.

`Kiểu phổ biến` - Biểu diễn XML của các kiểu như vậy được gọi là kiểu
`Kiểu tự động` - Chứa các thuộc tính định dạng, trong dạng xem giao diện người dùng của tài liệu, được gán cho một đối tượng chẳng hạn như đoạn văn.
`Mater Styles` - một kiểu phổ biến chứa thông tin định dạng và nội dung bổ sung được hiển thị cùng với nội dung tài liệu khi kiểu này được áp dụng. Một ví dụ về phong cách chính là các trang chính.

## Người giới thiệu ##
* [Định dạng Tài liệu Mở OASIS dành cho Ứng dụng Office](https://www.oasis-open.org/committees/tc_home.php?wg_abrev=office)
* [Định dạng Tài liệu Mở - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

