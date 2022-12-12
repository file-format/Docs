{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp HTX - Định dạng tệp mở rộng HTML",
  "description" :"Hướng dẫn định dạng tệp của bạn để tìm hiểu tệp HTX là gì và các API có thể tạo và mở tệp HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp HTX là gì?

Tệp HTX thực sự là một tệp HTML chứa các biến dữ liệu để hiển thị kết quả truy vấn cơ sở dữ liệu dưới dạng trang web. Hầu hết được tạo bằng phần mềm phát triển Web Microsoft FrontPage, các tệp HTX được lưu vào cùng thư mục với tệp Trình kết nối cơ sở dữ liệu Internet (.IDC) tương ứng.

Các tệp HTX có thể được mở bằng các ứng dụng như Microsoft FrontPage và bất kỳ trình soạn thảo văn bản nào như Notepad, TextEdit hoặc Atom.

## Định dạng tệp HTX

Các tệp HTX được lưu dưới dạng tệp văn bản thuần túy có mã để truy xuất dữ liệu từ cơ sở dữ liệu và lưu vào các biến để hiển thị.


### Ví dụ về tệp HTX

Một ví dụ về tệp HTX như sau xác định tiêu đề trang để hiển thị giới hạn truy vấn và các tài liệu được hiển thị trên trang để hiển thị cho người dùng.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

Đầu ra của mã mẫu này như sau.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Có thể thấy, tệp HTX là một khuôn mẫu định dạng cách kết quả được trả về và hiển thị cho người dùng cuối. Nó được viết ở định dạng HTML với một số tiện ích mở rộng IIS và Dịch vụ lập chỉ mục. Các phần mở rộng này bao gồm tên biến và các mã khác để xử lý kết quả.

## Người giới thiệu

* [Định dạng kết quả trong tệp .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

