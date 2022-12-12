{
  "date" : "2021-05-20",
  "keywords" :[ "stml","tệp stml", "định dạng tệp stml", "loại tệp stml", "tệp", "loại", "tệp stml là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - Tệp HTML SSI",
  "description":"Tìm hiểu về định dạng tệp STML và các API có thể tạo và mở tệp STML.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Tệp STML là gì?

Tệp có phần mở rộng .stml là một trang web có hướng dẫn phía máy chủ được thực thi khi người dùng tải trang trong trình duyệt web. Các trang STML chứa mã phía máy chủ có chứa phía máy chủ bao gồm để thực hiện các tác vụ không thể đạt được bằng HTML thuần túy. Mặc dù tương tự như [HTML](/vi/web/html/), STML cung cấp nhiều sức mạnh hơn bằng cách chạy các lệnh trên máy chủ, còn được gọi là Bao gồm phía máy chủ (SSI). Với sự ra đời của các ngôn ngữ lập trình mới với kịch bản phía máy chủ như PHP, việc sử dụng STML đã giảm đi mặc dù nó vẫn được hỗ trợ bởi tất cả các công nghệ phía máy chủ. Các tệp STML có thể được mở trong bất kỳ trình soạn thảo văn bản nào và được chỉnh sửa để cập nhật các lệnh.

## Định dạng tệp STML

STML dựa trên định dạng tệp văn bản ascii đơn giản mà con người có thể đọc được. Tuy nhiên, nó tuân theo cú pháp như đã xác định và được thực hiện bằng cách sử dụng [lệnh SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) được thực thi ở phía máy chủ. Giống như bất kỳ ngôn ngữ kịch bản phía máy chủ nào khác, STML có thể sử dụng các lệnh phía máy chủ để thực hiện các tác vụ như bộ đếm khách truy cập trang, lịch trang web, truy xuất bản ghi từ cơ sở dữ liệu và các tác vụ tương tự khác.

## Ví dụ STML

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

