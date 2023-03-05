{
  "date" : "2021-05-20",
  "keywords" :[ "shtml", "файл shtml", "формат файла shtml", "тип файла shtml", "файл", "тип", "что такое файл shtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML — серверная часть включает HTML-файл",
  "description":"Узнайте о формате файла SHTML и API-интерфейсах, которые могут создавать и открывать файлы SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## .SHTML вариант №

Файл с расширением .shtml представляет собой веб-страницу, написанную на [HTML](/ru/web/html/) и содержащую инструкции для сервера. Он также может содержать включения на стороне сервера, аналогичные файлам ASP, для более быстрой загрузки. Файлы на стороне сервера также могут содержать исполняемый код, из-за которого сервер загружается медленнее, чем обычно. Файлы SHTML похожи на HTML, но также позволяют использовать простые серверные команды. Эти серверные команды выполняются на простом языке компьютерного программирования, который называется включением на стороне сервера (SSI). SHTML был в значительной степени вытеснен другими серверными языками программирования, такими как [PHP](/ru/programming/php/).

## Формат файла SHTML

Файлы SHTML записываются в виде обычного текста и используют [команды SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html), которые выполняются на стороне сервера. Эти команды на стороне сервера можно использовать даже для подключения к базе данных с помощью драйверов базы данных и извлечения пользовательских данных из таблиц.

## Пример SHTML

Инструкции на стороне сервера используются в таких приложениях, как счетчик посетителей страницы или календарь веб-страницы. В следующем примере отображаются первые четыре столбца первых трех строк базы данных пользователей.

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
## использованная литература

* [Включает серверную часть](https://en.wikipedia.org/wiki/Server_Side_Includes)

