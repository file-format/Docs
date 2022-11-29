{
  "date" : "2021-05-20",
  "keywords" :[ "stml","stml-fil", "stml-filformat", "stml-filtyp", "fil", "typ", "vad är en stml-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI HTML-fil",
  "description":"Läs mer om STML-filformat och API:er som kan skapa och öppna STML-filer.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Vad är STML fil?

En fil med filtillägget .stml är en webbsida med instruktioner på serversidan som exekveras när en användare laddar sidan i webbläsaren. STML-sidor innehåller kod på serversidan som innehåller serversidan inkluderar för att utföra uppgifter som inte är möjliga att uppnå med vanlig HTML. Även om det liknar [HTML](/sv/web/html/), erbjuder STML mer kraft genom att köra kommandon på servern, även kallad Server Side Includes (SSI). Med introduktionen av nya programmeringsspråk med serversidescripting som PHP, minskar användningen av STML även om det fortfarande stöds av all serversidesteknologi. STML-filer kan öppnas i valfri textredigerare och redigeras för att uppdatera kommandona.

## STML filformat

STML är baserat på vanligt ascii-textfilformat som är läsbart för människor. Den följer dock syntaxen som definieras och utövas med [SSI-kommandon](https://www.w3.org/Jigsaw/Doc/User/SSI.html) som körs på serversidan. Liksom alla andra skriptspråk på serversidan kan STML använda kommandon på serversidan för att utföra uppgifter som sidbesökarräknare, webbsideskalender, hämta poster från databasen och liknande andra.

## Exempel på STML

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

