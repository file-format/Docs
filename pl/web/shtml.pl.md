{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","plik shtml", "format pliku shtml", "typ pliku shtml", "plik", "typ", "co to jest plik shtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - strona serwera zawiera plik HTML",
  "description":"Poznaj format pliku SHTML i interfejsy API, które mogą tworzyć i otwierać pliki SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Co to jest plik SHTML?

Plik z rozszerzeniem .shtml to strona internetowa napisana w [HTML](/pl/web/html/) i zawierająca instrukcje serwera. Może również zawierać elementy po stronie serwera podobne do plików ASP w celu szybszego ładowania. Pliki po stronie serwera mogą również zawierać kod wykonywalny, który może spowolnić ładowanie serwera. Pliki SHTML są podobne do HTML, ale umożliwiają również korzystanie z prostych poleceń serwera. Te polecenia serwera są wykonywane w prostym języku programowania komputerowego o nazwie Server Side Include (SSI). SHTML został w dużej mierze zastąpiony przez inne języki programowania po stronie serwera, takie jak [PHP](/pl/programming/php/).

## Format pliku SHTML

Pliki SHTML są zapisywane zwykłym tekstem i wykorzystują [polecenia SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html), które są wykonywane po stronie serwera. Te polecenia po stronie serwera mogą być używane nawet do łączenia się z bazą danych za pomocą sterowników bazy danych i pobierania danych użytkowników z tabel.

## Przykład SHTML

Instrukcje po stronie serwera są używane w aplikacjach, takich jak licznik odwiedzin strony lub kalendarz strony internetowej. Poniższy przykład wyświetla pierwsze cztery kolumny z pierwszych trzech wierszy bazy danych użytkowników.

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
## Bibliografia

* [Zawiera stronę serwera](https://en.wikipedia.org/wiki/Server_Side_Includes)

