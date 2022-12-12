{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "cơ bản" ],
  "description":"Định dạng Tài liệu Di động (PDF) là biểu diễn tiêu chuẩn của tài liệu độc lập với phần mềm, phần cứng và HĐH. Các tiêu chuẩn PDF bao gồm PDF/A, PDF/E, PDF/UA, PDF/VT và PDF/X.",
  "title" :"Định dạng tệp PDF - Tệp PDF là gì?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Định dạng Tài liệu Di động (PDF) là một loại tài liệu được Adobe tạo ra vào những năm 1990. Mục đích của định dạng tệp này là giới thiệu một tiêu chuẩn để trình bày tài liệu và tài liệu tham khảo khác ở định dạng độc lập với phần mềm ứng dụng, phần cứng cũng như Hệ điều hành. Định dạng tệp PDF có đầy đủ khả năng chứa thông tin như văn bản, hình ảnh, siêu liên kết, trường biểu mẫu, đa phương tiện, chữ ký số, tệp đính kèm, siêu dữ liệu, tính năng Không gian địa lý và đối tượng 3D trong đó có thể trở thành một phần của tài liệu nguồn.

Trong hầu hết các trường hợp, tài liệu hiện có được chuyển đổi thành PDF thay vì tạo PDF mới từ đầu. Nhưng điều đó không có nghĩa là không có phần mềm để tạo hoặc thao tác với các tệp PDF.

