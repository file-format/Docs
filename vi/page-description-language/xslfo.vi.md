{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "Đối tượng định dạng XSL", "Tệp", "Phần mở rộng", "Định dạng tệp", "Ngôn ngữ biểu định kiểu mở rộng"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Tìm hiểu về định dạng tệp XSLFO và các API có thể tạo và mở tệp XSLFO.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Tệp XSL-FO là gì? ##

XSL-FO (Đối tượng định dạng XSL) là ngôn ngữ biểu định kiểu mạnh mẽ để định dạng tài liệu XML. Ngữ nghĩa của dạng giới hạn của giấy và bản in được thể hiện bằng XSL-FO khi các kích thước được cố định. Trái ngược với HTML, thể hiện ngữ nghĩa của dạng không giới hạn của cửa sổ trình duyệt với các kích thước thay đổi. Các tài liệu XML được định dạng bởi XSL-FO hầu hết được sử dụng để tạo các tệp PDF. XSL (Ngôn ngữ biểu định kiểu mở rộng) là một tập hợp các công nghệ W3C có đầy đủ tính năng nhằm thiết kế để định dạng và trao đổi các tài liệu XML và một phần XSL-FO của ngôn ngữ này. XSLT và XPath cũng là những phần khác của XSL.

Người ta đề xuất rằng các tài liệu XML trước tiên nên được chuyển đổi thành XSL-FO, PDF là một ví dụ về tiêu chí này. Trong PDF, kết quả được hiển thị bằng cách sử dụng XSLT trước, sau đó là trình định dạng XSL-FO. Theo cách này, các tài liệu XML có thể được định dạng ngẫu nhiên. Mặc dù XSL-FO tận dụng lợi thế của việc sử dụng các thuộc tính Cascading Style Sheet (CSS) và mở rộng chúng khi cần thiết cho định dạng thực, nhưng nó cung cấp các mẫu trang được gọi là trang cái theo thuật ngữ của XSL-FO. XSL-FO cũng cung cấp định dạng cho các tài liệu khá phức tạp và hỗ trợ tạo chỉ mục.

## Lịch sử và các khái niệm cơ bản ##

Vào tháng 1 năm 2012, Bản thảo làm việc của XSL-FO đã được cập nhật lần cuối và vào tháng 11 năm 2013, Nhóm làm việc của nó đã bị đóng. Biểu định kiểu XSL chỉ định cách trình bày của một lớp tài liệu XML bằng cách mô tả cách một thể hiện của lớp được chuyển đổi thành một tài liệu XML sử dụng từ vựng định dạng. XSL-FO là ngôn ngữ trình bày tích hợp và không có đánh dấu ngữ nghĩa được sử dụng trong HTML. Hơn nữa, ngôn ngữ này lưu trữ tất cả dữ liệu của tài liệu bên trong chính nó, trái ngược với CSS làm thay đổi cài đặt mặc định của tài liệu HTML hoặc XML bên ngoài.

Tiêu chí chung của việc sử dụng XSL-FO là người dùng viết tài liệu bằng ngôn ngữ XML thay vì viết bằng FO. Sau đó, một biến đổi XSLT xảy ra. Biến đổi XSLT này chịu trách nhiệm chuyển đổi XML thành XSL-FO. Ngay sau khi tài liệu XSL-FO được tạo, nó sẽ được chuyển giao cho một ứng dụng có tên là bộ xử lý FO. Bộ xử lý FO chịu trách nhiệm chuyển đổi tài liệu này thành tài liệu có thể đọc được cũng như có thể in được. Các tệp PDF hoặc PS là những ví dụ về đầu ra phổ biến nhất của XSL-FO. Nhưng điều đó không có nghĩa là bộ xử lý FO chỉ có thể tạo ra hai loại định dạng này làm đầu ra. Một số bộ xử lý FO có thể xuất ra các tệp RTF hoặc thậm chí một cửa sổ có thể xuất hiện trong GUI của người dùng, cửa sổ này hiển thị trình tự của trang và nội dung của chúng.

Tài liệu XSL-FO khác với PDF hoặc PS theo nghĩa, nó không xác định cuối cùng bố cục văn bản trên các trang khác nhau. Có lẽ, nó tạo kiểu cho các trang và xác định vị trí hiển thị nội dung. Ngoài ra, bộ xử lý FO tổ chức văn bản trong các ranh giới được chỉ định bởi tài liệu FO. Thông số kỹ thuật này thậm chí còn cho phép các bộ xử lý FO khác nhau hoạt động tương ứng với các trang được tạo kết quả. Một ví dụ về hành vi như vậy là gạch nối, một số bộ xử lý FO có thể gạch nối các từ để tiết kiệm dung lượng khi ngắt dòng, trong khi một số bộ xử lý không chọn tùy chọn này. Nó phụ thuộc vào bộ xử lý để chọn các thuật toán gạch nối khác nhau phù hợp với yêu cầu của họ. Các thuật toán gạch nối này có thể rất đơn giản hoặc có thể phức tạp hơn. Trong một số trường hợp, đặc tả XSL-FO trừng phạt rõ ràng các bộ xử lý FO, một số mức độ lựa chọn theo ngữ cảnh của bố cục.

Sự thay đổi này giữa các bộ xử lý FO tạo ra các kết quả khác nhau mà các bộ xử lý thường không quan tâm. Bởi vì trọng tâm chung của XSL-FO là tạo ra các tài liệu được phân trang/in. Bản thân các tài liệu XSL-FO thường đóng vai trò trung gian, chức năng chính của chúng là tạo tệp PDF hoặc tài liệu có thể được in dưới dạng đầu ra để phân phối. Trong HTML/CSS hoặc XSL-FO, việc phân phối PDF dưới dạng kết quả cuối cùng thay vì nhập ngôn ngữ định dạng cho thấy rằng người nhận vẫn không bị ảnh hưởng bởi tính linh hoạt kết quả được tạo ra do sự khác biệt giữa các trình thông dịch ngôn ngữ định dạng. Mặt khác, rõ ràng là không có cách nào dễ dàng để một tài liệu có thể đáp ứng các nhu cầu khác nhau của người nhận, ví dụ như kích thước trang có thể thay đổi hoặc kích thước phông chữ mong muốn, hoặc tùy chỉnh cho phù hợp với trang hoặc bản in.

## Định dạng tệp XSLFO ##

Các tài liệu SL-FO về cơ bản là các tài liệu XML, nhưng chúng không tuân theo bất kỳ lược đồ nào. Thay vào đó, các tài liệu SL-FO tuân theo cú pháp được xác định trong đặc điểm kỹ thuật của ngôn ngữ riêng của chúng. Có hai phần bắt buộc trong mỗi tài liệu XSL-FO:

1. Phần chỉ định danh sách bố cục trang được gắn nhãn.
1. Phần có tất cả các chi tiết của dữ liệu tài liệu, có đánh dấu, xác định việc hiển thị nội dung trên các trang khác nhau thông qua các bố cục trang khác nhau.

Các thuộc tính của trang được đề cập trong bố cục trang, có thể xác định tổ chức cho văn bản, tuân thủ các quy ước cho ngôn ngữ cụ thể. Hơn nữa, kích thước của trang, lề của chúng và trình tự của các trang (áp dụng các thuộc tính khác nhau cho các trang lẻ và trang chẵn) cũng được xác định bởi bố cục trang.

Phần dữ liệu của tài liệu được chia thành một loạt các luồng, trong đó mỗi luồng được kết nối với một bố cục trang. Các luồng kèm theo một danh sách các khối trong đó. Danh sách các khối này có thể chứa các tính năng đánh dấu nội tuyến hoặc danh sách dữ liệu văn bản hoặc có thể cả hai cùng một lúc. Lề của tài liệu cũng có thể hiển thị số trang hoặc tiêu đề chương. Chức năng của cả khối và phần tử nội tuyến vẫn giống như trong CSS, tuy nhiên một số quy tắc đệm và lề khác nhau giữa FO và CSS.

Hướng định hướng trang được chỉ định hoàn toàn cho phần mở rộng của khối và nội tuyến, do đó làm cho tài liệu FO hoạt động dưới các ngôn ngữ khác với tiếng Anh. Ngôn ngữ của đặc tả FO sử dụng các từ bắt đầu và kết thúc thay vì trái và phải để mô tả chỉ đường. Các quy tắc xếp tầng và đánh dấu nội dung cơ bản của XSL-FO được lấy từ CSS. Ngôn ngữ của XSL-FO đồng ý với các thông số kỹ thuật sau.

## Nhiều cột ##

Một trang có thể có nhiều cột và khối và có thể mở rộng từ cột này sang cột khác theo mặc định. Nhiều trang được phép có chiều rộng và số lượng cột khác nhau. Tất cả các đặc điểm của FO đều tuân theo các giới hạn của trang nhiều cột.

### Danh sách ###

Một danh sách XSL-FO được thiết lập bởi hai tập hợp các khối được sắp xếp cạnh nhau bằng hàm. Về mặt khái niệm, trong một danh sách, khối bên trái biểu thị một số, dấu đầu dòng hoặc chuỗi văn bản, trong khi khối bên phải có thể hoạt động như mong đợi. Việc đánh số danh sách XSL-FO thường được thực hiện bởi XSLT.

### Những cái bàn ###

Bảng FO tương tự như bảng HTML/CSS. Người dùng có thể chọn các hàng dữ liệu, thông tin kiểu dáng, màu nền cho từng ô riêng lẻ. Sử dụng thông tin kiểu dáng riêng biệt, người dùng có đặc quyền chọn hàng đầu tiên làm hàng tiêu đề bảng. Bộ xử lý FO có thể được thông báo rõ ràng về đặc tả không gian của từng cột hoặc để tự động điều chỉnh văn bản trong bảng.

### Lập chỉ mục ###

XSL-FO 1.1 có các tính năng giúp tạo chỉ mục thông qua tham chiếu các phần tử được đánh dấu đúng cách.

### Lợi ích ###

* Thích hợp cho xuất bản dựa trên nội dung
* Dễ sử dụng
* Giá thấp

## Người giới thiệu ##

* [XSL-FO là gì?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [Đối tượng định dạng XSL](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

