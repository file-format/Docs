{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","tệp shtml", "định dạng tệp shtml", "loại tệp shtml", "tệp", "loại", "tệp shtml là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Phía máy chủ bao gồm tệp HTML",
  "description":"Tìm hiểu về định dạng tệp SHTML và các API có thể tạo và mở tệp SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Tệp SHTML là gì?

Tệp có phần mở rộng .shtml là một trang web được viết bằng [HTML](/vi/web/html/) và bao gồm các hướng dẫn của máy chủ. Nó cũng có thể chứa các tệp phía máy chủ tương tự như các tệp ASP để tải nhanh hơn. Các tệp phía máy chủ cũng có thể chứa mã thực thi có thể khiến máy chủ tải chậm hơn bình thường. Các tệp SHTML tương tự như HTML nhưng chúng cũng cho phép sử dụng các lệnh máy chủ đơn giản. Các lệnh máy chủ này được thực hiện bằng ngôn ngữ lập trình máy tính đơn giản có tên là Bao gồm phía máy chủ (SSI). SHTML đã được thay thế phần lớn bởi các ngôn ngữ lập trình phía máy chủ khác, chẳng hạn như [PHP](/vi/programming/php/) bao gồm.

## Định dạng tệp SHTML

Các tệp SHTML được viết bằng văn bản thuần túy và sử dụng [lệnh SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) được thực thi ở phía máy chủ. Các lệnh phía máy chủ này có thể được sử dụng để thậm chí kết nối với cơ sở dữ liệu bằng trình điều khiển cơ sở dữ liệu và tìm nạp dữ liệu người dùng từ các bảng.

## Ví dụ SHTML

Hướng dẫn phía máy chủ được sử dụng trong các ứng dụng như bộ đếm khách truy cập trang hoặc lịch trang web. Ví dụ sau, hiển thị bốn cột đầu tiên trong ba dòng đầu tiên của cơ sở dữ liệu người dùng.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## Người giới thiệu

* [Bao gồm phía máy chủ](https://en.wikipedia.org/wiki/Server_Side_Includes)

