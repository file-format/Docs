{
  "date" : "2020-03-16",
  "keywords" :[ "Tệp DXF", "Định dạng tệp", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp DXF và các API có thể tạo và mở tệp DXF.",
  "title" :"Định dạng tệp DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp DXF là gì?

DXF, Định dạng trao đổi bản vẽ hoặc Định dạng trao đổi bản vẽ, là biểu diễn dữ liệu được gắn thẻ của tệp bản vẽ AutoCAD. Mỗi phần tử trong tệp có một số nguyên tiền tố được gọi là mã nhóm. Mã nhóm này thực sự đại diện cho phần tử theo sau và cho biết ý nghĩa của phần tử dữ liệu đối với một loại đối tượng nhất định. DXF cho phép thể hiện hầu hết tất cả thông tin do người dùng chỉ định trong một tệp bản vẽ.

Định dạng tệp DXF được Autodesk phát triển dưới dạng định dạng tệp dữ liệu CAD cho khả năng tương tác dữ liệu giữa AutoCAD và các ứng dụng khác. Do đó, dữ liệu có thể được nhập từ các định dạng khác sang DXF sang AutoCAD theo thông số kỹ thuật về khả năng tương tác của định dạng tệp DXF.

## Lược Sử ##


Lịch sử của định dạng tệp DXF bắt đầu từ năm 1982 khi nó được giới thiệu như một phần của AutoCAD 1.0. Các phiên bản đầu tiên của AutoCAD chỉ hỗ trợ định dạng tệp ASCII của DXF. Với phiên bản 10 của AutoCAD (và cao hơn) vào năm 1988, hỗ trợ cho cả ASCII cũng như định dạng tệp DXF nhị phân đã được giới thiệu trong AutoCAD. Trong các giai đoạn trước, Autodesk không chia sẻ bất kỳ thông số định dạng tệp nào và do đó, việc nhập chính xác các tệp DXF không dễ dàng. Tuy nhiên, Autodesk hiện đã xuất bản các thông số kỹ thuật của DXF và có sẵn cho công chúng.

## Thông số kỹ thuật định dạng tệp ##

Định dạng tệp DXF sử dụng mã nhóm và các cặp giá trị để sắp xếp nội dung thành các phần. Mỗi phần bao gồm các bản ghi trong đó mỗi bản ghi bao gồm một mã nhóm và mục dữ liệu. Mỗi mã nhóm và giá trị nằm trên dòng riêng của chúng trong tệp DXF. Mỗi phần bắt đầu bằng một mã nhóm 0 theo sau là chuỗi, PHẦN. Tiếp theo là mã nhóm 2 và một chuỗi cho biết tên của phần (ví dụ: PHẦN 1). Mỗi phần bao gồm các mã nhóm và giá trị xác định các thành phần của nó. Phần kết thúc bằng số 0 theo sau là chuỗi ENDSEC.

Định dạng tệp DXF coi các đối tượng khác với các thực thể. Các đối tượng không có biểu diễn đồ họa ở đây nhưng các thực thể có nó. Do đó, các mục trong DXF được gọi là đối tượng đồ họa trong khi đối tượng đối tượng được gọi là đối tượng phi đồ họa. Phần BLOCK và ENTITIES của tệp DXF chứa các Thực thể và việc sử dụng mã nhóm trong hai phần này giống hệt nhau. Kết thúc một thực thể được biểu thị bằng nhóm 0 tiếp theo, bắt đầu thực thể tiếp theo hoặc biểu thị kết thúc phần.

### Cấu trúc tệp ###

Các phần trong tệp DXF được sắp xếp theo thứ tự sau:

|Phần|Mô tả cơ bản
---|---|
|Header|Phần này chứa thông tin chung về bản vẽ. Nó giống như chức năng Cài đặt trong điện thoại của bạn, chứa các biến khác nhau được liên kết với bản vẽ và các giá trị được liên kết của nó. Ví dụ: phần Header sẽ xác định phiên bản AutoCAD mà tệp DXF sử dụng (biến $ACADVER) hoặc đơn vị được sử dụng để đo các góc trong tệp (biến $AUNITS)
|Lớp|Phần LỚP chứa thông tin về các lớp do ứng dụng định nghĩa có các thể hiện xuất hiện trong các phần KHỐI, THỰC THỂ và ĐỐI TƯỢNG của cơ sở dữ liệu.
|Bảng|Phần này chứa các định nghĩa cho một số bảng khác nhau, mỗi bảng chứa một số mục ký hiệu khác nhau. Ví dụ: [loại đường kẻ](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A- 847B-5BBE36EC6FDF-htm.html) bảng (LTYPE) xác định mẫu dấu gạch ngang, dấu chấm, văn bản và ký hiệu trong tệp DXF cũng như cách chúng được chia tỷ lệ. Dưới đây là danh sách đầy đủ các bảng được tìm thấy trong phần này:<ul><li> Bảng ID ứng dụng (APPID)</li><li> Bảng ghi khối (BLOCK_RECORD)</li><li> Bảng Kiểu kích thước (DIMSTYPE)</li><li> Bảng lớp (LAYER)</li><li> Bảng loại đường kẻ (LTYPE)</li><li> Bảng kiểu văn bản (STYLE)</li><li> Bảng hệ thống tọa độ người dùng (UCS)</li><li> Xem (VIEW) bảng</li><li> Bảng cấu hình khung nhìn (VPORT)</li></ul>
|Khối|Phần này chứa các đối tượng đồ họa và các thực thể vẽ tạo nên mỗi tham chiếu khối trong bản vẽ.
|Thực thể|Phần này chứa dữ liệu đối tượng thực tế và các thực thể đồ họa của bản vẽ. Điều này có thể bao gồm dữ liệu thô – ví dụ: một thực thể hình tròn được xác định bởi độ dày, tâm, bán kính và hướng đùn của nó.
|Đối tượng|Ở đây, bạn sẽ tìm thấy các phần phi đồ họa của bản vẽ. Ví dụ, từ điển AutoCAD được lưu trữ ở đây.

## Người giới thiệu ##

* [Thông số tệp DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF của Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

