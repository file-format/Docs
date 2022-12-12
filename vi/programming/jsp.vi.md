{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Định dạng tệp trang máy chủ Java",
  "description":"Tìm hiểu về định dạng tệp JSP với ví dụ về JSP và các API có thể tạo và mở tệp JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Tệp JSP là gì?
Các tệp JSP được hiện thực hóa dưới dạng các trang động, dựa trên dữ liệu cho các ứng dụng web Java của bạn. JSP có nghĩa là Trang máy chủ Java; có thể được nhận ra như một phần mở rộng cho Servlet vì nó cho phép nhiều chức năng hơn servlet, chẳng hạn như ngôn ngữ biểu thức. JSP và Servlet thực hiện cùng một công việc trong các ứng dụng web Java cũ hơn. Từ góc độ lập trình, sự khác biệt rõ ràng nhất giữa chúng là với servlet bạn viết chương trình Java và sau đó nhúng phần đánh dấu tĩnh (như HTML) vào mã đó, trong khi đó, JSP bắt đầu với tập lệnh hoặc phần đánh dấu phía máy khách, sau đó nhúng các thẻ JSP vào kết nối trang của bạn với chương trình phụ trợ Java.

## Định dạng tệp JSP
Một tệp được lưu với phần mở rộng tệp **jsp** chứa các phần sau theo thứ tự chúng được liệt kê:

1. Lời mở đầu
2. (Các) chỉ thị trang JSP
3. (Các) chỉ thị thư viện thẻ tùy chọn
4. (Các) khai báo JSP tùy chọn
5. Mã HTML và JSP

### Bình Luận Mở Đầu
Tệp JSP hoặc tệp phân đoạn bắt đầu bằng nhận xét kiểu phía máy chủ:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Nhận xét trên chỉ xuất hiện ở phía máy chủ vì nó bị xóa trong khi hiển thị trang trong trình duyệt. Nhận xét có thể chứa thông tin về (các) tác giả, ngày tháng và thông báo bản quyền của bản sửa đổi, mã định danh và mô tả về trang JSP dành cho nhà phát triển. Việc kết hợp các ký tự " @(#)" được một số chương trình nhận dạng để biểu thị phần bắt đầu của mã định danh.

### (Các) Chỉ thị Trang JSP
Chỉ thị trang JSP xác định các thuộc tính được liên kết với trang JSPF tại thời điểm dịch. Đặc tả JSP không đặt ra ràng buộc về số lượng chỉ thị trang JSP có thể được viết trong một trang. Xem ví dụ sau:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Nếu một chỉ thị trang, vượt quá chiều rộng bình thường của một trang JSP, thì chỉ thị đó được chia thành nhiều dòng:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### (Các) Chỉ thị Thư viện Thẻ Tùy chọn
Trong trang JSP, chỉ thị thư viện thẻ khai báo các thư viện thẻ tùy chỉnh. Một chỉ thị ngắn có thể được khai báo trong một dòng. Nhiều chỉ thị thư viện thẻ được xếp chồng lên nhau ở cùng một vị trí trong nội dung của trang JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### (Các) khai báo JSP tùy chọn
  


Các phương thức và biến được khai báo trong tệp JSPF phải tồn tại trong các khai báo JSP. Các phương thức và biến này tương tự như các khai báo trong ngôn ngữ lập trình Java và đó là lý do tại sao phải tuân theo các quy ước mã có liên quan. Các khai báo thường được viết bằng một dấu < %! ... %> Khối khai báo JSP, để tập trung các khai báo trong một khu vực của nội dung trang JSP. xem các ví dụ sau:

#### Các khối khai báo khác nhau:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Khối khai báo ưu tiên:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Mã HTML và JSP
Phần này của một trang JSP chứa phần thân HTML của trang JSP và mã JSPF, chẳng hạn như các biểu thức JSP, tập lệnh và hướng dẫn JavaBeans.

## Vòng đời của một trang JSP

Luồng trang JSP theo từng giai đoạn được đưa ra ở đây:

- Dịch Trang JSP
- Biên dịch Trang JSP
- Tải lớp (trình tải lớp tải tệp lớp)
- Instantiation (Đối tượng của Servlet đã tạo được tạo).
- Khởi tạo ( bộ chứa gọi phương thức jspInit()).
- Xử lý yêu cầu ( bộ chứa gọi phương thức _jspService() ).
- Phá hủy ( bộ chứa gọi phương thức jspDestroy()).

{{< figure src="../jsp.jpg" alt="Định dạng tệp JSP" >}}

## Ví dụ JSP

Ngày nay, việc tìm hiểu về các công nghệ JSP rất dễ dàng vì có rất nhiều hướng dẫn về JSP có sẵn trên internet. Ví dụ JSP sau đây dùng để xử lý đơn đặt hàng, bằng cách cập nhật các bản ghi thích hợp trong cơ sở dữ liệu.
```
<html>
<head>
  <title>Order Book</title>
</head>
 

<body>
  <h1>Another E-Bookstore</h1>
  <h2>Thank you for ordering...</h2>
 

  <%
    String[] ids = request.getParameterValues("id");
    if (ids != null) {
  %>
  <%@ page import = "java.sql.*" %>
  <%
      Connection conn = DriverManager.getConnection(
          "jdbc:mysql://localhost:8888/ebookshop", "myuser", "xxxx"); // <== Check!
      // Connection conn =
      //    DriverManager.getConnection("jdbc:odbc:eshopODBC");  // Access
      Statement stmt = conn.createStatement();
      String sqlStr;
      int recordUpdated;
      ResultSet rset;
  %>
      <table border=1 cellpadding=3 cellspacing=0>
        <tr>
          <th>Author</th>
          <th>Title</th>
          <th>Price</th>
          <th>Qty In Stock</th>
        </tr>
  <%
      for (int i = 0; i < ids.length; ++i) {
        // Subtract the QtyAvailable by one
        sqlStr = "UPDATE books SET qty = qty - 1 WHERE id = " + ids[i];
        recordUpdated = stmt.executeUpdate(sqlStr);
        // carry out a query to confirm
        sqlStr = "SELECT * FROM books WHERE id =" + ids[i];
        rset = stmt.executeQuery(sqlStr);
        while (rset.next()) {
  %>
          <tr>
            <td><%= rset.getString("author") %></td>
            <td><%= rset.getString("title") %></td>
            <td>$<%= rset.getInt("price") %></td>
            <td><%= rset.getInt("qty") %></td>
          </tr>
  <%}
        rset.close();
  }
      stmt.close();
      conn.close();
}
  %>
  </table>
  <a href="query.jsp"><h3>BACK</h3></a>
</body>
</html>
```


 


## Người giới thiệu

* [Quy ước mã cho các trang JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Hướng dẫn JSP](https://www.javatpoint.com/jsp-tutorial)

