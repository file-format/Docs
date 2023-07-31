{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extension", "file", "file format", "Database File Type", "Database File Format", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp ADE và các API có thể tạo và mở tệp ADE.",
  "title" :"ADE - Tệp mở rộng dự án truy cập",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Tệp ADE là gì?

Tệp có phần mở rộng .ade là tệp Dự án Microsoft Access chứa đầu ra được biên dịch của thông tin có trong tệp dự án Microsoft Access ADP. Thông tin trong tệp dự án Access, ngoài Visual Basic for Applications (VBA), có sẵn ở dạng đã biên dịch trong tệp ADE. Dữ liệu được lưu trữ ở định dạng nén trong các tệp này để giảm kích cỡ tệp và cải thiện hiệu suất trong Access. Vì ADE là đầu ra được biên dịch của tệp dự án Access nên bất kỳ mã nguồn VBA nào là một phần của dự án, vẫn được bảo vệ bằng cách không cho phép nó là một phần của đầu ra. Các tệp ADE có thể được mở trong Microsoft Access 365.

## Định dạng tệp ADE - Thông tin khác

ADE là các tệp Cơ sở dữ liệu Access đã biên dịch được lưu vào đĩa dưới dạng tệp nhị phân. Cấu trúc tệp nội bộ của các tệp này không được biết.

Các tệp ADE có thể tạo ra sự cố khi mở dựa trên phiên bản Microsoft Access đã được sử dụng để tạo các tệp này. Cơ sở dữ liệu Access đang sử dụng phiên bản 64-bit của Microsoft Access 2010 và được biên dịch dưới dạng tệp MDE, [ACCDE](/vi/database/accde/) hoặc ADE phải được biên dịch lại trong Microsoft Access 2021 Gói Dịch vụ 1 (SP1) để hoạt động bình thường với Access 2010 SP1. Sự cố này xảy ra vì Access 2010 SP1 sử dụng phiên bản mới hơn của tệp VBE7.dll (phiên bản 7.00.1619).

## Người giới thiệu

* [Sự cố với tệp Access ADE](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Sử dụng định dạng tệp truy cập nào](https://support.microsoft.com/en-us/office/what-access-file-format-nên-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

