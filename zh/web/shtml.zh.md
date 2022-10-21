{
  "date" : "2021-05-20",
  "keywords" :["shtml","shtml文件","shtml文件格式","shtml文件类型","文件","类型","什么是shtml文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - 服务器端包含 HTML 文件",
  "description":"了解 SHTML 文件格式和可以创建和打开 SHTML 文件的 API。",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## 什么是 .shtml 文件？

扩展名为 .shtml 的文件是用 [HTML](/zh/web/html/) 编写的网页，其中包含服务器指令。它还可能包含类似于 ASP 文件的服务器端包含以加快加载速度。服务器端文件还可以包含可以使服务器加载速度比平时慢的可执行代码。 SHTML 文件类似于 HTML，但它们也允许使用简单的服务器命令。这些服务器命令以一种称为服务器端包含 (SSI) 的简单计算机编程语言执行。 SHTML 已在很大程度上被其他服务器端编程语言所取代，例如 [PHP](/zh/programming/php/) 包括在内。

## SHTML 文件格式

SHTML 文件以纯文本形式编写，并使用在服务器端执行的 [SSI 命令](https://www.w3.org/Jigsaw/Doc/User/SSI.html)。这些服务器端命令甚至可用于使用数据库驱动程序连接到数据库并从表中获取用户数据。

## SHTML 示例

服务器端指令用于页面访问者计数器或网页日历等应用程序。以下示例显示用户数据库前三行的前四列。

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
## 参考

* [服务器端包含](https://en.wikipedia.org/wiki/Server_Side_Includes)

