{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp PDB - Tệp cơ sở dữ liệu chương trình",
  "description":"Tìm hiểu về định dạng tệp PDB và API có thể tạo và mở tệp PDB.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Tệp PDB là gì?

Tệp có phần mở rộng .pdb là tệp cơ sở dữ liệu chương trình chứa thông tin gỡ lỗi cho tệp thực thi đã biên dịch (EXE/DLL). Các tệp PDB được tạo bởi Trình biên dịch Microsoft khi một chương trình ứng dụng được biên dịch ở chế độ gỡ lỗi. Sự hiện diện của tệp PDB có thể giúp kỹ thuật đảo ngược một tệp thực thi vì nó chứa thông tin quan trọng về tất cả các ký hiệu của mô-đun. Vì lý do này mà các tệp này được giữ tách biệt với tệp thực thi cuối cùng. [API DgbHelp] của Microsoft(https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) có thể mở tệp PDB để lấy thông tin như công khai và xuất khẩu, ký hiệu chung, ký hiệu cục bộ, nhập dữ liệu, tệp nguồn và số dòng.

## Định dạng tệp PDB

PDB là định dạng tệp độc quyền của Microsoft và chưa được ghi nhận chính thức ở bất kỳ đâu. Tuy nhiên, tài liệu bắt đầu có sẵn [tại đây](https://github.com/Microsoft/microsoft-pdb) và có thể được tham khảo.

### Luồng PDB

Các tệp PDB bao gồm nhiều luồng trong đó mỗi luồng hoạt động như một tệp riêng lẻ ảo và chứa thông tin. Người ghi tệp PDB có thể ghi vào các tệp này và tệp chỉ được hoàn thành sau khi một cam kết rõ ràng được đưa ra. Trình biên dịch có thể tiếp tục ghi vào tệp PDB nhưng chỉ cam kết nếu tất cả mã người dùng biên dịch thành công. Tệp PDB bao gồm các luồng sau:

|Số luồng |Nội dung |Mô tả ngắn|
---|---|---|
|1| Pdb (tiêu đề) |Thông tin phiên bản và thông tin để kết nối PDB này với EXE|
|2| Tpi (Trình quản lý kiểu) |Tất cả các kiểu được sử dụng trong tệp thực thi.|
|3| Dbi (Thông tin gỡ lỗi) |Giữ phần đóng góp của phần và danh sách 'Mods'|
|4| Bản đồ tên| Giữ một bảng chuỗi băm |
|4-(n+4)| n Mod's (Thông tin mô-đun)| Mỗi luồng Mod chứa các ký hiệu và số dòng cho một compiland|
|n+4| Băm ký hiệu toàn cầu| Một chỉ mục cho phép tìm kiếm trong các ký hiệu toàn cầu theo tên|
|n+5| Băm biểu tượng công cộng| Một chỉ mục cho phép tìm kiếm trong các biểu tượng công cộng theo địa chỉ|
|n+6| Bản ghi biểu tượng| Bản ghi biểu tượng thực tế của các biểu tượng toàn cầu và công cộng|
|n+7| Nhập băm | Hàm băm được sử dụng bởi luồng TPI.|

Mỗi luồng trong tệp PDB bao gồm một số trang không nhất thiết phải được đánh số liên tiếp.

### tiêu đề PDB

Tệp PDB tồn tại với Tiêu đề bao gồm chữ ký để xác định và xác thực định dạng cụ thể. Độ dài của chữ ký phụ thuộc vào định dạng PDB. Tiêu đề có thể dài hơn một trang.

### Siêu dữ liệu PDB
Siêu dữ liệu PDB chịu trách nhiệm nhận dạng tất cả các luồng thành phần, đưa ra độ dài và trình tự các trang cho mỗi luồng. Đơn đặt hàng được trao cho các luồng liên tiếp; bắt đầu bằng 0. Ngoài ra còn có một luồng gốc chưa được sắp xếp, chứa một số siêu dữ liệu.

## Người giới thiệu
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

