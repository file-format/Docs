{
  "date" : "2020-03-16",
  "keywords" :[ "Tệp IFC", "Định dạng", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp IFC và API có thể tạo và mở tệp IFC.",
  "title" :"Định dạng tệp IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp IFC là gì?

Các tệp có phần mở rộng IFC đề cập đến định dạng tệp Lớp nền tảng công nghiệp (IFC) thiết lập các tiêu chuẩn quốc tế để nhập và xuất các đối tượng tòa nhà và thuộc tính của chúng. Định dạng tệp này cung cấp khả năng tương tác giữa các ứng dụng phần mềm khác nhau. Các thông số kỹ thuật cho định dạng tệp này được buildSMART International phát triển và duy trì dưới dạng Tiêu chuẩn dữ liệu. Mục tiêu cuối cùng của định dạng tệp IFC là cải thiện khả năng giao tiếp, năng suất, thời gian giao hàng và chất lượng trong suốt vòng đời của tòa nhà.

Do các tiêu chuẩn được thiết lập cho các đối tượng phổ biến trong ngành công nghiệp xây dựng, nó làm giảm việc mất thông tin trong quá trình truyền từ ứng dụng này sang ứng dụng khác. IFC có thể lưu trữ dữ liệu về hình học, tính toán, số lượng, quản lý cơ sở, định giá, v.v. cho nhiều ngành nghề khác nhau (kiến trúc sư, điện, HVAC, kết cấu, địa hình, v.v.).

## Lược Sử ##

Sáng kiến IFC được Autodesk đưa ra vào năm 1994 để hỗ trợ phát triển ứng dụng tích hợp và bao gồm các công ty như Honeywell, Butler Manufacturing và AT&T. Năm 1995, tư cách thành viên được mở cho bất kỳ ai và tên được đổi thành Liên minh quốc tế về khả năng tương tác. Mục đích của tổ chức phi lợi nhuận là xuất bản Lớp nền tảng công nghiệp (IFC) dưới dạng mô hình sản phẩm AEC. Vào năm 2005, tên này lại được thay đổi và buildSMART hiện vẫn duy trì tên này.

## Định dạng tệp IFC ##

Định dạng tệp IFC đã trải qua một số thay đổi trong quá khứ để đạt được thông số định dạng tệp v4. Một số thay đổi nhỏ xảy ra theo thời gian cũng như đã được đưa vào một phần của thông số kỹ thuật dưới dạng Phụ lục. Sau đây là danh sách các phiên bản khác nhau của thông số kỹ thuật tệp đã được công khai trong quá khứ.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (tháng 3 năm 2013) ifcXML2x3 (tháng 6 năm 2007)
* IFC2x3 (tháng 2 năm 2006) ifcXML2 cho IFC2x2 add1 (RC2)
* IFC2x2 Phụ lục 1 (tháng 7 năm 2004)ifcXML2 cho IFC2x2 (RC1)
* IFC 2x2IFC 2x Phụ lục 1ifcXML1 cho IFC2x và
* Phụ lục IFC2x 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Các phiên bản mới nhất của thông số kỹ thuật định dạng tệp IFC luôn có sẵn trên trang web buildingSMART và nhà phát triển nên tham khảo những phiên bản này cho bất kỳ loại ứng dụng nào họ dự định phát triển. Khi viết bài này, thông số kỹ thuật của phiên bản 4 là thông số kỹ thuật mới nhất có sẵn trực tuyến.

### Định dạng tệp dữ liệu IFC ###

Định dạng tệp IFF hỗ trợ trao đổi dữ liệu giữa các ứng dụng sử dụng các định dạng khác nhau như được liệt kê bên dưới:

**IFC:** Đây là định dạng trao đổi IFC mặc định và sử dụng cấu trúc tệp vật lý BƯỚC theo ISO 10303-21. Định dạng tệp này có phần mở rộng tệp .ifc và là định dạng IFC được sử dụng nhiều nhất.

**IFC-XML:** Đây là phiên bản định dạng tệp XML của IFC có thể được tạo trực tiếp bởi ứng dụng gửi theo cấu trúc ISO 10303-28, còn được gọi là STEP-XML. Định dạng tệp IFC-XML được coi là phù hợp với khả năng tương tác giữa các công cụ XML. So với định dạng tệp IFC, IFC-XML có kích thước lớn hơn 300-400%.

**IFC-ZIP:** Đây là phiên bản nén [ZIP](/vi/compression/zip/) của IFC hoặc IFC-XML trong đó một trong các tệp này nằm trong thư mục chính của kho lưu trữ zip. Định dạng này nén .ifc xuống 60-80% và .ifc tệp XML xuống 90-95%.

### Kiến trúc IFC ###

Đặc tả của IFC bao gồm các thuật ngữ, khái niệm và các hạng mục đặc tả dữ liệu bắt nguồn từ việc sử dụng trong các ngành, nghề và chuyên môn của ngành xây dựng và quản lý cơ sở vật chất. Thuật ngữ và khái niệm sử dụng các từ tiếng Anh đơn giản, các mục dữ liệu trong đặc tả dữ liệu tuân theo quy ước đặt tên.

tên mục dữ liệu cho các loại, thực thể, quy tắc và chức năng bắt đầu bằng tiền tố "Ifc" và tiếp tục bằng các từ tiếng Anh trong quy ước đặt tên CamelCase (không có gạch dưới, chữ cái đầu tiên trong từ viết hoa); tên thuộc tính trong một thực thể tuân theo quy ước đặt tên CamelCase không có tiền tố; định nghĩa tập hợp thuộc tính là một phần của tiêu chuẩn này bắt đầu bằng tiền tố "Pset_" và tiếp tục bằng các từ tiếng Anh trong quy ước đặt tên CamelCase; các định nghĩa tập hợp số lượng là một phần của tiêu chuẩn này bắt đầu bằng tiền tố "Qto_" và tiếp tục bằng các từ tiếng Anh trong quy ước đặt tên CamelCase.

Kiến trúc lược đồ dữ liệu của IFC định nghĩa bốn lớp khái niệm, mỗi lược đồ riêng lẻ được gán cho chính xác một lớp khái niệm.

**Lớp tài nguyên** — lớp thấp nhất bao gồm tất cả các lược đồ riêng lẻ chứa các định nghĩa tài nguyên, các định nghĩa đó không bao gồm mã định danh duy nhất toàn cầu và sẽ không được sử dụng độc lập với định nghĩa được khai báo ở lớp cao hơn;

**Lớp lõi** — lớp tiếp theo bao gồm lược đồ hạt nhân và lược đồ mở rộng lõi, chứa các định nghĩa thực thể chung nhất, tất cả các thực thể được xác định ở lớp lõi hoặc cao hơn mang id duy nhất trên toàn cầu và thông tin lịch sử và chủ sở hữu tùy chọn;

**Lớp khả năng tương tác** — lớp tiếp theo bao gồm các lược đồ chứa các định nghĩa thực thể dành riêng cho một chuyên môn hóa sản phẩm, quy trình hoặc tài nguyên chung được sử dụng trong một số lĩnh vực, các định nghĩa đó thường được sử dụng để trao đổi và chia sẻ thông tin xây dựng giữa các miền;

**Lớp miền** — lớp cao nhất bao gồm các lược đồ chứa các định nghĩa thực thể là các chuyên môn hóa sản phẩm, quy trình hoặc tài nguyên dành riêng cho một lĩnh vực nhất định, những định nghĩa đó thường được sử dụng để trao đổi và chia sẻ thông tin trong miền.

## Người giới thiệu ##

* [Lớp nền tảng công nghiệp - Theo Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

