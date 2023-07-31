{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Bố cục trang báo cáo",
  "keywords" :[ "rpl", "Bố cục trang báo cáo", "XSD", "Máy chủ SQL", "báo cáo"],
  "description":"Tìm hiểu về định dạng luồng RPL là định dạng nhị phân nội bộ được Dịch vụ báo cáo của Microsoft SQL Server sử dụng khi liên hệ với các điều khiển của trình xem.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Tệp RPL là gì? ##

Định dạng luồng RPL (Bố cục trang báo cáo) là định dạng nhị phân nội bộ được Dịch vụ báo cáo của MS SQL Server sử dụng khi liên hệ với các điều khiển trình xem để giảm bớt một số công việc hiển thị từ máy chủ sang điều khiển trình xem của máy khách. Nhà phát triển có thể tạo trình thiết kế báo cáo tùy chỉnh bằng cách sử dụng RPL, RPL sẽ tạo RPL cũng như trình kết xuất báo cáo tùy chỉnh xử lý và hiển thị tệp RPL để hiển thị báo cáo.

## Cấu trúc RPL

Luồng RPL bao gồm cấu trúc luồng, cấu trúc báo cáo, thuộc tính báo cáo và liệt kê. Mỗi cấu trúc bao gồm những điều sau đây:

- Một định nghĩa của cấu trúc.

- Ngữ pháp Augmented Backus-Naur Form (ABNF) cho cấu trúc.

- Một sơ đồ bit của cấu trúc.

- Định nghĩa của tất cả các trường có trong cấu trúc.

Dưới đây là những lưu ý ngắn gọn về một số Cấu trúc RPL:

### Cấu trúc luồng
Cấu trúc luồng bao gồm một loạt các bản ghi. Một bản ghi không chứa hoặc nhiều trường có cấu trúc chứa bố cục báo cáo.

#### Luồng RPL
Luồng RPL phải chỉ có một bản ghi Báo cáo và luồng phải là một chuỗi các bản ghi nhị phân giữ cấu trúc phân cấp báo cáo.

#### Ghi lại
Bản ghi là một khối xây dựng cơ bản được sử dụng để lưu giữ thông tin về một báo cáo. Một bản ghi bao gồm một chuỗi byte có độ dài khác nhau. Một bản ghi bao gồm hai thành phần:
- Một loại bản ghi
- Dữ liệu bản ghi dành riêng cho loại bản ghi đó.
Loại bản ghi là một byte xác định loại thông tin nào được chỉ định bởi bản ghi và cấu trúc của dữ liệu bản ghi liên quan đến bản ghi được sắp xếp và cấu trúc như thế nào. Giá trị bản ghi phụ thuộc vào loại dữ liệu dành riêng cho bản ghi đó.

#### Cấu trúc kiểu dữ liệu đơn giản

Bảng sau đây xác định các loại dữ liệu trong luồng RPL.

|Mô tả| định dạng|
---|---|
|Char|Biểu thị giá trị số (thứ tự) 16 bit (2 byte).|
|Byte|Biểu thị một số nguyên không dấu 8 bit (1 byte).|
|Int16|Đại diện cho số nguyên có dấu 16 bit (2 byte).|
|Single|Đại diện cho giá trị dấu phẩy động có độ chính xác đơn 32 bit (4 byte).|
|Số thập phân|Đại diện cho loại dữ liệu 128 bit (16 byte).|
|DateTime|Đại diện cho mã hóa 64 bit (8 byte) của giá trị ngày và giờ.|
|Int64|Đại diện cho một số nguyên có dấu 64 bit (8 byte).|
|Int32|Đại diện cho số nguyên có dấu 32 bit (4 byte).|
|Float|Đại diện cho giá trị dấu phẩy động có độ chính xác đơn 32 bit (4 byte).|
|Boolean|Đại diện cho một giá trị kiểu Boolean logic 8 bit (1 byte). Các giá trị hợp lệ là đúng (1) và sai (0).|
|Dài|Đại diện cho số nguyên có dấu 64 bit (8 byte).|
|Chuỗi|Tất cả các giá trị Chuỗi trong giao thức PHẢI là UNICODE UTF-16. Theo mặc định, tất cả các giá trị Chuỗi bắt đầu bằng một số nguyên xác định độ dài của Chuỗi. Các giá trị chuỗi được biểu diễn trong giao thức dưới dạng một mảng byte; số byte PHẢI bằng số ký tự trong Chuỗi nhân với hai.|

### Cấu trúc báo cáo
Các cấu trúc báo cáo bao gồm các định nghĩa và kích thước của các cấu trúc và thành phần có liên quan của chúng.

Danh sách sau chỉ định cấu trúc báo cáo:

- Báo cáo
- Phiên bản
- Thuộc tính báo cáo
- Phần tử mảng bù đắp
- Nội dung trang
- Trang
- Thuộc tính trang
- Bố trí trang
- Tiết diện
- Phần đơn giản
- Phần hỗn hợp
- Thuộc tính phần
- Phần tử diện tích cơ thể
- Phần tử tiêu đề trang
- Phần tử chân trang
- Yếu tố cơ thể
- Thuộc tính phần tử
- Thuộc tính phần tử được chia sẻ
- Sử dụng thuộc tính phần tử được chia sẻ
- InlineSharedElementProperties
- NonSharedElementProperties
- Phong cách
- SharedStyleProperties
- NonSharedStyleProperties
- Thông tin hành động
- Nội dung thông tin hành động
- Hoạt động
- ActionImageMapArea
- ActionInfoWithMaps
-Dữ liệu hình ảnh động
- ImageConsolidationOffsets
- Mục báo cáo
- Hàng
- Hình ảnh
- ImageDataProperties
- Sử dụngSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- Dữ liệu hình ảnh
- ImageMapArea
- ImageMapArea
- Đồ thị
- Bảng đo
- Bản đồ
- Hình chữ nhật
- Báo cáo phụ
- RichTextBox
- Đoạn Nội dung
- TextRun
- Đoạn văn
- Cấu trúc RichTextBox
- Tablix
- Nội dung Tablix
- Cấu trúc Tablix
- TablixĐo lường
- CộtWidths
- Thông tin cột
- RowHeights
- RowInfo
- TablixRow
- TablixRowCell
- Góc Tablix
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Đo
- Đo đạc
- Báo cáoElementEnd

### Đặc tính
Sau đây là danh sách các thuộc tính có thể được sử dụng trong Luồng RPL:

- TÔI
- Số cột
- Khoảng cách cột
- Tên duy nhất
- Tên
- Nhãn mác
- Dấu trang
- Mẹo công cụ
- Chuyển đổi mục
- Sự mô tả
- Địa điểm
- Tiêu dùngContainerWhiteSpace (RPL 10.6)
- Ngôn ngữ
- Thời gian thực hiện
- Tác giả
- Tự động làm mới
- Tên báo cáo
- Chiều cao trang
- Chiều rộng trang
- Ký quỹ
- MarginLeft
- MarginRight
- Ký quỹ Đáy
- Cột
- Tên trang (RPL 10.6)
- Xiên
- Có thể phát triển
- Có thể thu nhỏ
- Giá trị
- ToggleState
- Có thểSắp xếp
- SortState
- Công thức
- IsToggleParent
- Loại Mã
- Giá trị gốc
- Thì đơn giản
- Bù đắp nội dung
- Tên dòng
- Định cỡ
- Liên kết với con
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- Xử lýWithError
- Hình ảnhMIMEType
- Tên Hình ảnh
- Bề rộng
- Chiều cao
- Độ phân giải ngang
- Độ phân giải dọc
- Định dạng thô
- Siêu liên kết
- Liên kết đánh dấu
- DrillthroughId
- DrillthroughUrl
- Màu viền
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- Kiểu viền
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- Chiều rộng biên giới
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- PaddingLeft
- Đệm phải
- Đệm hàng đầu
- ĐệmBên dưới
- Kiểu chữ
- Phông chữGia đình
- Cỡ chữ
- Trọng lượng phông chữ
- Định dạng
- Trang trí văn bản
- Căn chỉnh văn bản
- Căn dọc
- Màu sắc
- Chiều cao giữa các dòng
- Hướng đi
- Chế độ viết
- UnicodeBiDi
- Hình nền
- Màu nền
- Bối cảnh Lặp lại
- Ngôn ngữ số
- Biến thể số
- Lịch
- CộtHeaderRows
- RowHeaderCột
- Cols BeforeRowHeader
- Bố cụcDirection
- Định nghĩaPath
- Mức độ
- MemberCell Index
- CellItemOffset
- ColSpan
- RowSpan
- Chỉ số xác định
- Cột Index
- Row Index
-Nhãn nhóm
- Đệ quyToggleLevel
- Kiểu danh sách
- Cấp danh sách
- Đoạn Số
- Thụt lề phải
- Thụt lề trái
- Treo thụt lề
- Không gian trước
- Không gian sau
- Dòng đầu tiên
- đánh dấu
- Nội dung Đầu trang
- Nội dung còn lại
- Chiều rộng nội dung
- Chiều cao nội dung
- Tiểu bang
- CellItemState
- MemberDefState

### Bảng liệt kê
Danh sách sau đây hiển thị các liệt kê có thể được sử dụng trong luồng RPL:

- Tùy chọn sắp xếp
- Định cỡ
- Kiểu hình
- ImageRawFormat
- Kiểu chữ
- Trọng lượng phông chữ
- Trang trí văn bản
- Căn chỉnh văn bản
- Căn dọc
- Hướng
- Chế độ viết
- UnicodeBiDiTypes
- Lịch
- Kiểu viền
- BackgroundRepeatTypes
- Kiểu danh sách
- Kiểu đánh dấu
- Loại Mã
- StateValues
- Giá trị TablixMemberState
- TablixMemberDefStateValues
- Kích thước RPLS





## Người giới thiệu ##

- [Định dạng luồng nhị phân Bố cục trang báo cáo (RPL)](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

