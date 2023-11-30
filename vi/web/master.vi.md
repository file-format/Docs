{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp MASTER - Định dạng tệp trang chính ASP.NET",
  "description" :"Tìm hiểu về Định dạng tệp MASTER và API để tạo và mở tệp MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Tập tin MASTER là gì?

Tệp MASTER là tệp mẫu trang web chính được tạo bằng ASP.NET. Nó được sử dụng làm điểm bắt đầu để tạo nhiều trang có cùng bố cục và cài đặt như tệp MASTER. Tệp MASTER mẫu bao gồm các cài đặt cho thông tin về tiêu đề, menu điều hướng, chân trang, phông chữ và kiểu dáng. Sử dụng tệp MASTER giúp tạo nhiều trang web một cách nhanh chóng.

Bạn có thể mở tệp MASTER bằng Microsoft Visual Studio 2022 trở lên.

## Định dạng tệp MASTER - Thông tin thêm

Tệp MASTER được tạo và lưu ở định dạng tệp HTML và tương tự như bất kỳ tệp trang web nào khác. Nó được phân chia thành các phần có thể chỉnh sửa và không thể chỉnh sửa. Các phần có thể chỉnh sửa là những phần có thể được sửa đổi để đáp ứng yêu cầu của người dùng. Các phần không thể chỉnh sửa sẽ chuyển sang màu xám khi tệp MASTER được mở trong Microsoft Visual Studio.

Trang chính bao gồm hai phần tức là trang chính và một hoặc nhiều trang nội dung.

### Trang CHÍNH

Trang chính có phần mở rộng .master và được tạo bằng ASP.NET. Nó có bố cục được xác định trước bao gồm văn bản tĩnh, thẻ HTML và điều khiển phía máy chủ. Trong các trang .aspx thông thường, lệnh @ Page được sử dụng. Trong trường hợp tệp .master, điều này được thay thế bằng lệnh @ Master.

### Trang nội dung

Trang nội dung thể hiện nội dung cho các điều khiển giữ chỗ của trang chính. Đây là các trang .aspx thực sự là mã phía sau của trang chính. Các trang nội dung được liên kết bằng cách sử dụng chỉ thị @ Trang bằng cách bao gồm thuộc tính MasterPageFile trỏ đến trang chính sẽ được sử dụng như hiển thị bên dưới.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Người giới thiệu

* [Tổng quan về các trang chính của ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

