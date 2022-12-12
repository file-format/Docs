{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Tìm hiểu về định dạng tệp PCL và các API có thể tạo và mở tệp PCL.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp PCL là gì? ##

PCL là viết tắt của Ngôn ngữ Lệnh Máy in, là Ngôn ngữ Mô tả Trang được giới thiệu bởi Hewlett Packard (HP). HP đã tạo PCL để cung cấp một cách hiệu quả để kiểm soát các tính năng của máy in trên nhiều thiết bị in khác nhau. Định dạng ban đầu được phát triển cho máy in kim và máy in phun của HP, nhưng đã là một phần của các máy in nhiệt, ma trận và trang khác nhau theo thời gian. Định dạng đã trải qua một số sửa đổi khác nhau, dẫn đến các phiên bản khác nhau trong đó mỗi phiên bản được cải tiến để đáp ứng nhu cầu về thời gian đối với các tính năng điều khiển máy in. Ngày nay, PCL là ngôn ngữ máy in phổ biến rộng rãi nhất trên thị trường máy in mới nhất.

## Phiên bản PCL ##

Các phiên bản PCL khác nhau về chức năng (ví dụ: hỗ trợ loại phông chữ: phông chữ bitmap, phông chữ có thể mở rộng (phông chữ Intellifont, TrueType), phương pháp nén đồ họa raster, hỗ trợ đồ họa HP-GL/2).

**PCL 1:** khoảng năm 1980 - Chức năng In và Dấu cách là tập hợp các chức năng cơ bản được cung cấp cho đầu ra máy trạm một người dùng đơn giản, thuận tiện.

**PCL 2:** khoảng năm 1980 - EDP (Xử lý dữ liệu điện tử)/Chức năng giao dịch là tập hợp thay thế của PCL 1. Các chức năng được thêm vào cho mục đích chung, in hệ thống nhiều người dùng.

**PCL 3**: 1984 - Chức năng Xử lý văn bản của Office là tập hợp cao nhất của PCL 2. Các chức năng đã được thêm vào để sản xuất tài liệu văn phòng, chất lượng cao và tăng dpi lên đến 300 dpi. Nó cho phép sử dụng một số phông chữ và đồ họa được ánh xạ bit hạn chế và hỗ trợ HP-GL. PCL 3 đã được các nhà sản xuất máy in khác bắt chước rộng rãi và được các công ty này gọi là “Mô phỏng LaserJet Plus”.
(Máy in: dòng HP DeskJet, máy in dòng HP LaserJet, máy in dòng HP LaserJet Plus)

**PCL3+:** Được dòng máy in DeskJet và DesignJet sử dụng.

**PCL3c:** Được dòng máy in DeskJet và DesignJet sử dụng.

**PCL3e**: Được sử dụng bởi dòng máy in DeskJet và DesignJet. Hiện cũng được sử dụng trong PhotoSmart.

**PCL3GUI**: Sử dụng RTL và được dòng máy in DeskJet và DesignJet sử dụng.

**PCLSLEEK**: Sử dụng RTL và được dòng máy in DeskJet và DesignJet sử dụng.

**PCL 4**: 1985 - Chức năng định dạng trang là tập hợp cao nhất của PCL 3. Các macro được hỗ trợ, phông chữ và đồ họa được ánh xạ bit lớn hơn. (Máy in: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Chức năng Xuất bản Office là tập hợp cao nhất của PCL 4. Các khả năng xuất bản mới bao gồm chia tỷ lệ phông chữ và đồ họa (vector) HP-GL/2. (Máy in: HP LaserJet III)

**PCL 5e:** 1994 - Đây là bản sửa đổi lớn, bao gồm các tính năng mới như Hệ thống nén thích ứng, mã hóa ký tự 2byte, hỗ trợ phông chữ vectơ và các lệnh cấu hình hai chiều. Bao gồm các Thao tác logic (tương ứng với GDI ROP) để cải thiện khả năng hỗ trợ của Windows trước khi cắt các đường dẫn. (Máy in: HP LaserJet 4)

**PCL 5j:** Các tính năng mới như hỗ trợ ký tự 2 byte cho phông chữ có thể mở rộng dành cho người Nhật, cách viết dọc, khổ giấy và chuỗi kiểu chữ của Nhật Bản. (Máy in: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Hỗ trợ màu sắc và Hoạt động logic được thêm vào PCL5. PCL5c có trước PCL5e. Một số kiểu máy cũng hỗ trợ các đường cắt. (Máy in: HP Color LaserJet, HP PaintJet 300 XL (máy in đầu tiên có PCL5c), HP DeskJet 1200C/1600C (các số kiểu máy này đã được sử dụng lại và các kiểu máy mới hơn không phải là PCL 5c)

**PCL 5ce:** Hỗ trợ các kiểu chữ có thể mở rộng Agfa Microtype. (Máy in: Máy in HP 2500c Pro)

**PCL 6 / XL:** 1996 - PCL 6 hoặc PCL XL là một định dạng mới được giới thiệu vào năm 1995, không tương thích với bất kỳ phiên bản PCL nào trước đây. (Máy in: HP LaserJet 5, 5M và 5N)

## Tổng quan về PCL 6 ##

HP đã giới thiệu PCL 6 vào năm 1996, đây là bước phát triển tiếp theo của ngôn ngữ PCL và các công nghệ liên quan. Nó có các thành phần sau đây:

**PCL 6 Enhanced:** cung cấp phiên bản được tối ưu hóa để in từ giao diện đồ họa người dùng (GUIs) như MS Windows và OS/2

**PCL 6 Standard:** cung cấp khả năng tương thích ngược hoàn toàn với các máy in HP LaserJet trước đây

**Tổng hợp Phông chữ PCL:** cung cấp phông chữ có thể thay đổi quy mô, quản lý phông chữ và lưu trữ biểu mẫu cũng như phông chữ.

Phiên bản mở rộng PCL XL gần với GDI hơn mà nhiều ứng dụng sử dụng. Nó đảm bảo rằng ít bản dịch diễn ra hơn dẫn đến khả năng WYSIWYG tăng lên và hiệu suất tốt hơn với các ứng dụng hỗ trợ thoát do trình điều khiển Nâng cao triển khai. Đầu ra từ trình điều khiển Nâng cao (PCL XL) có thể không giống với đầu ra từ trình điều khiển Tiêu chuẩn. Nếu đầu ra không như mong đợi, hãy chọn trình điều khiển Tiêu chuẩn (PCL5e) để thay thế.

PCL 6 Các lệnh nâng cao được thiết kế để đáp ứng tối ưu các yêu cầu in đồ họa cho các ứng dụng dựa trên GUI. Trong hầu hết các trường hợp, đối với mọi lệnh in đồ họa mà GUI muốn thực hiện, sẽ có một lệnh PCL 6 Enhanced phù hợp. Điều này làm giảm số lệnh cần thiết để mô tả một trang đồ hoạ. Mỗi lệnh trong PCL 6 Enhanced được thiết kế để yêu cầu truyền dữ liệu tối thiểu từ PC chủ đến máy in. Điều này làm giảm lượng dữ liệu cần thiết để mô tả một trang.

Hệ thống In Windows cho hầu hết các máy in HP LaserJet cung cấp hai trình điều khiển riêng biệt: Tiêu chuẩn và Nâng cao. Trình điều khiển Tiêu chuẩn cung cấp khả năng tương thích ngược bằng cách sử dụng các lệnh PCL 6 Tiêu chuẩn (PCL5e) để in các trang văn bản đơn giản hoặc văn bản hỗn hợp và đồ họa. Trình điều khiển nâng cao sử dụng các lệnh PCL 6 nâng cao đã được tối ưu hóa để in các trang đồ họa phức tạp.

## Sửa đổi loại PCL 6 ##

#### Lớp 1.1 ####

**Công cụ vẽ:** Hỗ trợ vẽ các đường thẳng, cung/hình elip/cung, hình chữ nhật (tròn), hình đa giác, đường dẫn Bezier, đường dẫn được cắt bớt, hình ảnh raster, đường quét, thao tác raster.
**Xử lý màu:** Hỗ trợ bảng màu 1/4/8-bit, không gian màu RGB/xám. Hỗ trợ các mẫu bán sắc tùy chỉnh (tối đa 256 mẫu).
**Nén:** Hỗ trợ RLE.
**Đơn vị đo lường:** Inch, milimét, phần mười của milimét.
**Xử lý giấy:** Hỗ trợ các bộ loại giấy tùy chỉnh hoặc được xác định trước, bao gồm Letter thông thường, Legal, A4, v.v. Có thể chọn giấy từ nạp thủ công, khay, băng cassette. Giấy có thể được in hai mặt theo chiều ngang hoặc chiều dọc. Giấy có thể được định hướng theo hướng dọc, ngang hoặc xoay 180 độ của hai hướng trước.
**Phông chữ:** Hỗ trợ phông chữ bitmap hoặc TrueType, điểm mã 8 hoặc 16 bit. Việc chọn bộ ký tự sử dụng mã bộ ký hiệu khác với PCL 5. Khi sử dụng phông chữ bitmap, nhiều lệnh chia tỷ lệ sẽ không khả dụng. Khi phông chữ TrueType được sử dụng, các bộ mô tả độ dài thay đổi, các khối tiếp tục không được hỗ trợ. Phông chữ phác thảo có thể được xoay, thu nhỏ hoặc cắt.

#### Lớp 2.0 ####

**Nén:** Đã thêm một nén JPEG độc quyền được gọi là JetReady.
**Xử lý giấy:** Phương tiện có thể được chuyển hướng đến các ngăn giấy đầu ra khác nhau (tối đa 256). Đã thêm kích thước phương tiện cài sẵn A6 và B6 của Nhật Bản. Đã thêm cài đặt trước băng thứ ba, 248 nguồn phương tiện khay bên ngoài.
**Phông chữ:** Văn bản có thể được viết theo chiều dọc.

#### Lớp 2.1 ####

**Xử lý màu:** Đã thêm tính năng khớp màu.
**Nén:** Đã thêm Hàng Delta.
**Xử lý giấy:** Hướng, kích thước phương tiện là tùy chọn khi khai báo một trang mới. Đã thêm các loại giấy B5, JIS 8K, JIS 16K, JIS Exec.

#### Lớp 3.0 ####

**Xử lý màu:** Cho phép sử dụng các cài đặt bán sắc khác nhau cho đồ họa vector hoặc raster, văn bản. Hỗ trợ nửa tông màu thích ứng.
**Giao thức:** Hỗ trợ truyền qua PCL, cho phép các tính năng của PCL 5 được sử dụng bởi các luồng PCL 6. Tuy nhiên, một số trạng thái PCL 6 không được bảo toàn khi sử dụng tính năng này.
**Phông chữ:** Hỗ trợ phông chữ PCL.
**Trình xem/Trình chuyển đổi:** PCLReader (phần mềm miễn phí) có thể xem, chuyển đổi hoặc in bất kỳ cấp PCL 6 nào (bao gồm cả JetReady) sang bất kỳ máy in nào.

## Người giới thiệu ##

* [PCL - Theo Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)

