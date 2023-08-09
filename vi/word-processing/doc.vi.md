{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "file", "extension", "file format", "Word", "Document" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Tệp tài liệu Microsoft Word",
  "description":"Tìm hiểu về định dạng tệp DOC và các API có thể tạo và mở tệp DOC.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Tệp DOC là gì?

Các tệp có phần mở rộng .doc đại diện cho các tài liệu được tạo bởi Microsoft Word hoặc các tài liệu xử lý văn bản khác ở định dạng tệp nhị phân. Phần mở rộng ban đầu được sử dụng cho tài liệu văn bản thuần túy trên một số hệ điều hành khác nhau. Nó có thể chứa một số loại dữ liệu khác nhau như hình ảnh, được định dạng cũng như văn bản thuần túy, đồ thị, biểu đồ, đối tượng được nhúng, liên kết, trang, định dạng trang, cài đặt in và nhiều thứ khác. Định dạng này phổ biến cho tất cả các loại tài liệu do có nhiều tùy chọn mà nó cung cấp cho người dùng để viết hướng dẫn sử dụng, đề xuất, thông số kỹ thuật, sơ yếu lý lịch, bài báo hoặc bất kỳ tài liệu tương tự nào. Phiên bản cập nhật của DOC là [DOCX](/vi/word-processing/docx/) dựa trên Office OpenXML có thông số kỹ thuật sẵn có công khai.

## Lược Sử ##

WordPerfect, một sản phẩm của [Corel](https://www.corel.com/en/), đã sử dụng DOC làm phần mở rộng của định dạng độc quyền của họ. Vào những năm 1980, WordPerfect vẫn là lựa chọn sử dụng trên hầu hết các máy tính do tính sẵn có dễ dàng, phù hợp với hầu hết các máy tính và Hệ điều hành. Tuy nhiên, WordPerfect đã chứng kiến sự sụp đổ của nó trên HĐH Windows khi Microsoft giới thiệu Microsoft Word làm sản phẩm của mình cho định dạng tệp tài liệu và chọn phần mở rộng DOC cho định dạng độc quyền của họ. Khi Microsoft Word ngày càng trở nên phổ biến, định dạng tệp DOC đã trải qua một số lần sửa đổi từ Microsoft Word 97 - 2003. Đó là năm 2007 khi định dạng tệp DOC mặc định được thay thế bằng định dạng Office Open XML (được gọi là DOCX) và các phiên bản mới của Microsoft Word hiện sử dụng tiện ích mở rộng mới này làm định dạng tệp mặc định.

## Thông số kỹ thuật định dạng tệp DOC - Thông tin khác

Microsoft đã không phát hành các đặc tả định dạng tệp DOC trong một thời gian dài cho đến năm 2008. Vào tháng 2 năm 2008, các đặc tả định dạng đã được phát hành cho định dạng tệp .doc theo Lời hứa Đặc tả Mở của Microsoft. Mặc dù thông số kỹ thuật không mô tả tất cả các tính năng mà định dạng DOC sử dụng, nhưng nó cung cấp nhiều thông tin về kiến thức cần thiết để làm việc với định dạng tệp này. Tuy nhiên, kỹ thuật đảo ngược là cần thiết để sử dụng các thông tin có sẵn. Thông số kỹ thuật đã được cập nhật nhiều lần và [bản sửa đổi] mới nhất(https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) là 8.0 được cập nhật kể từ tháng 8 năm 2018 .

### Một số khái niệm cơ bản ###

Trước khi chúng tôi đi vào bất kỳ chi tiết nào về đặc tả định dạng tệp cho DOC, cần hiểu một số khái niệm cơ bản để làm việc với định dạng tệp này.

**Cơ sở thông tin tệp (Fib):** Cấu trúc Fib chứa thông tin về tài liệu và chỉ định con trỏ tệp tới các phần khác nhau tạo nên tài liệu.
Fib là một cấu trúc có độ dài thay đổi. Ngoại trừ phần cơ sở có kích thước cố định, mỗi phần được bắt đầu bằng một trường đếm xác định kích thước của phần tiếp theo.

**Vị trí ký tự:** CP hoặc Vị trí ký tự biểu thị một số nguyên 32 bit không dấu đóng vai trò là chỉ mục dựa trên số 0 của một ký tự trong văn bản tài liệu. Không thể truy xuất trực tiếp vị trí và kích thước của từng ký tự trong tệp và cần được tính toán bằng thuật toán được chỉ định trước. Nhân vật bao gồm:

* Nội dung của tài liệu
* Neo của các đối tượng như chú thích hoặc hộp văn bản
* Các ký tự điều khiển như dấu phân đoạn và dấu ô trong bảng

**PLC:** Cấu trúc PLC là một mảng các CP theo sau là một mảng các phần tử dữ liệu. Các phần tử dữ liệu cho bất kỳ PLC nào phải có cùng kích thước từ 0 byte trở lên và vì lý do này, số lượng CP phải nhiều hơn một phần tử dữ liệu. Các cấu trúc PLC có nhiều loại khác nhau trong đó mỗi loại chỉ định liệu các CP trùng lặp có được phép cho loại đó hay không. Cấu trúc của một PLC bao gồm:

* **aCP (độ dài thay đổi):** Một mảng các phần tử CP. Mỗi loại cấu trúc **PLC** chỉ định ý nghĩa của các phần tử CP và phạm vi cho phép.
* **aDữ liệu (độ dài thay đổi):** Mỗi loại cấu trúc **PLC** chỉ định cấu trúc và ý nghĩa của các thành phần dữ liệu, bất kỳ hạn chế nào về số lượng thành phần dữ liệu và bất kỳ hạn chế nào đối với dữ liệu chứa trong đó. Nó cũng xác định mối quan hệ giữa các phần tử dữ liệu và các CP tương ứng.

**Lựa chọn hợp lệ:** Cấu trúc tệp .DOC chủ yếu được mô tả bởi một loạt các CP. Có một số [quy tắc](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) được Microsoft chỉ định phải tuân theo trong trường hợp như vậy.

**STTB:** STTB là một bảng chuỗi được tạo thành từ một tiêu đề theo sau là một mảng các phần tử. Giá trị **cData** chỉ định số phần tử có trong mảng.

**Lưu trữ Thuộc tính:** Một tệp từ có thể có các thành phần khác nhau như văn bản, đoạn văn, bảng, ảnh và các phần trong đó mỗi thành phần có thể có các thuộc tính riêng. Các thuộc tính này được lưu trữ trong tệp Word dưới dạng khác biệt so với mặc định. Những khác biệt như vậy được chỉ định bởi PRl bao gồm một Công cụ sửa đổi thuộc tính đơn (Sprm) và toán hạng của nó. Một ứng dụng có thể xác định tập hợp thuộc tính cuối cùng bằng cách áp dụng danh sách **Prl**s.

**Bảo vệ bằng mật khẩu:** Các tệp Word cũng có thể được bảo vệ bằng mật khẩu, có thể sử dụng một trong các cơ chế sau.

* Làm xáo trộn XOR
* Mã hóa tài liệu nhị phân văn phòng RC4
* Văn phòng mã hóa tài liệu nhị phân RC4 CryptoAPI

Nếu FibBase.fEncrypted và FibBase.fObfuscation đều là 1, thì tệp sẽ bị xáo trộn bằng cách sử dụng XOR obfuscation.

Nếu FibBase.fEncrypted là 1 và FibBase.fObfuscation là 0, thì tệp được mã hóa bằng cách sử dụng Mã hóa RC4 Tài liệu nhị phân Office hoặc Mã hóa RC4 CryptoAPI của Tài liệu nhị phân Office, với EncryptionHeader được lưu trữ trong các byte FibBase.lKey đầu tiên của luồng Bảng. EncryptionHeader.EncryptionVersionInfo chỉ định cơ chế mã hóa nào được sử dụng để mã hóa tệp.

### Cấu trúc tệp ###

Tệp Word nhị phân ở dạng nguyên bản là tệp hỗn hợp OLE bao gồm một số kho lưu trữ và luồng. Các kho lưu trữ và luồng này có cấu trúc và kích thước riêng, chỉ định các tham số để ghi và đọc. Đó là:

#### Luồng WordDocument ####

Luồng này chứa văn bản tài liệu và các thông tin khác được tham chiếu từ các phần khác của tệp. Luồng không có cấu trúc được xác định trước ngoài FIB ở đầu, cấu trúc này là bắt buộc và phải ở độ lệch 0. Luồng này không được lớn hơn 2147 MB.

#### 1TableStream hoặc 0TableStream ####

Tệp Word nhị phân có thể chứa Luồng bảng được gọi là luồng 1Table hoặc luồng 0Table. Ít nhất một trong số này nên có mặt trong tài liệu. Tuy nhiên, nếu tài liệu chứa cả luồng 1Table và 0Table, thì chỉ luồng được tham chiếu bởi base.fWhichTblStm được sử dụng. Luồng không được ước tính PHẢI được bỏ qua.
Luồng bảng KHÔNG ĐƯỢC lớn hơn 2147 MB.

#### Dòng dữ liệu ####

Luồng dữ liệu không có cấu trúc được xác định trước. Nó chứa dữ liệu được tham chiếu từ FIB hoặc từ các phần khác của tệp. Luồng này không cần phải có mặt nếu không có tham chiếu đến nó. Luồng dữ liệu KHÔNG ĐƯỢC lớn hơn 2147 MB.

#### Lưu trữ nhóm đối tượng ####

Bộ lưu trữ nhóm đối tượng chứa các kho lưu trữ cho các đối tượng OLE được nhúng. Lưu trữ này không cần phải có mặt nếu không có đối tượng OLE nhúng trong tài liệu.

#### Lưu trữ dữ liệu XML tùy chỉnh ####

Kho lưu trữ Dữ liệu XML tùy chỉnh là một kho lưu trữ tùy chọn có tên PHẢI là "MsoDataStore".

#### Luồng thông tin tóm tắt ####

Luồng Thông tin Tóm tắt là một luồng tùy chọn có tên PHẢI là "\005SummaryInformation", trong đó \005 là ký tự có giá trị 0x0005 và không phải là chuỗi ký tự "\005".

#### Luồng thông tin tóm tắt tài liệu ####

Luồng Thông tin Tóm tắt Tài liệu là một luồng tùy chọn có tên PHẢI là "\005DocumentSummaryInformation", trong đó \005 là ký tự có giá trị 0x0005, không phải là chuỗi ký tự "\005".

#### Dòng mã hóa ####

Luồng mã hóa là luồng tùy chọn có tên PHẢI là "mã hóa". Luồng này KHÔNG ĐƯỢC xuất hiện trừ khi đáp ứng cả hai điều kiện sau:

* Tài liệu được mã hóa bằng Mã hóa tài liệu nhị phân RC4 CryptoAPI của Office.
* Giá trị fDocProps được đặt trong EncryptionHeader.Flags.

#### Lưu trữ macro ####

Bộ lưu trữ Macro là bộ lưu trữ tùy chọn có chứa các macro cho tệp. Nếu có, nó PHẢI là Bộ lưu trữ gốc của dự án.

#### Lưu trữ Chữ ký XML ####

Bộ lưu trữ chữ ký XML là một bộ lưu trữ tùy chọn có tên PHẢI là "_xmlsignatures".

#### Dòng chữ ký ####

Luồng chữ ký là một luồng tùy chọn có tên PHẢI là "_signatures". Luồng này chứa chữ ký số.

#### Quản lý quyền thông tin Không gian lưu trữ dữ liệu ####

Bộ lưu trữ Không gian Dữ liệu Quản lý Quyền Thông tin là một bộ lưu trữ tùy chọn có tên PHẢI là "\006DataSpaces", trong đó \006 là ký tự có giá trị 0x0006 và không phải là chuỗi ký tự "\006". Nếu có bộ lưu trữ này thì Luồng nội dung được bảo vệ cũng PHẢI có.
Nếu có bộ lưu trữ này, thì tất cả các luồng và kho lưu trữ được chỉ định ngoài kho lưu trữ này và Luồng Nội dung được Bảo vệ NÊN được đọc từ Luồng Nội dung được Bảo vệ như được chỉ định trong [MS-OFFCRYPTO] và nếu có bất kỳ luồng và kho lưu trữ nào trong số đó tồn tại bên ngoài Nội dung được Bảo vệ Stream, chúng NÊN được bỏ qua.

#### Luồng nội dung được bảo vệ ####

Luồng nội dung được bảo vệ là một luồng tùy chọn có tên PHẢI là "\009DRMContent", trong đó \009 là ký tự có giá trị 0x0009 và không phải là chuỗi ký tự "\009".
Nếu có luồng này, thì Bộ lưu trữ Không gian Dữ liệu Quản lý Quyền Thông tin cũng PHẢI có.

## Người giới thiệu ##

* [Thông số kỹ thuật tạo tệp MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc máy tính](https://en.wikipedia.org/wiki/Doc_(computing))

