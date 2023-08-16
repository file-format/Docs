{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Định dạng tệp", "CAD", "Mở", "Tạo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp DWG và các API có thể tạo và mở tệp DWG.",
  "title" :"Định dạng tệp DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp DWG là gì?

Các tệp có phần mở rộng DWG đại diện cho các tệp nhị phân độc quyền được sử dụng để chứa dữ liệu thiết kế 2D và 3D. Giống như DXF, là các tệp ASCII, DWG đại diện cho định dạng tệp nhị phân cho các bản vẽ CAD (Thiết kế hỗ trợ máy tính). Nó chứa hình ảnh vector và siêu dữ liệu để thể hiện nội dung của tệp CAD. Có sẵn các trình xem miễn phí để xem các tệp DWG trên Hệ điều hành Windows, chẳng hạn như DWG TrueView miễn phí của Autodesk. Ngoài ra còn có các ứng dụng bên thứ ba khác hỗ trợ tiếp cận các tệp DWG. Các tệp DWG chứa thông tin do người dùng tạo và bao gồm:

* Kiểu dáng
* Dữ liệu hình học
* Bản đồ và hình ảnh

Định dạng này được sử dụng rộng rãi bởi các kiến trúc sư, kỹ sư và nhà thiết kế cho các mục đích thiết kế khác nhau.

## Lược Sử ##

Định dạng tệp DWG đã phát triển theo thời gian kể từ khi được giới thiệu chính thức vào năm 1982. Dưới đây là tổng quan ngắn gọn về các sự kiện trong quá khứ từ góc độ lịch sử.

**1982:** Autodesk đã cấp phép cho định dạng tệp DWG, được phát triển bởi Mike Riddle vào năm 1970, làm cơ sở cho AutoCAD.

**1998:** Với việc phát hành AutoCAD R14.01, Autodesk đã thêm tính năng xác minh tệp thông qua một chức năng có tên là DWGCHECK, chức năng này đã nhúng mã sản phẩm và tổng kiểm tra được mã hóa, được Autodesk gọi là WaterMark, vào các tệp DWG do chương trình tạo ra.

**2006:** Autodesk đã sửa đổi AutoCAD 2007, bao gồm "công nghệ TrustedDWG" để nhúng chuỗi văn bản "Autodesk DWG. Tệp này là DWG đáng tin cậy được lưu lần cuối bởi ứng dụng Autodesk hoặc ứng dụng được cấp phép Autodesk" vào tệp DWG. Mục đích của việc này là giúp người dùng phần mềm Autodesk đảm bảo rằng các tệp này được tạo bởi ứng dụng Autodesk hoặc RealDWG, điều này chắc chắn sẽ giúp giảm nguy cơ không tương thích.

## Cấu trúc tệp ##

DWG là một trong những định dạng tệp được sử dụng rộng rãi bởi nhiều ứng dụng và có cấu trúc tệp mạnh mẽ. Vì DWG là định dạng tệp nhị phân nên con người không thể đọc được nó như định dạng tệp ASCII [DXF](/vi/cad/dxf/) thuần túy. Các tệp DWG thường bao gồm thông tin về tọa độ hình ảnh và bất kỳ siêu dữ liệu nào được liên kết với nó. Toàn bộ [thông số kỹ thuật](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) của định dạng tệp DWG có sẵn để OpenDesign tải xuống. Cấu trúc tệp của định dạng tệp DWG được tóm tắt như sau.

**Tiêu đề**: Tiêu đề tệp bao gồm các biến Tiêu đề DWG và thông tin về Kiểm tra dự phòng theo chu kỳ (CRC) được sử dụng để phát hiện lỗi. Mỗi tiểu mục là một vectơ chuyên biệt trong đó các bit có độ dài khác nhau được sử dụng để biểu thị các nhãn khác nhau. Chẳng hạn, 6 bit đầu tiên của biến Tiêu đề DWG là viết tắt của chuỗi phiên bản.

**Định nghĩa lớp:** Tệp DWG có thể chứa nhiều lớp tùy thuộc vào mục đích cụ thể của tệp .dwg. Thông tin như kích thước siêu dữ liệu lớp của vùng dữ liệu lớp, số lớp và tổng kiểm tra ngoài những thông tin khác.

**Mẫu**: Đây là tùy chọn và đối với các phiên bản R15 và R15, phần này nằm bên dưới phần Không gian trống đối tượng.

**Đệm**: Siêu dữ liệu có thêm hậu tố và hậu tố với một số byte cụ thể giúp các phiên bản phần mềm AutoCAD cũ hơn tương thích chuyển tiếp với định dạng tệp DWG mới.

**Dữ liệu hình ảnh**: Siêu dữ liệu cho phần này phụ thuộc vào loại .dwg cụ thể. Đối với người dùng R14 và R15, phần này là tùy chọn.

**Dữ liệu đối tượng**: Dữ liệu đối tượng bao gồm danh sách đầy đủ các thực thể bảng, mục từ điển, v.v. tương ứng với danh sách đối tượng hiện có.

**Bản đồ đối tượng**: Vị trí của từng đối tượng trong tệp được chỉ định trong phần này của tệp. Hầu hết siêu dữ liệu trong phần này là các phần xử lý tệp đóng vai trò xác định và hiển thị lại đối tượng.

**Không gian trống đối tượng**: Phần này là tùy chọn cho tất cả người dùng

**Tiêu đề thứ hai**: Bản sao của phần tiêu đề tệp ở cuối tệp DWG

## Người giới thiệu ##

* [Thông số định dạng tệp DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [Đặc tả tệp DWG](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG - Theo Wikipedia](https://en.wikipedia.org/wiki/.dwg)

