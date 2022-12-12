{
  "date" : "2021-05-20",
  "keywords" :[ "shtml", "shtml fájl", "shtml fájlformátum", "shtml fájltípus", "fájl", "típus", "mi az shtml fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Szerveroldali HTML-fájlt tartalmaz",
  "description":"További információ az SHTML fájlformátumról és az SHTML-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Mi az SHTML fájl?

Az .shtml kiterjesztésű fájl egy [HTML](/hu/web/html/) nyelven írt weboldal, amely szerver utasításokat tartalmaz. A gyorsabb betöltés érdekében az ASP-fájlokhoz hasonló szerveroldali elemeket is tartalmazhat. A szerveroldali fájlok futtatható kódot is tartalmazhatnak, amely a szokásosnál lassabban töltheti be a szervert. Az SHTML fájlok hasonlóak a HTML-hez, de egyszerű szerverparancsok használatát is lehetővé teszik. Ezeket a kiszolgálóparancsokat egy egyszerű számítógépes programozási nyelven hajtják végre, az úgynevezett Server Side Includes (SSI). Az SHTML-t nagymértékben felváltották más szerveroldali programozási nyelvek, például a [PHP](/hu/programing/php/) tartalmazza.

## SHTML fájlformátum

Az SHTML-fájlok egyszerű szöveggel vannak írva, és az [SSI-parancsokat] (https://www.w3.org/Jigsaw/Doc/User/SSI.html) használják, amelyek a szerver oldalon futnak le. Ezekkel a szerveroldali parancsokkal még az adatbázis-illesztőprogramok segítségével is csatlakozhat az adatbázishoz, és lekérheti a felhasználók adatait a táblákból.

## SHTML példa

A szerveroldali utasítások olyan alkalmazásokban használatosak, mint például az oldallátogatói számláló vagy a weboldal naptár. A következő példa a felhasználói adatbázis első három sorának első négy oszlopát jeleníti meg.

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
## Hivatkozások

* [Server Side Includes](https://en.wikipedia.org/wiki/Server_Side_Includes)

