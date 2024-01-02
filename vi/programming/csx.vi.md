{
"ngày": "2023-05-15",
  "keywords": [
"tệp csx",
"tệp csx là gì",
"tệp csx chứa gì",
"định dạng của tệp csx là gì",
"tài liệu",
"phần mở rộng tệp csx",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp CSX - Tập lệnh Visual C#",
  "description":"Tìm hiểu về định dạng CSX và các API có thể tạo và mở tệp CSX.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## Một tập tin CSX là gì?

Visual C# Script (còn được gọi là CSX) là định dạng tệp được sử dụng bởi công cụ tạo tập lệnh Roslyn trong hệ sinh thái .NET của Microsoft. Các tệp CSX chứa mã C# có thể được thực thi trực tiếp mà không cần bước biên dịch riêng.

Định dạng CSX dành riêng cho hệ sinh thái Microsoft và không phải là định dạng tệp được sử dụng rộng rãi trong lập trình chung. Các tệp CSX thường được sử dụng trong các tình huống yêu cầu chức năng tạo mẫu hoặc tạo tập lệnh nhanh. Chúng cho phép bạn tạo và chạy các chương trình C# theo cách nhẹ nhàng hơn so với việc tạo một ứng dụng được biên dịch chính thức.

Để thực thi các tệp CSX, bạn có thể sử dụng các công cụ như .NET Interactive Notebooks, công cụ này cung cấp môi trường tương tác để chạy mã C#. Visual Studio Code với phần mở rộng C# và .NET Core SDK cũng có thể được sử dụng để hoạt động với các tệp CSX.

## Tệp CSX chứa gì?

Tệp CSX (C# Script) chứa mã C# có thể được thực thi trực tiếp. Nó có thể bao gồm bất kỳ mã C# hợp lệ nào chẳng hạn như khai báo biến, hàm, lớp và các cấu trúc lập trình khác.

Dưới đây là ví dụ về nội dung tệp CSX có thể chứa:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

Các tệp CSX cũng có thể bao gồm các câu lệnh nhập, tham chiếu thư viện bên ngoài và các tính năng ngôn ngữ C# khác để hỗ trợ chức năng của mã. Mã được diễn giải và thực thi nhanh chóng mà không cần biên dịch, khiến nó phù hợp với các tác vụ tạo kịch bản và tạo mẫu nhanh.

## Định dạng của tệp CSX là gì?

Định dạng CSX (C# Script) tuân theo định dạng dựa trên văn bản đơn giản. Nó thường có phần mở rộng tệp .csx để phân biệt với các tệp mã nguồn C# thông thường (.cs).

Các tệp CSX có thể được chỉnh sửa bằng bất kỳ trình soạn thảo văn bản hoặc môi trường phát triển tích hợp (IDE) nào hỗ trợ tô sáng cú pháp C#. Khi tệp CSX đã sẵn sàng, nó có thể được thực thi bằng các công cụ như .NET Interactive Notebooks, giao diện dòng lệnh .NET Core (CLI) hoặc IDE có hỗ trợ tập lệnh C#.

## Người giới thiệu
* [Lập trình C# với Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