**(Phải chia sẻ điều gì đó về định dạng tệp PDF? Bạn có thể đăng phát hiện của mình trong phần [Tin tức về định dạng tệp PDF](https://news.fileformat.com/t/PDF).)**

## Định dạng tệp PDF - Lược sử

Xem nhanh dòng thời gian về quá trình hình thành tệp PDF theo dòng thời gian như sau:

**1993** - Adobe Systems cung cấp miễn phí các thông số kỹ thuật PDF

**2008** - PDF được phát hành dưới dạng tiêu chuẩn mở vào ngày 1 tháng 7 năm 2008 và được Tổ chức Tiêu chuẩn hóa Quốc tế xuất bản dưới dạng **ISO 32000-1:2008**.

**2008** - Adobe đã xuất bản Giấy phép Bằng sáng chế Công cộng cho định dạng ISO 32000-1, các quyền miễn phí bản quyền đối với tất cả các bằng sáng chế thuộc sở hữu của Adobe cần thiết để tạo, sử dụng, bán và phân phối các triển khai tuân thủ PDF.

Phiên bản đầu tiên của PDF được chỉ định là PDF 1.0, sau đó đã trải qua các lần sửa đổi cho đến PDF 1.7. PDF 1.7, đã trở thành ISO 32000-1, bao gồm một số công nghệ độc quyền không được tiêu chuẩn hóa cũng như Adobe XML Forms Architecture (XFA) và phần mở rộng JavaScript cho Acrobat. Đó là vào ngày 28 tháng 7 năm 2017 khi PDF 2.0, được gọi là ISO 32000-2:2017, không bao gồm bất kỳ công nghệ phi tiêu chuẩn nào được xuất bản.

## Thông số kỹ thuật định dạng tệp PDF

Tệp PDF là một tập hợp các byte có thể được nhóm thành các mã thông báo theo quy tắc cú pháp được xác định bởi thông số kỹ thuật PDF. Một khi hoặc nhiều mã thông báo được kết hợp để tạo thành các thực thể cú pháp cấp cao hơn, chủ yếu là các đối tượng, là các giá trị dữ liệu cơ bản mà tài liệu PDF được tạo từ đó.

### Cấu trúc tệp của tệp PDF

Nội dung tệp PDF được sắp xếp theo trình tự sau bên trong tệp.

|tiêu đề
|Cơ thể
|Bảng tham khảo chéo
|Đoạn giới thiệu

#### Tiêu đề tệp PDF ####

Bất kể phiên bản PDF là gì, tệp PDF bắt đầu bằng tiêu đề chứa số nhận dạng duy nhất cho PDF và phiên bản của định dạng, chẳng hạn như %PDF-1.x trong đó x nằm trong khoảng từ 1-7.

#### Nội dung tệp ####

Phần thân của tệp PDF bao gồm một chuỗi các đối tượng gián tiếp đại diện cho nội dung của tài liệu. Các đối tượng, như được mô tả ở trên, đại diện cho các thành phần của tài liệu như phông chữ, trang và hình ảnh mẫu. Bắt đầu với PDF 1.5, phần thân cũng có thể chứa các luồng đối tượng, mỗi luồng chứa một chuỗi các đối tượng gián tiếp.

#### Bảng tham khảo chéo ####

Bảng tham chiếu chéo chứa thông tin cho phép truy cập ngẫu nhiên vào các đối tượng gián tiếp trong tệp để không cần phải đọc toàn bộ tệp để định vị bất kỳ đối tượng cụ thể nào. Bảng sẽ chứa mục nhập một dòng cho từng đối tượng gián tiếp, chỉ định độ lệch byte của đối tượng đó trong phần thân của tệp. (Bắt đầu với PDF 1.5, một số hoặc tất cả thông tin tham chiếu chéo có thể được chứa trong các luồng tham chiếu chéo.

#### Đoạn giới thiệu tệp ####

Đoạn giới thiệu của tệp PDF cho phép người đọc tuân thủ nhanh chóng tìm thấy bảng tham chiếu chéo và một số đối tượng đặc biệt. Trình đọc phù hợp nên đọc tệp PDF từ cuối tệp. Dòng cuối cùng của tệp sẽ chỉ chứa điểm đánh dấu cuối tệp, %%EOF. Hai dòng trước sẽ chứa, một dòng trên mỗi dòng và theo thứ tự, từ khóa startxref và phần bù byte trong luồng được giải mã từ đầu tệp đến đầu từ khóa xref trong phần tham chiếu chéo cuối cùng.

### Đối tượng PDF ###

Một tệp PDF bao gồm một số loại đối tượng khác nhau thuộc các loại sau

* Giá trị Boolean - đại diện cho điều kiện đúng hoặc sai
* Số - Số nguyên và Giá trị thực
* Chuỗi - chứa các ký tự trong dấu ngoặc đơn
* Tên - bắt đầu bằng ký tự chuyển tiếp /, ví dụ /ASomewhatLongerName dẫn đến ASomewhatLongerName
* Mảng - PDF hỗ trợ mảng một chiều. Mảng có kích thước cao hơn có thể được xây dựng bằng cách sử dụng mảng làm phần tử lồng nhau
* Từ điển - tập hợp các đối tượng dưới dạng cặp khóa-giá trị. Nó có thể không có mục nào.
* Luồng - đại diện cho chuỗi byte cũng có thể có độ dài không giới hạn
* Null Object - đại diện cho một giá trị null

Có thể có các đối tượng khác như nhận xét được giới thiệu bằng dấu % và có thể chứa các ký tự 8 bit.

### Đối tượng gián tiếp ###

Bất kỳ đối tượng nào trong tệp PDF có thể được gắn nhãn là đối tượng gián tiếp. Các đối tượng gián tiếp được cung cấp mã định danh đối tượng duy nhất mà theo đó các đối tượng khác có thể tham chiếu đến nó. Tham chiếu chéo đến những thứ này được duy trì trong một bảng chỉ mục và được đánh dấu bằng từ khóa xref theo sau phần chính và đưa ra độ lệch byte của từng đối tượng gián tiếp từ đầu tệp.

### Bố cục PDF tuyến tính và phi tuyến tính ###

Bố cục PDF được phân loại là Llnear và phi tuyến tính tùy thuộc vào ứng dụng đích và các yếu tố khác.

Phi tuyến tính - Các tệp PDF phi tuyến tính sử dụng ít dung lượng ổ đĩa hơn so với các tệp PDF tuyến tính. Các trang PDF của tài liệu nằm ở dạng rải rác trên tệp PDF và đó là lý do tại sao các tệp phi tuyến tính chậm hơn so với các tệp tuyến tính.

Linear PDF - Nhắm mục tiêu người xem PDF trực tuyến, các tệp PDF tuyến tính được xây dựng theo cách chúng được ghi vào đĩa theo kiểu tuyến tính. Điều này không yêu cầu plugin trình duyệt để tải toàn bộ tài liệu trước khi hiển thị.

### Tổng quan về đối tượng ###

Như đã đề cập, phần thân PDF là một tập hợp các đối tượng được đề cập ở trên. PDF chủ yếu dựa trên PostScript mà không có các tính năng kiểm soát của ngôn ngữ lập trình như lệnh if và vòng lặp. Các lệnh do mã Postscript đưa ra để tạo nội dung đồ họa được thu thập và mã hóa cùng với bất kỳ tệp, đồ họa hoặc phông chữ nào được tài liệu giới thiệu. Tất cả những nội dung này được tích lũy vào một tệp duy nhất, dẫn đến đầu ra PostScript tổng hợp.

#### Chữ ####

Văn bản trong PDF được thể hiện bằng các phần tử văn bản thực sự được hiển thị bằng các nét chữ từ phông chữ. Hình tượng là một hình dạng đồ họa và chịu mọi thao tác đồ họa, chẳng hạn như chuyển đổi tọa độ. Do tầm quan trọng của văn bản trong hầu hết các mô tả trang, PDF cung cấp các tiện ích cấp cao hơn để mô tả, chọn và hiển thị các nét tượng trưng một cách thuận tiện và hiệu quả.

#### Đồ họa ####

Các toán tử đồ họa được sử dụng trong luồng nội dung PDF mô tả hình thức của các trang sẽ được sao chép trên thiết bị đầu ra raster. Các cơ sở được dành cho cả ứng dụng máy in và hiển thị. Các toán tử đồ họa tạo thành sáu nhóm chính:

* Các toán tử trạng thái đồ họa thao tác với cấu trúc dữ liệu được gọi là trạng thái đồ họa, khuôn khổ chung mà trong đó các toán tử đồ họa khác thực thi. Trạng thái đồ họa bao gồm ma trận chuyển đổi hiện tại (CTM), ánh xạ tọa độ không gian người dùng được sử dụng trong luồng nội dung PDF thành tọa độ thiết bị đầu ra. Nó cũng bao gồm màu hiện tại, đường cắt hiện tại và nhiều tham số khác là toán hạng ẩn của toán tử vẽ.
* Các toán tử xây dựng đường dẫn chỉ định các đường dẫn, xác định hình dạng, quỹ đạo đường và các vùng thuộc nhiều loại khác nhau. Chúng bao gồm các toán tử để bắt đầu một đường dẫn mới, thêm các đoạn thẳng và đường cong vào nó và đóng nó.
* Toán tử vẽ đường dẫn tô màu đường dẫn, vẽ một nét dọc theo đường dẫn hoặc sử dụng đường viền đó làm ranh giới cắt.
* Các toán tử vẽ khác vẽ một số đối tượng đồ họa tự mô tả. Chúng bao gồm các hình ảnh được lấy mẫu, các sắc thái được xác định bằng hình học và toàn bộ luồng nội dung lần lượt chứa các chuỗi toán tử đồ họa.
* Toán tử văn bản chọn và hiển thị các ký tự glyphs từ các phông chữ (mô tả các kiểu chữ để thể hiện các ký tự văn bản). Vì PDF coi các nét tượng hình là hình dạng đồ họa chung nên nhiều toán tử văn bản có thể được nhóm với trạng thái đồ họa hoặc toán tử vẽ tranh. Tuy nhiên, các cấu trúc dữ liệu và cơ chế để xử lý các mô tả về phông chữ và hình tượng là đủ chuyên biệt.
* Các toán tử nội dung được đánh dấu liên kết thông tin logic mức cao hơn với các đối tượng trong luồng nội dung. Thông tin này không ảnh hưởng đến hình thức hiển thị của nội dung; nó rất hữu ích cho các ứng dụng sử dụng PDF để trao đổi tài liệu.

## Người giới thiệu ##

* [Định dạng tệp PDF: Cấu trúc cơ bản](https://resources.infosecinst acad.com/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://vi.wikipedia.org/wiki/PDF)
* [Tham khảo PDF - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

