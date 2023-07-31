{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","tệp cshtml", "định dạng tệp cshtml", "loại tệp cshtml", "tệp", "loại", "tệp cshtml là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - Trang web ASP.NET Razor",
  "description":"Tìm hiểu về định dạng tệp CSHTML và API có thể tạo và mở tệp CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Tệp CSHTML là gì?

Tệp có phần mở rộng .cshtml là tệp HTML [C#](/vi/programming/cs/) được công cụ Razor Markup sử dụng ở phía máy chủ để hiển thị tệp trang web cho trình duyệt của người dùng. Mã hóa phía máy chủ này tương tự như trang ASP.NET tiêu chuẩn cho phép tạo nội dung web động một cách nhanh chóng khi trang web được ghi vào trình duyệt. Máy chủ thực thi mã phía máy chủ bên trong trang trước khi gửi trang được tạo tới trình duyệt. Các tác vụ phức tạp như truy cập cơ sở dữ liệu và hiển thị các chế độ xem phức tạp. Các tệp CSHTML có thể được tạo và lập trình bằng Microsoft Visual Studio.

## Định dạng tệp CSHTML

Các tệp CSHTML là các tệp văn bản tuân theo cú pháp được vạch ra bởi công cụ đánh dấu Razor. Razor hỗ trợ cả C# và VB.NET, đồng thời dễ học và dễ sử dụng hơn ASP và ASP.NET cổ điển. w3schools có một hướng dẫn đơn giản nhưng hiệu quả về mã hóa [cú pháp của C# và VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) của Razor.

### Ví dụ CSHTML

Sau đây là ví dụ Mã C# được sử dụng trong tệp CSHTML cho Razor.

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

Mã VB.NET tương đương cho Razor như sau.

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## Người giới thiệu

* [Tham khảo cú pháp dao cạo - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

