{
  "date" : "2019-10-11",
  "keywords" :[ "asax","tệp asax", "định dạng tệp asax", "loại tệp asax", "tệp", "loại", "tệp asax là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - Tệp ứng dụng máy chủ ASP.NET",
  "description" :"Tìm hiểu để biết tệp ASAX là gì và các API có thể tạo và mở tệp ASAX.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Tệp ASAX là gì?

Tệp có phần mở rộng .asax là tệp được sử dụng bởi các ứng dụng ASP.NET nằm ở phía máy chủ. Nó chứa mã để phản hồi các sự kiện cấp ứng dụng và cấp phiên do ASP.NET hoặc các mô-đun HTTP đưa ra. Điều này cũng bao gồm việc xử lý các sự kiện nhất định khi ứng dụng khởi chạy hoặc tắt. Các tệp ASAX là tùy chọn và chỉ một tệp ASAX duy nhất được thêm vào các ứng dụng web để xử lý các sự kiện và lỗi cấp ứng dụng ở cấp độ toàn cầu. Không giống như các trang ASPX, các tệp ASAX không chứa bất kỳ mã nào để triển khai chức năng của ứng dụng.

## Định dạng tệp ASAX

Các tệp ASAX được viết ở định dạng tệp văn bản thuần túy và con người có thể đọc được. Tệp ASAX được sử dụng phổ biến nhất là Global.asax nằm trong thư mục gốc của ứng dụng ASP.NET. Máy chủ web được định cấu hình để từ chối mọi cuộc gọi đến tệp này để cấm người dùng tải xuống hoặc xem mã của tệp này.

### Global.ASAX - Ví dụ về Định dạng Tệp ASAX

Một tệp ASAX duy nhất bao gồm nhiều phần được viết để xử lý các sự kiện cấp ứng dụng. Đây là như sau.

* **Chỉ thị ứng dụng** - Chỉ thị ứng dụng là các thẻ được sử dụng để xác định cài đặt tùy chọn dành riêng cho ứng dụng sẽ được trình phân tích cú pháp ASP.NET sử dụng khi xử lý tệp Global.asax. Các lệnh này nằm ở phần đầu của tệp Global.asax và được định nghĩa như sau.

```
<%@ chỉ thị thuộc tính=giá trị [thuộc tính=giá trị … ]%>
```
* **Khối khai báo mã** - Khối khai báo mã được sử dụng để xác định các phần mã máy chủ được nhúng trong tệp ứng dụng ASP.NET trong thư mục \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Khối kết xuất mã** - Những khối này xác định mã hoặc biểu thức nội tuyến sẽ thực thi khi trang được hiển thị. Hai kiểu khối kết xuất mã bao gồm mã nội tuyến và biểu thức nội tuyến. Cái trước được sử dụng để xác định các dòng hoặc khối mã độc lập, trong khi cái bên được sử dụng làm lối tắt để gọi phương thức Viết.

## Người giới thiệu

* [Tổng quan về trình xử lý HTTP và mô-đun HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Cú pháp Global.asax](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

