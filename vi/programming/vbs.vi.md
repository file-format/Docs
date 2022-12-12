{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "file", "extension", "file format", "Visual Basic Script", "Programming Guide", "vbs example", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Tệp tập lệnh Visual Basic",
  "description":"Tìm hiểu về định dạng tệp VBS và API có thể tạo và mở tệp VBS.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Tệp VBS là gì?

VBS hoặc VBScript được kết nối với phiên bản tập lệnh của Microsoft Visual Basic. Trong môi trường máy tính, người dùng được phép truy cập và kiểm soát nhiều khía cạnh của nó. VBScript được phép sử dụng một mô hình có tên **Mô hình đối tượng thành phần** để sử dụng các phần tử và công cụ của môi trường. Môi trường này được chỉ định để làm việc và chạy VBScript.

Nó hoạt động tương tự như Javascript khi nó được khách hàng truy cập trong lĩnh vực phát triển Web. Nó cũng được sử dụng bởi các máy chủ để xử lý các trang web. Nó có thể được xem xét trong một số loại tệp kịch bản khác, chẳng hạn như các ứng dụng của [HTML](/vi/web/html/).


## Lược Sử ##

Nó được ra mắt lần đầu tiên vào năm 1996, như một phần của các công nghệ được Microsoft sử dụng được chỉ định cho Windows Scripts. Ban đầu, nó được phát triển đặc biệt để hỗ trợ các nhà phát triển Web. Cùng năm đó, trình khám phá của Microsoft Windows có tên là Internet Explorer được phát hành cùng với các tính năng của Visual Basic Script.

Với sự phát triển của công nghệ và sự phát triển web, nhiều phiên bản VBScript cùng với nhiều tính năng nâng cao đã được ra đời. Hơn nữa, trong năm tới, ngôn ngữ kịch bản này sẽ là một phần của Microsoft Windows với các tính năng mới.

## Đặc điểm kỹ thuật ##

Đối với các trang web ở phía máy chủ, các công cụ như **Active Server Pages** được sử dụng cùng với VBScript. Ngôn ngữ kịch bản này cũng có thể được sử dụng trong thành phần kịch bản của Windows. Các tệp của ngôn ngữ này được lưu trữ với phần mở rộng .vbs trong Windows.

Có nhiều cấu trúc điều khiển như vòng lặp được sử dụng trong mã của ngôn ngữ này. Nó cũng bao gồm các đối số là dòng lệnh và có thể được đặt tên hoặc không đặt tên. Các tệp của ngôn ngữ này có thể được lưu trữ đơn giản trong các thư mục hoặc trên màn hình nền của hệ điều hành Windows. Mặc dù không có môi trường phát triển tích hợp cụ thể cho các chương trình VBScript như Microsoft Script Editor cung cấp cơ sở phát triển ngôn ngữ này.

Khi VBScript được lưu trữ bởi máy chủ Script của Windows, nó cung cấp các tính năng khác nhau khá phổ biến đối với các ngôn ngữ viết kịch bản nhưng không có sẵn trong Visual Basic 6.0. Các tính năng liên quan đến truy cập dễ dàng hoặc trực tiếp liên quan đến Máy in mạng, đối số dòng lệnh được đặt tên và đặt tên, thiết bị xuất chuẩn và thiết bị xuất chuẩn, Chia sẻ mạng, Công cụ quản lý Windows, thông tin người dùng của mạng như tư cách thành viên nhóm, v.v.

## Ví dụ về định dạng tệp VBS ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Tài liệu tham khảo ##

* [VBS - theo Wikipedia](https://vi.wikipedia.org/wiki/VBScript)



