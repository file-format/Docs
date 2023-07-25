{
  "date" : "2020-08-20",
  "keywords" :[ "tệp eot", "định dạng tệp eot", "tệp eot là gì", "tệp", "ví dụ eot", "phần mở rộng tệp eot","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - Định dạng tệp phông chữ TrueType",
  "description":"Tìm hiểu về Định dạng tệp EOT và API để tạo và mở tệp EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Tệp EOT là gì?

Tệp có phần mở rộng .eot là phông chữ OpenType được nhúng trong tài liệu. Chúng chủ yếu được sử dụng trong các tệp web, chẳng hạn như trang Web. Nó được tạo bởi Microsoft và được hỗ trợ bởi các Sản phẩm của Microsoft bao gồm tệp bản trình bày PowerPoint [.pps](/vi/presentation/pps). Tệp không được sử dụng chính và là loại tài liệu đi kèm với tài liệu hoặc trang web chính. Tương tự như các phông chữ OTF, EOT hỗ trợ cả phác thảo Postscript và TrueType cho các nét tượng trưng. Các tệp EOT có kích thước nhỏ hơn vì lý do chúng được nén bằng cách nén LZ. EOT sử dụng công cụ của Microsoft để tạo phông chữ từ các phông chữ TTF/OTF hiện có.

## Tóm tắt lịch sử

Phông chữ EOT đã được gửi tới W3C vào năm 2007 như một phần của CSS3 nhưng do yêu cầu của nó là phải được cài đặt vĩnh viễn trên hệ thống từ xa đã trở thành lý do khiến nó bị từ chối. Nó đã được gửi lại vào tháng 3 năm 2008, nhưng W3C cuối cùng đã chọn [Định dạng Phông chữ Web](/vi/font/woff/) (WOFF) đã được chuẩn hóa sau đó.

## Định dạng tệp EOT

Bạn có thể tìm thấy chi tiết định dạng tệp EOT trên [trang gửi W3](https://www.w3.org/Submission/EOT/#FileFormat) và xây dựng cấu trúc được định dạng phông chữ này sử dụng. EOT bao gồm một cấu trúc EMBEDDEDFONT duy nhất cung cấp đủ thông tin cơ bản về tên phông chữ hte và các ký tự được hỗ trợ. Việc đóng gói thông tin này cho phép Tác nhân người dùng tránh giải nén, giải nén hoặc cài đặt phông chữ nếu nó đã có trên máy.

### Cấu trúc EMBEDDEDFONT
Cấu trúc EMBEDDEDFONT đã trải qua ba lần sửa đổi, với việc bổ sung dữ liệu bổ sung ở cuối cấu trúc với mỗi lần sửa đổi. Phiên bản cuối cùng của cấu trúc EMBEDDEDFONT được mô tả bên dưới.

|Kiểu dữ liệu|Tên mục nhập|Mô tả|
---|---|---|
|unsigned long|EOTSize|Tổng chiều dài cấu trúc tính bằng byte (bao gồm dữ liệu chuỗi và phông chữ)|
|unsigned long|FontDataSize|Độ dài của phông chữ OpenType (FontData) tính bằng byte|
|unsigned long|Phiên bản|Số phiên bản của định dạng này - 0x00020002|
|unsigned long|Cờ|Đang xử lý cờ|
|byte[10]|Phông chữPANOSE|Giá trị PANOSE cho phông chữ này - Xem http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|Trong Windows, điều này bắt nguồn từ TEXTMETRIC.tmCharSet. Giá trị này chỉ định bộ ký tự của phông chữ. DEFAULT_CHARSET (0x01) cho biết không có tùy chọn nào. - Xem https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Nếu bit cho ITALIC được đặt trong OS/2.fsSelection, giá trị sẽ là 0x01 - Xem http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Trọng lượng|Giá trị trọng số cho phông chữ này - Xem http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Loại cờ cung cấp thông tin về quyền nhúng - Xem http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|Magic number cho tệp EOT - 0x504C. Dùng để kiểm tra xem dữ liệu có bị hỏng không.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bit 0-31) - Xem http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bit 32-63) - Xem http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bit 64-95) - Xem http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bit 96-127) - Xem http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bit 0-31) - Xem http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bit 32-63) - Xem http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Xem http://www.microsoft.com/typography/otspec/head.htm|
|unsigned long|Reserveed1|Reserveed - phải là 0|
|unsigned long|Reserveed2|Reserveed - phải là 0|
|unsigned long|Reserveed3|Reserveed - phải là 0|
|unsigned long|Reserveed4|Reserveed - phải là 0|
|unsigned short|Padding1|Padding để duy trì sự liên kết dài. Giá trị đệm phải luôn được đặt thành 0x0000.|
|unsigned short|FamilyNameSize|Số byte được sử dụng bởi mảng FamilyName|
|byte|FamilyName[FamilyNameSize]|Mảng ký tự UTF-16 có độ dài bằng byte FamilyNameSize. Đây là chuỗi Font Family ngôn ngữ tiếng Anh được tìm thấy trong bảng tên của phông chữ (tên ID = 1) - Xem http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding2|Giá trị đệm phải luôn được đặt thành 0x0000.|
|unsigned short|StyleNameSize|Số byte được sử dụng bởi StyleName|
|byte|StyleName[StyleNameSize]|Mảng ký tự UTF-16 có độ dài bằng byte StyleNameSize. Đây là chuỗi Phân họ phông chữ ngôn ngữ tiếng Anh được tìm thấy trong bảng tên của phông chữ (tên ID = 2) - Xem http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding3|Giá trị đệm phải luôn được đặt thành 0x0000.|
|unsigned short|VersionNameSize|Số byte được sử dụng bởi VersionName|
|bytes|VersionName[VersionNameSize]|Mảng ký tự UTF-16 có độ dài bằng VersionNameSize byte. Đây là chuỗi phiên bản tiếng Anh được tìm thấy trong bảng tên của phông chữ (tên ID = 5) - Xem http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding4|Giá trị đệm phải luôn được đặt thành 0x0000.|
|unsigned short|FullNameSize|Số byte được sử dụng bởi FullName|
|byte|FullName[FullNameSize]|Mảng ký tự UTF-16 có độ dài bằng FullNameSize byte. Đây là chuỗi tên đầy đủ của ngôn ngữ tiếng Anh được tìm thấy trong bảng tên của phông chữ (tên ID = 4) - Xem http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding5|Giá trị đệm phải luôn được đặt thành 0x0000.|
|unsigned short|RootStringSize|Số byte được sử dụng bởi mảng RootString|
|byte|RootString[RootStringSize]|Mảng ký tự UTF-16 có độ dài bằng RootStringSize byte.|
|unsigned long|RootStringCheckSum|Giá trị RootString CheckSum. Xem thuật toán để xử lý RootStringChecksum bên dưới.|
|unsigned long|EUDCCodePage|Giá trị trang mã cần thiết để hỗ trợ phông chữ EUDC.|
|unsigned short|Padding6|Giá trị đệm phải luôn được đặt thành 0x0000.|
|unsigned short|SignatureSize|Số byte được sử dụng bởi mảng Chữ ký. Hiện được bảo lưu và phải được đặt thành 0x0000.|
|byte|Chữ ký[SignatureSize]|Hiện được bảo lưu. Nếu SignatureSize là 0x0000 thì mảng này không có độ dài.|
|unsigned long|EUDCFlags|Xử lý cờ cho phông chữ EUDC. Các giá trị điển hình có thể là TTEMBED_XORENCRYPTDATA và TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Số byte được sử dụng bởi mảng Chữ ký.|
|byte|EUDCFontData[EUDCFontSize]|Số byte được sử dụng cho dữ liệu phông chữ EUDC. Nếu EUDCFontSize là 0x00000000 thì mảng này không có độ dài.|
|byte|FontData[FontDataSize]|Dữ liệu phông chữ cho tệp EOT này. Dữ liệu có thể được nén hoặc mã hóa XOR như được chỉ báo bởi các cờ xử lý.|

## Người giới thiệu

* [Định dạng tệp EOT](https://www.w3.org/Submission/EOT/)
* [OpenType nhúng](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Nhúng phông chữ](https://en.wikipedia.org/wiki/Font_embedding)

