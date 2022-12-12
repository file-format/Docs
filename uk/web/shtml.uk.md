{
  "date" : "2021-05-20",
  "keywords" :[ "shtml", "файл shtml", "формат файлу shtml", "тип файлу shtml", "файл", "тип", "що таке файл shtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Включити файл HTML на стороні сервера",
  "description":"Дізнайтеся про формат файлу SHTML та API, які можуть створювати та відкривати файли SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Що таке файл SHTML?

Файл із розширенням .shtml — це веб-сторінка, написана мовою [HTML](/uk/web/html/) і містить інструкції сервера. Він також може містити включення на стороні сервера, схожі на файли ASP для швидшого завантаження. Файли на стороні сервера також можуть містити виконуваний код, через який сервер завантажується повільніше, ніж зазвичай. Файли SHTML подібні до HTML, але вони також дозволяють використовувати прості команди сервера. Ці команди сервера виконуються простою мовою комп’ютерного програмування під назвою Server Side Includes (SSI). SHTML був значною мірою витіснений іншими серверними мовами програмування, такими як [PHP](/uk/programming/php/).

## Формат файлу SHTML

Файли SHTML написані у вигляді звичайного тексту та використовують [команди SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html), які виконуються на стороні сервера. Ці команди на стороні сервера можна використовувати навіть для підключення до бази даних за допомогою драйверів бази даних і отримання даних користувачів із таблиць.

## Приклад SHTML

Інструкції на стороні сервера використовуються в таких програмах, як лічильник відвідувачів сторінки або календар веб-сторінки. У наступному прикладі показано перші чотири стовпці з перших трьох рядків бази даних користувачів.

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
## Список літератури

* [Серверна сторона включає](https://en.wikipedia.org/wiki/Server_Side_Includes)

