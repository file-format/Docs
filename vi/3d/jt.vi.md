{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "file", "extension", "format", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp JT và API có thể tạo và mở tệp JT.",
  "title" :"JT - Định dạng tệp sao Mộc Tessellation",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp JT là gì?

**JT** (Jupiter Tessellation) là định dạng dữ liệu 3D chuẩn ISO linh hoạt, tập trung vào ngành và hiệu quả được phát triển bởi Siemens PLM Software. Các lĩnh vực CAD cơ học của Hàng không vũ trụ, công nghiệp ô tô và Thiết bị nặng sử dụng JT làm định dạng trực quan 3D hàng đầu của họ.

Định dạng JT là biểu đồ cảnh hỗ trợ các thuộc tính và nút dành riêng cho CAD. Kỹ thuật nén tinh vi được sử dụng để lưu trữ dữ liệu khía cạnh (hình tam giác). Định dạng này được cấu trúc để hỗ trợ các thuộc tính trực quan, thông tin sản phẩm và sản xuất (PMI) và Siêu dữ liệu. Có một sự hỗ trợ tốt cho truyền phát nội dung không đồng bộ. Trong ngành cơ khí nặng, các chuyên gia sử dụng tệp JT trong các giải pháp CAD và chương trình phần mềm quản lý vòng đời sản phẩm (PLM) để kiểm tra hình dạng của hàng hóa phức tạp.

Vì JT hỗ trợ gần như tất cả các định dạng CAD 3D quan trọng nên hệ thống của nó có thể xử lý nhiều kiểu kết hợp được gọi là "multi-CAD". Việc lắp ráp nhiều CAD này luôn được quản lý tốt và cập nhật vì việc đồng bộ hóa giữa các tệp mô tả sản phẩm CAD gốc với các tệp JT được liên kết của chúng diễn ra tự động. Các tệp JT ban đầu rất nhẹ, vì vậy được coi là phù hợp để cộng tác trên internet. Các công ty Cộng tác thông qua việc gửi hình ảnh 3D qua phương tiện dễ dàng hơn nhiều so với các tệp CAD gốc “nặng”. Ngoài ra, các tệp JT đảm bảo nhiều tính năng bảo mật giúp chia sẻ tài sản trí tuệ an toàn hơn.

## Lịch sử tóm tắt về định dạng tệp JT

Engineering Animation, Inc. và Hewlett Packard là những nhà thiết kế ban đầu của JT, họ đã phát triển định dạng đó dưới dạng bộ công cụ Mô hình Trực tiếp. Sau khi EAI được mua lại bởi UGS Corp. JT đã trở thành một phần của bộ UGS. Đầu năm 2007, UGS công bố JT là định dạng 3D chính của họ. Trong cùng năm đó, Siemens AG đã mua UGS và trở thành Phần mềm PLM của Siemens. Siemens sử dụng JT làm định dạng khả năng tương tác chung và định dạng lưu trữ dữ liệu. Năm 2009, ISO đã chấp nhận đặc tả JT để xuất bản dưới dạng Đặc tả có sẵn công khai của ISO (PAS). Vào giữa năm 2010, ProSTEP iViP đã thông báo rằng ở cấp độ công nghiệp, JT và STEP AP 242 XML có thể được sử dụng cùng nhau để đạt được lợi thế tối đa về dữ liệu kịch bản trao đổi. Vào năm 2012, JT đã chính thức được tuyên bố là định dạng trực quan hóa 3D được tiêu chuẩn hóa ISO (ISO 14306:2012 (ISO JT V1)).

## Định dạng tệp JT ##

Tất cả các đối tượng ở định dạng JT được biểu diễn thông qua mã định danh đối tượng và các tham chiếu giữa các đối tượng được xử lý thông qua mã định danh của đối tượng được tham chiếu. Tính toàn vẹn của các tham chiếu đối tượng này có thể được duy trì thông qua các con trỏ unswizzling/swizzling.

Một tệp JT được sắp xếp dưới dạng một loạt các khối và khối Tiêu đề luôn là khối dữ liệu đầu tiên trong tệp. Một loạt phân đoạn dữ liệu và phân đoạn TOC ngay sau khối tiêu đề. Một phân đoạn Dữ liệu (6 Phân đoạn LSG) luôn tồn tại một tệp JT tuân thủ tham chiếu. Phân đoạn TOC chứa thông tin vị trí của tất cả các Phân đoạn dữ liệu khác của tệp đó.

{{< figure src="../JT-1.png" alt="Định dạng tệp JT" >}}

### Tiêu đề tệp ###

Tiêu đề tệp là khối đầu tiên trong hệ thống phân cấp dữ liệu của tệp JT. Thông tin lập phiên bản và thông tin vị trí TOC được đính kèm trong tiêu đề để tạo điều kiện thuận lợi cho trình tải đọc tệp. Nội dung tiêu đề tập tin được sắp xếp như sau.

### Phân đoạn TOC ###

Phân đoạn TOC phải tồn tại trong một tệp và chứa thông tin nhận dạng và vị trí của tất cả các phân đoạn dữ liệu khác. Vị trí thực tế của Phân đoạn TOC được chỉ định bởi trường Độ lệch TOC của tiêu đề tệp. Mỗi Phân đoạn dữ liệu có thể định địa chỉ riêng lẻ được biểu thị bằng mục nhập TOC trong phân đoạn TOC.

### Đoạn dữ liệu ###

Tệp JT xác định tất cả dữ liệu được lưu trữ trong Phân đoạn dữ liệu. Một số Phân đoạn dữ liệu có thể nén tất cả các byte dữ liệu của thông tin còn lại trong phân đoạn. Phân đoạn dữ liệu có cấu trúc như sau:

![alt text](../JT-2.png "JT Data Segment")

Bảng sau đây mô tả các loại phân đoạn dữ liệu khác nhau:

|Tên|Mô tả
---|---|
|Đoạn LSG|Bao gồm một tập hợp các đối tượng được liên kết thông qua các tham chiếu có hướng để tạo thành LSG (cấu trúc đồ thị tuần hoàn có hướng)
|Đoạn LOD hình dạng|chứa dữ liệu xác định cho các hình dạng hình học (ví dụ: đỉnh, pháp tuyến, đa giác, v.v.)
|Phân đoạn JT B-Rep|Có phần tử để dữ liệu biểu thị ranh giới hình học chính xác cho một phần riêng lẻ ở định dạng JT B-Rep.
|Phân đoạn XT B-Rep|Có phần tử để dữ liệu biểu thị ranh giới hình học chính xác cho một phần riêng lẻ ở định dạng biểu diễn ranh giới
|Phân đoạn khung dây|Dữ liệu biểu thị khung dây 3D chính xác cho một phần cụ thể được xác định bởi một phần tử có trong phân đoạn này.
|Phân đoạn siêu dữ liệu|Cho phép lưu trữ siêu dữ liệu trong các phân đoạn có thể định địa chỉ riêng biệt.
|Phân đoạn JT ULP|Có phần tử cho dữ liệu biểu thị ranh giới hình học bán chính xác cho một phần riêng lẻ ở định dạng JT ULP.
|Phân đoạn JT LWPA|Chứa phần tử xác định dữ liệu phân tích cho một phần cụ thể. LWPA bao gồm bộ sưu tập các bề mặt phân tích trong định nghĩa b-rep của bộ phận.

## Nén ##

Yêu cầu truyền tải và lưu trữ của các mô hình 3D đòi hỏi khắt khe hơn, vì vậy các tệp JT có thể tận dụng lợi thế của việc nén. Một mô hình dữ liệu JT có thể bao gồm các tệp khác nhau sử dụng kỹ thuật nén khác nhau nhưng quá trình nén là minh bạch đối với người dùng dữ liệu JT.

Cho đến nay, Bộ công cụ mở JT (dưới dạng tiêu chuẩn) và nén nâng cao là hai kỹ thuật nén được sử dụng bởi các tệp JT. Bộ công cụ mở JT sử dụng thuật toán nén dễ dàng, không mất dữ liệu, trong khi tính năng nén nâng cao sử dụng kỹ thuật nén dành riêng cho miền, tinh vi hơn dẫn đến nén hình học có tổn thất. Các ứng dụng khách thích nén nâng cao hơn là sử dụng nén tiêu chuẩn, vì nén nâng cao mang lại tỷ lệ nén khá cao. Khả năng tương thích ngược với các ứng dụng xem tệp JT thông thường được duy trì thông qua việc cung cấp nén tiêu chuẩn. Dạng nén phải tương thích với phiên bản định dạng tệp JT. Phiên bản này có thể được nhìn thấy khi tệp JT mở bằng trình chỉnh sửa văn bản và được đính kèm trong thông tin tiêu đề ASCII.

## Người giới thiệu ##

* [Tham chiếu định dạng tệp JT](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (định dạng trực quan hóa)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

