{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "file", "extension", "file format", "Visual Basic", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Tệp mã Visual Basic",
  "description":"Tìm hiểu về định dạng tệp VB và API có thể tạo và mở tệp VB.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp VB là gì?

Tệp VB là tệp mã nguồn được tạo bằng ngôn ngữ Visual Basic do Microsoft tạo để phát triển các ứng dụng .NET. Một ngôn ngữ tương tự khác với cú pháp khác là C# có tệp được lưu với phần mở rộng tệp [.CS](/vi/programming/cs/). Định dạng tệp cung cấp ngôn ngữ lập trình cấp thấp để viết mã được biên dịch để tạo tệp đầu ra cuối cùng ở dạng EXE hoặc DLL. Chúng có thể được tạo và biên dịch bằng Microsoft Visual Studio. Microsoft Visual Studio Express cũng có thể được sử dụng để tạo và cập nhật các tệp như vậy, đây là một IDE miễn phí. Một dự án Visual Studio đơn giản [giải pháp](/vi/programming/sln/) được tạo bằng ngôn ngữ VB có thể bao gồm một hoặc nhiều tệp như vậy. Các tệp được đánh dấu để đưa vào quá trình biên dịch được liệt kê trong tệp [CSPROJ](/vi/programming/csproj/) là một phần của dự án và yêu cầu trình biên dịch sử dụng các tệp được đánh dấu.

## Định dạng tệp VB - Thông tin khác

Tệp VB là định dạng tệp dựa trên văn bản có thể được mở trong bất kỳ trình soạn thảo văn bản nào để chỉnh sửa. Tuy nhiên, khi được mở trong một IDE được hỗ trợ với cú pháp tô sáng thích hợp, mã sẽ dễ đọc và sắp xếp. Một tệp VB đơn giản chứa:

* Khai báo không gian tên - Để tham chiếu đến một chức năng cụ thể được xác định bởi không gian tên cụ thể đó
* Khai báo biến - Để khai báo các biến cấp độ lớp cho việc thực hiện cụ thể
* Khai báo phương thức - Để khai báo khai báo phương thức cho chức năng cụ thể

## Ví dụ về định dạng tệp VB

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



