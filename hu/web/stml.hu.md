{
  "date" : "2021-05-20",
  "keywords" :[ "stml", "stml fájl", "stml fájlformátum", "stml fájltípus", "fájl", "típus", "mi az stml fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI HTML fájl",
  "description":"További információ az STML fájlformátumról és az STML-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Mi az STML fájl?

Az .stml kiterjesztésű fájl olyan szerveroldali utasításokat tartalmazó weboldal, amely akkor fut le, amikor a felhasználó betölti az oldalt a webböngészőbe. Az STML oldalak olyan szerveroldali kódot tartalmaznak, amely olyan kiszolgálóoldali kódokat tartalmaz, amelyek egyszerű HTML-kóddal nem megvalósíthatók. Bár hasonló a [HTML]-hez (/hu/web/html/), az STML nagyobb teljesítményt kínál a parancsok kiszolgálón való futtatásával, amelyet szerveroldali beépítésnek (SSI) is neveznek. Az új, szerveroldali szkriptekkel rendelkező programozási nyelvek, például a PHP bevezetésével az STML használata csökkent, bár továbbra is minden szerveroldali technológia támogatja. Az STML fájlok bármely szövegszerkesztőben megnyithatók és szerkeszthetők a parancsok frissítéséhez.

## STML fájl formátum

Az STML sima ascii szöveges fájlformátumon alapul, amely ember által olvasható. Azonban követi a szintaxist, ahogy azt a kiszolgáló oldalon végrehajtott [SSI-parancsok] (https://www.w3.org/Jigsaw/Doc/User/SSI.html) segítségével definiálják és gyakorolják. Mint minden más szerveroldali szkriptnyelv, az STML is használhatja a szerveroldali parancsokat olyan feladatok végrehajtására, mint az oldallátogatók számlálója, a weboldal naptár, a rekordok lekérése az adatbázisból és hasonlók.

## STML példa

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

