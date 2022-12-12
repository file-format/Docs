{
  "date" : "2020-03-16",
  "keywords" :[ "Tệp IGES", "Định dạng tệp", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp IGES và API có thể tạo và mở tệp IGES.",
  "title" :"Định dạng tệp IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Tệp IGES là gì?

Tệp có phần mở rộng .iges được sử dụng để trao đổi thông tin thiết kế giữa các ứng dụng thiết kế có sự trợ giúp của máy tính (CAD). IGES là viết tắt của Thông số kỹ thuật trao đổi đồ họa ban đầu. Thông tin được trao đổi bằng IGES bao gồm sơ đồ mạch, khung dây, bề mặt dạng tự do hoặc các biểu diễn mô hình khối. IGES tìm thấy các ứng dụng của nó trong các bản vẽ kỹ thuật truyền thống, phân tích mô hình và chức năng sản xuất. Định dạng có thể trao đổi cả thông tin thiết kế 2D hoặc 3D giữa các chương trình CAD. Các tệp IGES có thể được mở bằng một số ứng dụng CAD như Autodesk và CADSoftTools ABViewer. Ngoài ra còn có một số API có sẵn để mở và chuyển đổi các tệp IGES theo chương trình.

## Định dạng tệp IGES

Các tệp IGES ở định dạng văn bản ASCII và có thể được mở trong bất kỳ trình soạn thảo văn bản nào để xem nội dung của tệp. Thông tin văn bản trong tệp IGES được thể hiện ở định dạng "Hollerith". Một tệp IGES phổ biến có thể chứa hàng nghìn dòng để biểu thị thông tin 2D hoặc 3D có thể được trao đổi theo định dạng này. Tệp IGES được chia thành năm phần, được biểu thị bằng chữ in hoa cụ thể trong cột thứ 73. Các phần đó là các phần `Bắt đầu` (S), `Toàn cầu` (G), `Nhập dữ liệu` (D), `Dữ liệu tham số` (P) và `Kết thúc` (T). Phần Nhập dữ liệu và Dữ liệu tham số thường được viết tắt lần lượt là DE và PD.

### Tiêu đề tệp IGES

Phần Bắt đầu và Toàn cầu chứa thông tin cơ bản về:
* Tên của tập tin và nguồn của nó
* Dấu phân cách cho phần Dữ liệu tham số
* Tác giả của tập tin, và các thông tin chung khác.

Các phần Bắt đầu và Toàn cầu từ tài liệu mẫu trên Wikipedia như sau.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Như có thể thấy, trường bắt đầu chứa các mô tả tệp có thể đọc được của con người và của tôi có bất kỳ ký tự nào trong cột 1-72, với dòng kết thúc bằng tiêu đề phần và số dòng phần. Phải có ít nhất 1 dòng của phần Bắt đầu. Phần toàn cầu chứa dữ liệu tiền xử lý. Nó cũng phải có trong tệp và kết thúc bằng định dạng G000000#.

### Phần Nhập dữ liệu (DE) và Dữ liệu tham số (PD)

#### Phần nhập liệu
Tệp IGES bao gồm một số thực thể chứa thông tin về dữ liệu cơ bản của định dạng tệp IGES. Một thực thể chứa thông tin về các thành phần khác nhau của định dạng dữ liệu IGES và được sử dụng để vẽ. Các thực thể được sử dụng phổ biến hơn bao gồm:
* Cung tròn
* Đường cong tổng hợp
* Cung hình nón
* Chiếc máy bay
* Hàng

Đây chỉ là một số và có khoảng 150 thực thể khác nhau trong IGES. Mỗi thực thể được xác định bởi một số Loại, chẳng hạn như:
* VÒNG CUNG (Loại 100)
* DÒNG (Loại 110)

##### Thuộc tính thực thể

Mỗi thực thể được khai báo có các thuộc tính sau.

|Tên trường|Mô tả|
---|---|
|Loại thực thể |Đây là loại thực thể được mô tả. Ví dụ: 116 mô tả một thực thể Điểm.|
|Con trỏ PD |Điều này cung cấp vị trí cho dữ liệu thực thể này trong phần Dữ liệu tham số. Vị trí này chỉ đơn giản là số dòng bên trong phần PD có dòng đầu tiên của dữ liệu thực thể này.|
|Structure |Zero hoặc con trỏ tới thực thể định nghĩa. Không áp dụng cho hầu hết các thực thể|
|Mẫu phông chữ Line| Số hoặc con trỏ tới thực thể mẫu phông chữ dòng. Số biểu thị: * 0 Không có mẫu được chỉ định (mặc định) * 1 Nét liền * 2 Nét đứt * 3 Bóng mờ * 4 Đường tâm * 5 Nét chấm|
|Cấp| Chỉ định các cấp được liên kết với thực thể này. Cho phép thực thể xuất hiện trên nhiều cấp độ|
|Xem| Chỉ định các tùy chọn xem. Đó là: 0 Cho biết khả năng hiển thị và đặc điểm như nhau trong tất cả các chế độ xem. Con trỏ mặc định tới thực thể Dạng xem (Loại 410) mà nó có thể được xem từ Tham chiếu một thực thể Liên kết có thể nhìn thấy dạng xem (Loại 402, Biểu mẫu 3)
|Con trỏ ma trận biến đổi| Tham chiếu một thực thể ma trận chuyển đổi (Loại 124) hoặc bằng 0 theo mặc định (không chuyển đổi)|
|Hiệp hội Hiển thị Nhãn| Tham chiếu Liên kết Hiển thị Nhãn (Loại 402, Biểu mẫu 5) xác định cách nhãn thực thể xuất hiện.|
|Số trạng thái| Chứa bốn phần của hai số. 1-2: Trạng thái trống. 00 cho bình thường hoặc 01 cho trống. 3-4: Công tắc thực thể cấp dưới: là 00 cho độc lập, 01 cho phụ thuộc vật lý, 02 cho phụ thuộc logic và 03 cho cả hai. 5-6: Cờ sử dụng thực thể: là 00 cho Hình học, 01 cho chú thích, 02 cho định nghĩa, 03 cho Khác, 04 cho Lôgic, 05 cho tham số 2D và 06 cho Hình học xây dựng. Cuối cùng, 7-8 là hệ thống phân cấp, trong đó 00 biểu thị toàn cầu từ trên xuống (sử dụng các đặc điểm của thực thể này), 01 là trì hoãn toàn cầu (không sử dụng các đặc điểm của thực thể này) và 02 là sử dụng thuộc tính phân cấp (sử dụng Thực thể phân cấp (Loại 406, Biểu mẫu 10)để xác định các đặc điểm của nhóm phân cấp).|
|Số thứ tự| Được chỉ định bởi D#, trong đó # là số dòng cho phần này (không phải từ đầu tệp). Điều này cũng được sử dụng để trỏ đến thực thể Nhập dữ liệu này.|
|Loại thực thể| nó được chỉ định hai lần cho mỗi danh sách thực thể|
|Số Trọng lượng Dòng| Chỉ định độ dày khi hiển thị thực thể. Nhỏ nhất là 1, 0 là mặc định|
|Số Màu| Chỉ định màu thực thể. Các giá trị số nguyên được phép là: 0 Không có màu (mặc định) 1 Đen 2 Đỏ 3 Lục 4 Lam 5 Vàng 6 Đỏ tươi 7 Lục lam 8 Trắng|
|Số đếm dòng tham số| Chỉ định số lượng dòng mà thực thể này chiếm trong Phần Dữ liệu Tham số|
|Mẫu số| Cho biết biểu mẫu hoặc biểu diễn của thực thể này. Thay đổi cách diễn giải dữ liệu tham số. Mặc định là 0|
|Trường dành riêng| Không sử dụng|
|Trường dành riêng| Không sử dụng|
|Nhãn thực thể| Số nhận dạng được chỉ định của ứng dụng- chứng minh đúng|
|Số đăng ký| Hạn định số cho nhãn thực thể. Cả hai cùng nhau tạo thành một mã định danh duy nhất cho thực thể|
|Số thứ tự Xem ở trên. |Đây sẽ là D#+1, vì mỗi thực thể được chỉ định trên hai dòng.|

#### Phần dữ liệu tham số
Phần Mục nhập dữ liệu được theo sau bởi phần Dữ liệu tham số. Nó liệt kê dữ liệu cho từng mục nhập tương ứng và liệt kê các tham số cho thực thể dựa trên các dấu phân cách được chỉ định trong phần Toàn cầu (thường là dấu phẩy để phân tách các tham số và dấu chấm phẩy để kết thúc danh sách).


## Người giới thiệu
* [IGES của WikiPedia](https://en.wikipedia.org/wiki/IGES)

