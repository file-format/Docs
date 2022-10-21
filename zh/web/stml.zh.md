{
  "date" : "2021-05-20",
  "keywords" :["stml","stml 文件","stml 文件格式","stml 文件类型","文件","类型","什么是 stml 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI HTML 文件",
  "description":"了解 STML 文件格式和可以创建和打开 STML 文件的 API。",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## 什么是一 .stml 文件？

扩展名为 .stml 的文件是带有服务器端指令的网页，当用户在 Web 浏览器中加载页面时会执行这些指令。 STML 页面包含服务器端代码，其中包含服务器端包含以执行使用纯 HTML 无法实现的任务。虽然类似于 [HTML](/zh/web/html/)，但 STML 通过在服务器上运行命令（也称为服务器端包含 (SSI)）来提供更多功能。随着 PHP 等带有服务器端脚本的新编程语言的引入，STML 的使用减少了，尽管它仍然受到所有服务器端技术的支持。 STML 文件可以在任何文本编辑器中打开并进行编辑以更新命令。

## STML 文件格式

STML 基于人类可读的纯 ascii 文本文件格式。但是，它遵循使用在服务器端执行的 [SSI 命令](https://www.w3.org/Jigsaw/Doc/User/SSI.html) 定义和执行的语法。与任何其他服务器端脚本语言一样，STML 可以使用服务器端命令来执行诸如页面访问者计数器、网页日历、从数据库中检索记录等任务。

## STML 示例

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

