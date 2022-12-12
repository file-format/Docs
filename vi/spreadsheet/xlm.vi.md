{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "file", "extension", "file format", "Microsoft Excel Macro File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Hướng dẫn định dạng tệp của bạn để biết tệp Macro XLM là gì và các API có thể tạo và mở tệp XLM.",
  "title" :"Tệp XLM là gì?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Tệp XLM là gì?

XLM, cho Excel Macro, là một loại tệp Bảng tính được sử dụng để lưu trữ Macro. Từ quan điểm ứng dụng, Macro là tập hợp các hướng dẫn được sử dụng để tự động hóa các quy trình. Macro được sử dụng để ghi lại các bước được thực hiện lặp lại cho định dạng tệp [XLS](/vi/spreadsheet/xls/) và hỗ trợ thực hiện các hành động bằng cách chạy lại macro. Macro được lập trình bằng Visual Basic for Applications (VBA) của Microsoft từ trong Sổ làm việc Excel bằng Trình chỉnh sửa Visual Basic và có thể chạy/gỡ lỗi trực tiếp từ đó.

## Lược Sử ##

Microsoft Excel đã hỗ trợ lập trình macro kể từ lần ra mắt công chúng đầu tiên. Các tính năng của macro vẫn giữ nguyên qua các phiên bản tiếp theo cho Excel với phần mở rộng theo các tính năng mới. XLM là ngôn ngữ macro mặc định cho Excel cho đến Excel 4.0. Excel 5.0 ghi macro trong VBA theo mặc định nhưng với phiên bản 5.0 ghi XLM vẫn được cho phép dưới dạng tùy chọn. Sau phiên bản 5.0, tùy chọn đó đã bị ngừng. Tất cả các phiên bản Excel, kể cả Excel 2010 đều có khả năng chạy macro XLM, mặc dù Microsoft không khuyến khích sử dụng chúng.

## Đang ghi Macro trong XLM ##

Excel cung cấp các bước dễ sử dụng để ghi macro. Nó yêu cầu bạn phải cài đặt các công cụ dành cho Nhà phát triển để hoạt động với Macro. Khi quá trình ghi macro đang được xử lý, nó sẽ ghi lại từng hành động của người dùng để phát sau này. Ghi macro thực sự bao gồm tất cả các bước mà người dùng thực hiện sau khi quá trình ghi bắt đầu. Vì vậy, nếu bạn làm cho nội dung của một ô được in đậm, in nghiêng và đặt căn lề văn bản sau khi bắt đầu ghi macro, thì tất cả các lệnh này sẽ được ghi lại. Mỗi macro đã ghi cũng có thể được gán một phím tắt để phát lại nhanh sau này. Ghi macro tạo mã VBA ở dạng macro có thể được chỉnh sửa bằng Trình chỉnh sửa Visual Basic (VBE).

## Mô hình đối tượng Excel ##

Macro sử dụng các quy trình VBA ở phía sau và tuân theo [Mô hình đối tượng Excel](https://docs.microsoft.com/en-us/office/vba/api/overview/excel/object-model) cho mục đích này. Mô hình này xác định các đối tượng của bảng tính để tương tác với bảng tính thông qua thanh công cụ lệnh, thanh lệnh hoặc hộp thông báo do người dùng xác định. Ví dụ: quyền truy cập vào các thuộc tính của sổ làm việc được cấp cho đối tượng Sổ làm việc. Tương tự, có đối tượng Worksheet trong mô hình để làm việc với các trang tính của sổ làm việc theo chương trình.

## Macro và Bảo mật ##

VBA cho phép truy cập vào tất cả các lĩnh vực của ứng dụng cũng như hệ thống tệp và cũng có thể gây nguy hiểm. Điều này gây lo ngại khi chia sẻ sổ làm việc với người có thể chạy tệp ở cuối. Đó là cảnh báo của Microsoft Excel về việc mở một tệp như vậy. Macro có thể được chứng nhận bằng chữ ký điện tử để những người dùng khác xác minh rằng chúng đáng tin cậy. Do đó, macro có thể được kích hoạt sau khi xác minh nguồn của chúng.

## Người giới thiệu ##

* [[MS-XLS] - Cấu trúc định dạng tệp nhị phân Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Lập trình Macro](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

