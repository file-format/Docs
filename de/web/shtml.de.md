{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","shtml-Datei", "shtml-Dateiformat", "shtml-Dateityp", "Datei", "Typ", "was ist eine shtml-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - HTML-Datei serverseitig einschließen",
  "description":"Erfahren Sie mehr über das SHTML-Dateiformat und APIs, die SHTML-Dateien erstellen und öffnen können.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Was ist eine SHTML-Datei?

Eine Datei mit der Erweiterung .shtml ist eine Webseite, die in [HTML](/de/web/html/) geschrieben ist und Serveranweisungen enthält. Es kann auch serverseitige Includes enthalten, die ASP-Dateien zum schnelleren Laden ähneln. Die serverseitigen Dateien können auch ausführbaren Code enthalten, der dazu führen kann, dass der Server langsamer als gewöhnlich lädt. SHTML-Dateien ähneln HTML, ermöglichen jedoch auch die Verwendung einfacher Serverbefehle. Diese Serverbefehle werden in einer einfachen Computerprogrammiersprache namens Server Side Includes (SSI) ausgeführt. SHTML wurde weitgehend von anderen serverseitigen Programmiersprachen wie [PHP](/de/programming/php/) Includes abgelöst.

## SHTML-Dateiformat

SHTML-Dateien sind im Klartext geschrieben und verwenden die [SSI-Befehle] (https://www.w3.org/Jigsaw/Doc/User/SSI.html), die serverseitig ausgeführt werden. Diese serverseitigen Befehle können verwendet werden, um mithilfe der Datenbanktreiber sogar eine Verbindung zur Datenbank herzustellen und Benutzerdaten aus Tabellen abzurufen.

## SHTML-Beispiel

Serverseitige Anweisungen werden in Anwendungen wie Seitenbesucherzähler oder Webseitenkalender verwendet. Das folgende Beispiel zeigt die ersten vier Spalten der ersten drei Zeilen der Benutzerdatenbank.

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
## Verweise

* [Server Side Includes] (https://en.wikipedia.org/wiki/Server_Side_Includes)

