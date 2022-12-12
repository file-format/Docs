{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - Định dạng tệp đoạn JSP",
  "description":"Tìm hiểu về định dạng tệp JSPF và API có thể tạo và mở tệp JSPF.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Tệp JSPF là gì?
Tệp có phần mở rộng .jspf được gọi là đoạn JSP; một tệp tĩnh được bao gồm trong một tệp JSP khác. Các tệp JSPF không được biên dịch riêng, tuy nhiên, chúng được biên dịch dọc theo trang chứa chúng. Cú pháp của nó tương tự như mã Trang máy chủ Java (JSP). Nó chỉ chứa một đoạn JSP; không bao gồm tất cả toàn bộ tài liệu JSP.

## Định dạng tệp JSPF
Thuật ngữ "phân đoạn JSP" được sử dụng thay vì thuật ngữ "đoạn JSP" bị quá tải trong Đặc tả JSP 2.0. Các đoạn JSP có thể sử dụng phần mở rộng .jsp hoặc .jspf và phải được đặt trong **/WEB-INF/jspf** hoặc với phần còn lại của tệp tĩnh. Các đoạn JSP không phải là trang hoàn chỉnh phải sử dụng phần mở rộng .jspf và phải được đặt trong **/WEB-INF/jspf**

### Tổ chức tệp phân đoạn JSP hoặc JSP
Một tệp JSP chứa các phần sau đây theo thứ tự chúng được liệt kê:

1. Lời mở đầu
2. (Các) chỉ thị trang JSP
3. (Các) chỉ thị thư viện thẻ tùy chọn
4. (Các) khai báo JSP tùy chọn
5. Mã HTML và JSP

Một tệp JSP hoặc JSPF đều bắt đầu bằng một nhận xét kiểu phía máy chủ được gọi là **Nhận xét mở đầu**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Nhận xét này chỉ có thể hiển thị ở phía máy chủ vì nó bị xóa trong quá trình hiển thị trang JSP.

## Khi nào nên sử dụng tệp JSP Fragment?
Khi một trang JSP yêu cầu một cấu trúc nhất định nhưng phức tạp, cấu trúc này cũng có thể được sử dụng lại trong các trang JSP khác, một cách để xử lý việc này là chia nhỏ nó thành nhiều phần, sử dụng mẫu Chế độ xem tổng hợp (phần Mẫu của Bản thiết kế Java). Ví dụ: một trang JSP đôi khi có bố cục hợp lý sau trong cấu trúc trình bày của nó:

{{< figure src="../jspf.png" alt="Định dạng tệp JSPF" >}}

Trong tình huống này, trang JSP tổng hợp này có thể được chuyển đổi thành nhiều mô-đun khác nhau, mỗi mô-đun sẽ được gọi là một đoạn JSP riêng biệt. Các đoạn JSP sau đó có thể được đặt ở các vị trí thích hợp trong trang JSP tổng hợp. Do đó, tệp JSPF được sử dụng khi các lệnh bao gồm tĩnh được sử dụng để bao gồm một trang không được gọi bởi chính nó, các tệp có phần mở rộng .jspf phải được đặt trong thư mục /WEB-INF/jspf/ của kho lưu trữ ứng dụng Web ( chiến tranh).

## Ví dụ về JSPF
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Người giới thiệu

* [Quy ước mã cho các trang JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

