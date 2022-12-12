{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Siêu tệp đồ họa máy tính", "Tệp", "Phần mở rộng", "Định dạng tệp", "Đồ họa véc-tơ", "Mô tả siêu tệp"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp CGM",
  "description":"Tìm hiểu về định dạng tệp CGM và các API có thể tạo và mở tệp CGM.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Tập tin CGM là gì? ##

Siêu tệp đồ họa máy tính (CGM) là định dạng siêu tệp tiêu chuẩn quốc tế, miễn phí, độc lập với nền tảng để lưu trữ và trao đổi đồ họa vector (2D), đồ họa raster và văn bản. CGM sử dụng cách tiếp cận hướng đối tượng và nhiều chức năng cung cấp để sản xuất hình ảnh. CGM sử dụng các đặc điểm hướng đối tượng này để làm lại các phần tử đồ họa để hiển thị hình ảnh. Siêu tệp chứa thông tin cần thiết xác định các tệp khác. Trong CGM, tệp nguồn dựa trên văn bản chứa tất cả các yếu tố đồ họa mà sau này có thể được biên dịch thành tệp nhị phân. Về cơ bản, CGM là một cách để tạo điều kiện trao đổi dữ liệu đồ họa 2D, độc lập với bất kỳ nền tảng hoặc thiết bị cụ thể nào.

Định dạng CGM cung cấp các yếu tố khác nhau để thực hiện các chức năng và biểu thị các đối tượng để điều chỉnh các nguyên mẫu hình học và thông tin đồ họa. Mặc dù CGM đã được thay thế bằng các định dạng khác để hiển thị nghệ thuật đồ họa trên các trang web vì nó không được các trang web hỗ trợ tốt, nhưng CGM vẫn rất phổ biến trong các ứng dụng công nghiệp, hàng không và kỹ thuật khác. Mặc dù World Wide Web Consortium đã phát triển WebCGM, một cách tiếp cận thay thế cho việc sử dụng CGM trên Web. Việc triển khai CGM chính là một minh họa về trình tự các hoạt động cơ bản của Hệ thống hạt nhân đồ họa (GKS). Nó không được áp dụng nhiều trong các thiết kế chuyên nghiệp nhưng phần lớn đã được thay thế bằng các định dạng khác như DXF và SVG.

## Lịch sử ##

CGM hóa ra là một tiêu chuẩn quốc tế vào năm 1987 (ISO 8632-1987) và cũng được BSI áp dụng làm tiêu chuẩn quốc gia ở Anh và ANSI ở Hoa Kỳ. Sau một số sửa đổi vào năm 1991, tiêu chuẩn CGM sửa đổi đã được ban hành vào năm 1992 (ISO 8632:1992). Năm 2001, World Wide Web Consortium đã phát triển WebCGM với khả năng nâng cao để sử dụng với các trang web. Năm 2007, phiên bản thứ hai của WebCGM được phát hành và phiên bản thứ ba được phát hành vào năm 2010 với các khả năng nâng cao.

## Định dạng tệp CGM ##

Siêu tệp đồ họa máy tính về cơ bản là cơ sở dữ liệu cho thông tin đồ họa và cung cấp phương tiện để thu thập, lưu trữ và truyền dữ liệu đồ họa. Do đó, phải có một thành phần hệ thống đồ họa để tạo cơ sở dữ liệu đồng thời cùng với việc thực thi ứng dụng ở định dạng siêu tệp. Trong hầu hết các trường hợp, thành phần này là trình tạo siêu tệp. Bên cạnh đó, cần có một thành phần khác có thể tìm nạp, giải thích và hiển thị dữ liệu đồ họa trong siêu tệp. Nhu cầu này được đáp ứng bởi sự hiện diện của trình thông dịch siêu tệp. Hình dưới đây thể hiện môi trường làm việc siêu tệp đồ họa.

Mối quan hệ của CGM với các thành phần khác của một hệ thống đồ họa điển hình được minh họa trong hình trên. Từ hình này cũng thấy rõ rằng chức năng của siêu tệp không phụ thuộc vào đầu ra của thiết bị cuối cùng.

Nói chung, có hai loại siêu tệp: **chụp phần** và **chụp ảnh**. Chức năng chính của siêu tệp chụp ảnh là chụp nhiều định nghĩa ảnh độc lập với thiết bị. Trong khi các siêu tệp chụp phiên sử dụng giao diện hệ thống để chụp đoạn hội thoại đầu ra trong một hệ thống đồ họa. CGM thuộc danh mục siêu tệp chụp ảnh tĩnh. CGM cung cấp sự sắp xếp các thành phần được tổ chức tốt với cấu trúc hai cấp.

1. Bộ mô tả siêu tệp
1. Một nhóm các hình ảnh độc lập về mặt logic

Mỗi ảnh là một tập hợp các mô tả ảnh và phần thân ảnh bao gồm định nghĩa ảnh. bộ mô tả siêu tệp xác định thông tin mô tả áp dụng như nhau cho tất cả các ảnh của siêu tệp đó. Thông tin này giúp trình thông dịch phân tích chính xác siêu tệp và nhận ra các tài nguyên cần thiết để hiển thị ảnh chính xác. Mặc dù bộ mô tả hình ảnh cũng bao gồm thông tin mô tả nhưng nó chỉ có thể nhận ra hình ảnh chứa bộ mô tả. Ở định dạng tệp này, mỗi định nghĩa ảnh là độc lập và có chủ quyền hợp lý. Chúng độc lập với tất cả các định nghĩa ảnh khác trong một tệp. Ngay sau khi giải thích bộ mô tả meta, hình ảnh có thể được truy cập và giải thích một cách ngẫu nhiên. Thay đổi trạng thái của hình ảnh trước đó không ảnh hưởng đến người kế vị của họ. Tính độc lập của hình ảnh này là một tính năng nổi bật khác của CGM.CGM bao gồm không gian tọa độ là tọa độ Descartes 2D được gọi là tọa độ thiết bị ảo và có thể được biểu thị thông qua số hoặc độ chính xác biểu thị phạm vi và mức độ chi tiết. CGM chỉ định cả lựa chọn màu sắc trực tiếp và lựa chọn dựa trên chỉ mục. Trước đây, bộ xác định màu bao gồm bộ ba RGB trong khi sau đó, bộ xác định màu chỉ ra một chỉ mục trong bảng màu.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
