{
  "date" : "2019-10-11",
  "keywords" :[ "tệp emf", "định dạng tệp emf", "tệp emf là gì", "tệp", "ví dụ emf", "phần mở rộng tệp emf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Định dạng siêu tệp nâng cao",
  "description":"Tìm hiểu về định dạng tệp EMF và các API có thể tạo và mở tệp EMF.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp EMF là gì?

**Định dạng siêu tệp nâng cao (EMF)** lưu trữ hình ảnh đồ họa độc lập với thiết bị. Siêu tệp của EMF bao gồm các bản ghi có độ dài thay đổi theo thứ tự thời gian có thể hiển thị hình ảnh được lưu trữ sau khi phân tích cú pháp trên bất kỳ thiết bị đầu ra nào. Các bản ghi có độ dài thay đổi này có thể là định nghĩa của các đối tượng kèm theo, các lệnh để vẽ và các thuộc tính đồ họa quan trọng để hiển thị hình ảnh một cách chính xác. Khi một thiết bị mở siêu tệp EMF bằng môi trường đồ họa của chính nó, tỷ lệ, kích thước, màu sắc và các thuộc tính đồ họa khác của hình ảnh gốc vẫn giữ nguyên bất kể nền tảng thiết bị mở là gì.

## Lược Sử ##

Năm 1990, Microsoft đã thiết kế định dạng tệp hình ảnh Windows Metafile ([WMF](/vi/image/wmf/)) cho Microsoft Windows. Siêu tệp Windows có định dạng 16-bit có thể chứa một số thành phần bản đồ bit. WMF có thể bao gồm đồ họa véc-tơ và nhằm mục đích duy trì khả năng di động giữa các ứng dụng khác nhau. Năm 1993, Win32/GDI đã công bố Siêu tệp nâng cao (EMF), một phiên bản mới hơn với tính linh hoạt và khả năng mở rộng được nâng cao. EMF cũng được sử dụng làm lệnh ngôn ngữ đồ họa để chạy trình điều khiển máy in. Microsoft hiện khuyến nghị định dạng siêu tệp nâng cao (EMF) thay vì định dạng Windows (WMF). Khi Windows XP được giới thiệu, phiên bản Enhanced Metafile Format Plus (EMF+) đã được phát hành. Phiên bản mới hơn này hoạt động bằng cách tuần tự hóa các lệnh gọi API GDI+, tương tự như vậy, WMF/EMF ghi lại các lệnh gọi tới GDI. Có một phiên bản nén gzip của EMF được gọi là EMZ.

## Định dạng siêu tệp EMF ##

Sau đây là các yếu tố cần thiết của định dạng siêu tệp nâng cao:

* Một EMR_HEADER (phiên bản, kích thước, độ phân giải của ảnh lúc tạo)
* Một bảng cho các đối tượng GDI
* Một bảng màu dành riêng (tùy chọn)
* Bản ghi siêu tệp được sắp xếp theo cấu trúc mảng (cài đặt thuộc tính, đối tượng được xác định, lệnh vẽ)
* Bản ghi EMR_EOF (bản ghi cuối cùng trong siêu tệp EMF)

## Phiên bản EMF ##
* **Bản gốc**: Phiên bản gốc chỉ định bản ghi cần thiết để giữ hình ảnh gốc và duy trì hình ảnh độc lập với thiết bị. Hơn nữa, hỗ trợ bản ghi chứa các đối tượng đồ họa và các lệnh để vẽ.
* **Phiên bản 1**: Phiên bản thứ hai của EMF đã cải thiện tính linh hoạt và tính độc lập của thiết bị bằng cách thêm bản ghi cho định dạng pixel và cung cấp khả năng sử dụng lệnh OpenGL.
* **Phiên bản 2**: Phiên bản thứ ba đã nâng cao độ chính xác bằng cách thêm hệ thống Số liệu để đo khoảng cách bề mặt thiết bị, giúp bản ghi có thể mở rộng hơn.

## Bản ghi siêu tệp nâng cao ##

Các bản ghi siêu tệp được sắp xếp dưới dạng mảng. Các bản ghi này có cấu trúc ENHMETARECORD và có độ dài thay đổi. ENHMETARECORD chỉ định dữ liệu xác định các hàm GDI để tạo ảnh bằng cách sử dụng định dạng siêu tệp nâng cao. Cấu trúc **ENHMETAHEADER** luôn là bản ghi đầu tiên ở định dạng này. Tiêu đề EMF này chứa thông tin sau.

Mọi bản ghi của siêu tệp nâng cao đều có hai thành viên của EMR (cung cấp cấu trúc cơ sở) ngay từ đầu. Thành viên đầu tiên nhận ra chức năng GDI (các tham số được sử dụng trong bản ghi) xác định loại bản ghi và được gọi là iType. Thành viên khác nSize xác định kích thước của mỗi bản ghi. Các thông số còn lại (nếu có) và dữ liệu bổ sung sắp xếp ngay bên dưới nSize. Ngay sau tiêu đề, một mô tả văn bản tùy chọn có thể xuất hiện. Tên của hình ảnh và tác giả được ghi lại trong mô tả văn bản đó. Bảng màu có sự hiện diện của một tùy chọn chỉ định các màu được sử dụng trong quá trình tạo siêu tệp nâng cao. Các bản ghi khác được sử dụng để chỉ định chức năng GDI cần thiết trong việc tạo ảnh.

Ít nhất một bản ghi EMF phải có trong mỗi siêu tệp. Thông tin di chuyển từ bản ghi này sang bản ghi khác phụ thuộc vào bản ghi EMF nên các bản ghi này phải được sắp xếp liền kề. Tại bất kỳ bản ghi cụ thể nào trong siêu tệp ngoại trừ EOF_record, độ dài của bản ghi cụ thể đó được xác định để chuyển sang bản ghi tiếp theo.

## Tạo siêu tệp nâng cao ##

Hàm **CreateEnhMetaFile** được sử dụng để tạo siêu tệp nâng cao. Các đối số chức năng này được sử dụng để kích thước và lưu trữ hình ảnh trên đĩa/bộ nhớ. Hơn nữa, chức năng này yêu cầu kích thước của thiết bị mà hình ảnh xuất hiện đầu tiên (thiết bị được tham chiếu) và ngữ cảnh của thiết bị tham chiếu (DC). Vì vậy, các đối số để xử lý DC này phải cung cấp khi gọi hàm **CreateEnhMetaFile**. Cú pháp của hàm như sau:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** xử lý cho một thiết bị tham chiếu.

**lptoFilename:** Một con trỏ tới tên tệp.

**lprc:** Con trỏ tới cấu trúc hình bầu dục chỉ định kích thước hình ảnh tính bằng mm.

**lpDesc:** một con trỏ tới một chuỗi cho tiêu đề của ảnh và tên ứng dụng đã tạo ra ảnh.

## Hoạt động siêu tệp nâng cao ##

Sau đây là các công việc có thể được thực hiện bằng cách sử dụng tay cầm cho siêu tệp nâng cao.

* Hiển thị và chỉnh sửa hình ảnh được lưu trữ.
* Tạo các bản sao siêu tệp nâng cao.
* Truy xuất bản sao của tiêu đề EMF, mô tả tùy chọn và phiên bản nhị phân của siêu tệp nâng cao
* Tóm tắt lại các màu trong bảng màu.

## Đối tượng đồ họa ##

Trong các hoạt động vẽ và sơn, các đối tượng đồ họa có thể được tạo bởi các bản ghi tạo đối tượng và có thể lưu lại để sử dụng tiếp. Bản ghi `EMR_SELECTOBJECT` có thể truy xuất các đối tượng đồ họa này bằng ngữ cảnh thiết bị phát lại. Bút, bảng màu, cọ vẽ, không gian màu, phông chữ và đối tượng stock là một số loại đối tượng có thể tái sử dụng.

## Thứ tự byte ##

Định dạng Little-endian được sử dụng để lưu trữ dữ liệu trong các bản ghi siêu tệp.

## Phiên bản ##

Định dạng tệp EMF đã được sửa đổi hai lần. Các phiên bản đã thay đổi là phiên bản gốc, tiện ích mở rộng 1 và tiện ích mở rộng 2. Các phiên bản mở rộng có cung cấp bản ghi OpenGL và bộ mô tả tùy chọn cho định dạng pixel bên trong. Một cơ sở đo tính bằng mililit được thêm vào cho các kích thước được hiển thị.

## Người giới thiệu ##

* [Siêu tệp định dạng nâng cao | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Đặc tả và định dạng siêu tệp nâng cao](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

