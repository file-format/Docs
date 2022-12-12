{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","tệp asmx", "định dạng tệp asmx", "loại tệp asmx", "tệp", "loại", "tệp asmx là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - Tệp dịch vụ web ASP.NET",
  "description" :"Tìm hiểu về tệp ASMX là gì và các API có thể tạo và mở tệp ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Tệp ASMX là gì?

Tệp có phần mở rộng .asmx là tệp Dịch vụ web ASP.NET cung cấp liên lạc giữa hai đối tượng qua internet bằng Giao thức truy cập đối tượng đơn giản (SOAP). Nó được triển khai như một dịch vụ trên Máy chủ Web dựa trên Windows để xử lý yêu cầu gửi đến và trả về phản hồi. Không giống như các tệp [ASPX](/vi/web/aspx/) chứa mã để hiển thị trực quan các trang web ASP.NET, các tệp ASMX chạy ở chế độ nền trên máy chủ và thực hiện các tác vụ khác nhau như kết nối với cơ sở dữ liệu, truy xuất dữ liệu và trả lại dữ liệu trong một định dạng trong đó yêu cầu đã được thực hiện. Chúng được sử dụng riêng cho các dịch vụ web XML.

## Định dạng tệp ASMX

Các tệp ASMX ở định dạng văn bản thuần túy và có thể được mở hoặc chỉnh sửa trong các ứng dụng như Microsoft Visual Studio hoặc trình soạn thảo văn bản. Đây là định dạng tệp độc quyền của Microsoft và có cú pháp được xác định rõ để tạo các dịch vụ web. Phản hồi của tệp ASMX ở dạng SOAP XML có các thành phần sau.

* `Envelop` - Phần tử gốc xác định tài liệu XML dưới dạng thông báo SOAP.
* `Header` - Một thành phần tùy chọn chứa thông tin dành riêng cho ứng dụng, chẳng hạn như dữ liệu xác thực. Nếu có phần tử Header thì nó phải là phần tử con đầu tiên của phần tử Envelope.
* `Nội dung` - Chứa thông báo SOAP dành cho người nhận.
* `Lỗi` - Một thành phần tùy chọn được sử dụng để biểu thị các thông báo lỗi. Nếu phần tử Lỗi xuất hiện, nó phải là phần tử con của phần tử Body.

Các tệp ASMX có thể được viết bằng các ngôn ngữ .NET như [C#](/vi/programming/cs/), [Visual Basic](/vi/programming/vb/) hoặc JScript.

## ASMX khác với ASPX và ASCX như thế nào?

Tệp ASMX khác với tệp ASPX và ASCX.

* ASPX, Active Server Pages, files là các tệp lập trình được tạo bằng Microsoft ASP.NET framework chạy trên các máy chủ web. Chúng được hiển thị trong trình duyệt web của khách hàng khi người dùng yêu cầu truy cập trang đó.
* ASCX, Active Server User Control, xác định các điều khiển người dùng được sử dụng để xác định các điều khiển có thể sử dụng lại trong các trang web ASP.NET hoặc toàn bộ trang web.

## Người giới thiệu

* [Sử dụng dịch vụ ASMX](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Kiểm soát người dùng ASCX](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

