{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","shtml-fil", "shtml-filformat", "shtml-filtyp", "fil", "typ", "vad är en shtml-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Server Side Include HTML File",
  "description":"Läs mer om SHTML-filformat och API:er som kan skapa och öppna SHTML-filer.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Vad är en SHTML-fil?

En fil med tillägget .shtml är en webbsida som är skriven i [HTML](/sv/web/html/) och inkluderar serverinstruktioner. Det kan också innehålla server-side inkluderar liknande ASP-filer för snabbare laddning. Serversidans filer kan också innehålla körbar kod som kan få servern att laddas långsammare än vanligt. SHTML-filer liknar HTML men de tillåter också användning av enkla serverkommandon. Dessa serverkommandon utförs i ett enkelt datorprogrammeringsspråk som kallas Server Side Includes (SSI). SHTML har till stor del ersatts av andra programmeringsspråk på serversidan som [PHP](/sv/programming/php/) inkluderar.

## SHTML filformat

SHTML-filer skrivs i vanlig text och använder [SSI-kommandon](https://www.w3.org/Jigsaw/Doc/User/SSI.html) som körs på serversidan. Dessa kommandon på serversidan kan användas för att till och med ansluta till databasen med hjälp av databasdrivrutinerna och hämta användardata från tabeller.

## Exempel på SHTML

Instruktioner på serversidan används i applikationer som för sidbesökarräknare eller webbsidekalender. Följande exempel visar de fyra första kolumnerna i de första tre raderna i användardatabasen.

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
## Referenser

* [Server Side Includes](https://en.wikipedia.org/wiki/Server_Side_Includes)

