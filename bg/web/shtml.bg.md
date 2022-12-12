{
  "date" : "2021-05-20",
  "keywords" :[ "shtml", "shtml файл", "shtml файлов формат", "shtml тип файл", "файл", "тип", "какво е shtml файл" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML – Включване на HTML файл от страна на сървъра",
  "description":"Научете за SHTML файловия формат и API, които могат да създават и отварят SHTML файлове.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Какво е SHTML файл?

Файл с разширение .shtml е уеб страница, която е написана на [HTML](/bg/web/html/) и включва инструкции на сървъра. Може също да съдържа включвания от страна на сървъра, подобни на ASP файлове за по-бързо зареждане. Файловете от страна на сървъра могат също да съдържат изпълним код, който може да накара сървъра да се зарежда по-бавно от обикновено. SHTML файловете са подобни на HTML, но също така позволяват използването на прости сървърни команди. Тези сървърни команди се изпълняват на прост език за компютърно програмиране, наречен Server Side Includes (SSI). SHTML до голяма степен е заменен от други езици за програмиране от страна на сървъра, като например [PHP](/bg/programming/php/).

## SHTML файлов формат

SHTML файловете са написани в обикновен текст и използват [SSI командите](https://www.w3.org/Jigsaw/Doc/User/SSI.html), които се изпълняват от страна на сървъра. Тези команди от страна на сървъра могат да се използват дори за свързване към база данни с помощта на драйверите на базата данни и извличане на потребителски данни от таблици.

## Пример за SHTML

Инструкциите от страна на сървъра се използват в приложения, като например за брояч на посетители на страница или календар на уеб страница. Следващият пример показва първите четири колони от първите три реда на потребителската база данни.

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
## Препратки

* [Сървърната страна включва](https://en.wikipedia.org/wiki/Server_Side_Includes)

