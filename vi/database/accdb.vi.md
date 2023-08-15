{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp ACCDB và API có thể tạo và mở tệp ACCDB.",
  "title" :"Định dạng tệp ACCDB - Tệp cơ sở dữ liệu Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Tệp ACCDB là gì?

Tệp có phần mở rộng .accdb là tệp cơ sở dữ liệu Microsoft Access 2007 lưu trữ dữ liệu người dùng trong bảng. Nó hỗ trợ lưu trữ
biểu mẫu tùy chỉnh, truy vấn SQL và dữ liệu khác. Các tệp ACCDB đã thay thế các tệp [MDB](/vi/database/mdb/) sau khi Microsoft chuyển sang cấu trúc tệp dựa trên XML. Các tệp ACCDB vẫn có thể được chuyển đổi sang MDB với khả năng tương thích cũ. Tuy nhiên, ACCDB là định dạng tệp cơ sở dữ liệu Access được sử dụng rộng rãi hiện nay. Microsoft cũng hỗ trợ các tính năng bổ sung ở định dạng ACCDB, chẳng hạn như khả năng lưu trữ tệp đính kèm, dữ liệu nhị phân và hỗ trợ trường đa giá trị.

## Định dạng tệp ACCDB

Giống như MDB, không có thông số kỹ thuật công khai nào dành cho định dạng tệp ACCDB. Microsoft hỗ trợ truy cập các tệp này theo chương trình thông qua tiêu chuẩn Kết nối Cơ sở dữ liệu Mở (ODBC) và Visual Basic for Applications (VBA).

### Một cái nhìn sâu sắc

Kết xuất hex của tệp ACCDB đơn giản gợi ý rằng có những điểm tương đồng chung về cấu trúc với các phiên bản mới nhất của Dòng định dạng MDB tiền nhiệm. Cả hai định dạng tệp đều sử dụng kích thước trang cố định là 4096 byte. Một điểm tương đồng khác giữa ACCDB và MDB là dạng số ma thuật, bao gồm chuỗi "ACE DB tiêu chuẩn" cho ACCDB. Phiên bản hoặc mã tương thích ở cùng một vị trí ở cả hai định dạng. mdbtools | Tệp HACKING nêu rõ "Offset 0x14 chứa phiên bản Jet của cơ sở dữ liệu này" và Hướng dẫn MDB không chính thức đồng tình. Thông tin trong các nguồn này, kết hợp với mục nhập Wikipedia cho [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), gợi ý rằng giá trị 0x02 biểu thị ACE 12 (Access 2007) và 0x03 biểu thị ACE 14 (Truy cập 2010). Tuy nhiên, cơ sở dữ liệu tối thiểu được tạo trong Access 2010 và cơ sở dữ liệu tương tự được tạo trong Access 2016 đều có 0x02 ở vị trí này. Cơ sở dữ liệu tối thiểu được tạo trong Access 2016, nhưng xác định một cột có kiểu dữ liệu "số nguyên lớn" mới được giới thiệu, có giá trị là 0x05. Trong các tệp ACCDB, chỉ báo này xuất hiện để phản ánh khả năng tương thích của tệp chứ không phải phiên bản của công cụ ACE được sử dụng để tạo tệp.

## Người giới thiệu

* [Định dạng tệp truy cập](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
* [Thông số kỹ thuật Access 2016](https://support.microsoft.com/en-us/office/access-specations-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Công cụ cơ sở dữ liệu Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Tôi nên sử dụng định dạng tệp Access nào?](https://support.microsoft.com/en-us/office/which-access-file-format-nên-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
