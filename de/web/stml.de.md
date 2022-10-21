{
  "date" : "2021-05-20",
  "keywords" :[ "stml","stml-Datei", "stml-Dateiformat", "stml-Dateityp", "Datei", "Typ", "was ist eine stml-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI-HTML-Datei",
  "description":"Erfahren Sie mehr über das STML-Dateiformat und APIs, die STML-Dateien erstellen und öffnen können.",
  "linktitle" :"STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Was ist eine STML-Datei?

Eine Datei mit der Erweiterung .stml ist eine Webseite mit serverseitigen Anweisungen, die ausgeführt werden, wenn ein Benutzer die Seite im Webbrowser lädt. STML-Seiten enthalten serverseitigen Code, der serverseitige Includes enthält, um Aufgaben auszuführen, die mit einfachem HTML nicht möglich sind. Obwohl ähnlich wie [HTML](/de/web/html/), bietet STML mehr Leistung, indem es die Befehle auf dem Server ausführt, auch Server Side Includes (SSI) genannt. Mit der Einführung neuer Programmiersprachen mit serverseitiger Skripterstellung wie PHP wird die Verwendung von STML reduziert, obwohl es immer noch von allen serverseitigen Technologien unterstützt wird. STML-Dateien können in jedem Texteditor geöffnet und zum Aktualisieren der Befehle bearbeitet werden.

## STML-Dateiformat

STML basiert auf einem reinen ASCII-Textdateiformat, das für Menschen lesbar ist. Es folgt jedoch der Syntax, wie sie unter Verwendung der [SSI-Befehle] (https://www.w3.org/Jigsaw/Doc/User/SSI.html) definiert und ausgeübt wird, die serverseitig ausgeführt werden. Wie jede andere serverseitige Skriptsprache kann STML die serverseitigen Befehle verwenden, um Aufgaben wie Seitenbesucherzähler, Webseitenkalender, Abrufen von Datensätzen aus der Datenbank und ähnliches auszuführen.

## STML-Beispiel

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

