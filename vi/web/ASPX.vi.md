{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","tệp aspx", "định dạng tệp aspx", "loại tệp aspx", "tệp", "loại", "tệp aspx là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp ASPX",
  "description" :"Hướng dẫn định dạng tệp của bạn để tìm hiểu tệp ASPX là gì và các API có thể tạo và mở tệp ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Tệp ASPX là gì?

Một tệp có phần mở rộng .aspx là một trang web được tạo bằng Microsoft ASP.NET framework chạy trên các máy chủ web. ASPX là viết tắt của Active Server Pages Extended và các trang này được hiển thị trong trình duyệt web ở cuối người dùng khi URL được truy cập. Nó là sự kế thừa của công nghệ [ASP](/vi/web/asp/) cũng được tạo ở cuối máy chủ nhưng không sử dụng .NET framework. Các trang ASP.NET có thể chứa các tập lệnh [C#](/vi/programming/cs/) hoặc [VB.NET](/vi/programming/vb/) được máy chủ web dịch sang HTML để hiển thị cho người dùng trong trình duyệt web. Các trang ASPX còn được gọi là .NET Web Forms. Chúng có thể được mở và tạo bằng các ứng dụng như Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ và bất kỳ trình soạn thảo văn bản nào.

## Định dạng tệp ASPX

Biểu mẫu web ASP.NET dựa trên mô hình hướng sự kiện để tương tác với ứng dụng web. Trình duyệt, với tư cách là người dùng cuối, gửi một biểu mẫu web đến máy chủ và máy chủ sẽ trả về một trang đánh dấu đầy đủ hoặc trang HTML để phản hồi. Mô hình thành phần ASP.NET cung cấp mô hình đối tượng cho các trang ASPX. Mô hình này mô tả:

* Bản sao phía máy chủ của hầu hết các phần tử hoặc thẻ HTML, chẳng hạn như \<form> và \<input> .
* Điều khiển máy chủ, giúp phát triển giao diện người dùng phức tạp. Ví dụ: điều khiển Lịch hoặc điều khiển Gridview.

Các tệp ASPX sử dụng mô hình ASP.NET **Code Behind** để xây dựng các trang này.

### Mã Nội tuyến

Mã mẫu được nhúng nội tuyến trong trang ASPX và cung cấp tất cả chức năng để triển khai người dùng. Mã [C#](/vi/programming/cs/) sau biểu thị một trang ASP.NET mẫu bao gồm mã nội tuyến:

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### Mã ẩn

Mã có thể được viết và lưu trữ trong các tệp lớp riêng biệt để tách HTML khỏi logic trình bày. Điều này làm cho lớp trình bày độc lập với mã thực thi. Sau đây là mã phía sau để trình bày cho người dùng.

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

Việc triển khai C# của logic thực tế cho lớp trình bày như sau.

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## Người giới thiệu

* [ASP.NET WebApps - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

