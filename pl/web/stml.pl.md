{
  "date" : "2021-05-20",
  "keywords" :[ "stml", "plik stml", "format pliku stml", "typ pliku stml", "plik", "typ", "co to jest plik stml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - Plik HTML SSI",
  "description":"Poznaj format pliku STML i interfejsy API, które mogą tworzyć i otwierać pliki STML.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Czym jest plik STML?

Plik z rozszerzeniem .stml to strona internetowa z instrukcjami po stronie serwera, które są wykonywane, gdy użytkownik ładuje stronę w przeglądarce internetowej. Strony STML zawierają kod po stronie serwera, który zawiera elementy po stronie serwera do wykonywania zadań, których nie można osiągnąć za pomocą zwykłego kodu HTML. Chociaż podobny do [HTML](/pl/web/html/), STML oferuje więcej możliwości, uruchamiając polecenia na serwerze, zwane także dołączaniem po stronie serwera (SSI). Wraz z wprowadzeniem nowych języków programowania ze skryptami po stronie serwera, takich jak PHP, użycie STML jest ograniczone, chociaż nadal jest obsługiwane przez wszystkie technologie po stronie serwera. Pliki STML można otwierać w dowolnym edytorze tekstu i edytować w celu aktualizacji poleceń.

## Format pliku STML

STML jest oparty na prostym formacie pliku tekstowego ASCII, który jest czytelny dla człowieka. Jednak jest zgodny ze składnią zdefiniowaną i wykonaną za pomocą [poleceń SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html), które są wykonywane po stronie serwera. Jak każdy inny język skryptowy po stronie serwera, STML może używać poleceń po stronie serwera do wykonywania zadań, takich jak licznik odwiedzających stronę, kalendarz strony internetowej, pobieranie rekordów z bazy danych i podobne.

## Przykład STML

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

