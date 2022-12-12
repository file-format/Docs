{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "file", "extension", "file format", "CSharp", "Programming Language" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - Tệp mã CSharp",
  "description":"Tìm hiểu về định dạng tệp CS và các API có thể tạo và mở tệp CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp CS là gì?

Các tệp có phần mở rộng .cs là các tệp mã nguồn cho ngôn ngữ lập trình C#. Được Microsoft giới thiệu để sử dụng với .NET Framework, định dạng tệp cung cấp ngôn ngữ lập trình cấp thấp để viết mã được biên dịch để tạo tệp đầu ra cuối cùng ở dạng EXE hoặc DLL. Chúng có thể được tạo và biên dịch bằng Microsoft Visual Studio. Microsoft Visual Studio Express cũng có thể được sử dụng để tạo và cập nhật các tệp như vậy, đây là một IDE miễn phí. Các tệp CS được sử dụng để phát triển ứng dụng có thể bao gồm từ các ứng dụng máy tính để bàn đơn giản đến các chương trình phức tạp hơn. Một dự án Visual Studio đơn giản [giải pháp](/vi/programming/sln/) được tạo bằng ngôn ngữ C# có thể bao gồm một hoặc nhiều tệp như vậy. Các tệp được đánh dấu để đưa vào quá trình biên dịch được liệt kê trong tệp [CSPROJ](/vi/programming/csproj/) là một phần của dự án và yêu cầu trình biên dịch sử dụng các tệp được đánh dấu.

## Định dạng tệp CS ##

Tệp CS là định dạng tệp dựa trên văn bản có thể được mở trong bất kỳ trình soạn thảo văn bản nào để chỉnh sửa. Tuy nhiên, khi được mở trong một IDE được hỗ trợ với cú pháp tô sáng thích hợp, mã sẽ dễ đọc và sắp xếp. Một tệp CS đơn giản chứa:

* Khai báo không gian tên - Để tham chiếu đến một chức năng cụ thể được xác định bởi không gian tên cụ thể đó
* Khai báo biến - Để khai báo các biến cấp độ lớp cho việc thực hiện cụ thể
* Khai báo phương thức - Để khai báo khai báo phương thức cho chức năng cụ thể

### Cú pháp ###

* Dấu chấm phẩy dùng để kết thúc câu lệnh.
* Dấu ngoặc nhọn dùng để nhóm các câu lệnh. Các câu lệnh thường được nhóm thành các phương thức (hàm), các phương thức thành các lớp và các lớp thành các không gian tên.
* Các biến được gán bằng dấu bằng, nhưng được so sánh bằng hai dấu bằng liên tiếp.
* Dấu ngoặc vuông được sử dụng với các mảng, cả để khai báo chúng và để nhận giá trị tại một chỉ mục đã cho trong một trong số chúng.

### Thí dụ ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

