{
  "date" : "2020-08-20",
  "keywords" :[ "tệp woff", "định dạng tệp woff", "tệp woff là gì", "tệp", "ví dụ woff", "phần mở rộng tệp woff","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Định dạng tệp mở trên web",
  "linktitle" : "WOFF",
  "linktitle" : "WOFF",
  "menu" : {
      "parent" : "font"
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Tệp WOFF là gì?

Tệp có phần mở rộng .woff là tệp phông chữ web dựa trên Định dạng phông chữ mở trên web (WOFF). Nó có bộ chứa nén dành riêng cho định dạng dựa trên các loại phông chữ TrueType (.TTF) hoặc OpenType (.OTT). WOFF được giới thiệu với mục đích phân biệt các phông chữ web với các tệp phông chữ được sử dụng trong các ứng dụng dành cho máy tính để bàn. Ngoài ra, định dạng được nhắm mục tiêu để giảm độ trễ khi truyền phông chữ từ máy chủ sang máy tính của khách hàng qua mạng. Một số công cụ có sẵn có thể chuyển đổi các tệp WOFF sang TTF và các định dạng tệp phông chữ khác.

## **Định dạng tệp WOFF**

Định dạng phông chữ WOFF nén bảng dữ liệu phông chữ của các cấu trúc sfnt dựa trên bảng được sử dụng trong các loại phông chữ khác nhau như TrueType, OpenType và Định dạng phông chữ mở. Nó giống như một vùng chứa cho các loại phông chữ này và cũng có chỗ để bao gồm siêu dữ liệu của phông chữ và dữ liệu sử dụng cá nhân được đưa vào vùng chứa. Bộ chuyển đổi sử dụng tệp sfnt thành tệp có định dạng WOFF và tác nhân người dùng khôi phục tệp được mã hóa để sử dụng với tài liệu web. Cần lưu ý rằng dữ liệu phông chữ được khôi phục hoàn toàn khớp với định dạng phông chữ đầu vào từ mọi khía cạnh.

Tệp WOFF Các tiện ích thường chứa các tính năng bổ sung như cài đặt con glyph, xác thực hoặc bổ sung tính năng phông chữ nhưng không cần thiết. Cả tác nhân tạo và tác nhân sử dụng phải đảm bảo rằng tính hợp lệ của dữ liệu phông chữ cơ bản được giữ nguyên.

### Cấu trúc tệp WOFF

Cấu trúc tệp WOFF tương tự như cấu trúc của phông chữ sfnt. Nó dựa trên một thư mục bảng chứa độ dài và độ lệch cho mỗi bảng dữ liệu phông chữ. Tất cả các bảng được theo sau thông tin ban đầu này. Tệp chứa cơ sở dữ liệu phông chữ giống như trong các phông chữ gốc. Thứ tự của các bảng cũng giống nhau nhưng mỗi bảng có thể được nén. Mặc dù vậy, thư mục bảng WOFF thay thế thư mục bảng gốc.

Một tệp WOFF bao gồm:

* WOFFHeader - Tiêu đề tệp có loại và phiên bản phông chữ cơ bản, cùng với phần bù cho siêu dữ liệu và khối dữ liệu riêng tư.
* TableDirectory - Thư mục chứa các bảng phông chữ, cho biết kích thước gốc, kích thước nén và vị trí của từng bảng bên trong tệp WOFF.
* FontTables - Các bảng dữ liệu phông chữ từ phông chữ sfnt đầu vào, được nén để giảm yêu cầu băng thông.
* Siêu dữ liệu mở rộng - Một khối siêu dữ liệu mở rộng tùy chọn, được trình bày ở định dạng XML và được nén để lưu trữ trong tệp WOFF.
* PrivateData- Khối dữ liệu riêng tư tùy chọn dành cho nhà thiết kế phông chữ, xưởng đúc hoặc nhà cung cấp sử dụng.

### Tiêu đề WOFF
Tiêu đề WOFF bao gồm một chữ ký xác định cho biết loại dữ liệu có trong tệp. Tiêu đề WOFF cùng với các trường của nó như sau.

|Loại|Tên trường|Mô tả|
---|---|---|
|UInt32|chữ ký |0x774F4646 'wOFF' |
|UInt32| hương vị |"Phiên bản sfnt" của phông chữ đầu vào.|
|UInt32| chiều dài |Tổng kích thước của tệp WOFF.|
|UInt16| numTables |Số mục trong thư mục của bảng phông chữ.|
|UInt16| dành riêng |dành riêng; đặt thành 0.|
|UInt32| totalSfntSize |Tổng kích thước cần thiết cho dữ liệu phông chữ không nén, bao gồm tiêu đề sfnt, thư mục và bảng phông chữ (bao gồm cả phần đệm).|
|UInt16| majorVersion |Phiên bản chính của tệp WOFF.|
|UInt16| minorVersion |Phiên bản nhỏ của tệp WOFF.|
|UInt32| metaOffset |Bù sang khối siêu dữ liệu, từ đầu tệp WOFF.|
|UInt32| metaLength |Độ dài của khối siêu dữ liệu được nén.|
|UInt32| metaOrigLength |Kích thước không nén của khối siêu dữ liệu.|
|UInt32| privOffset |Bù sang khối dữ liệu riêng tư, từ đầu tệp WOFF.|
|UInt32| privLength |Độ dài của khối dữ liệu riêng tư.|


## **Người giới thiệu**
* [Định dạng tệp w3 WOFF](https://www.w3.org/TR/WOFF/)

