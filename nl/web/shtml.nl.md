{
  "date" : "2021-05-20",
  "keywords" :[ "shtml", "shtml-bestand", "shtml-bestandsindeling", "shtml-bestandstype", "bestand", "type", "wat is een shtml-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Serverzijde inclusief HTML-bestand",
  "description":"Meer informatie over SHTML-bestandsindelingen en API's die SHTML-bestanden kunnen maken en openen.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Wat is een SHTML-bestand?

Een bestand met de extensie .shtml is een webpagina die is geschreven in [HTML](/nl/web/html/) en serverinstructies bevat. Het kan ook server-side bevat die vergelijkbaar is met ASP-bestanden voor sneller laden. De server-side-bestanden kunnen ook uitvoerbare code bevatten waardoor de server langzamer kan laden dan normaal. SHTML-bestanden lijken op HTML, maar ze laten ook het gebruik van eenvoudige serveropdrachten toe. Deze serveropdrachten worden uitgevoerd in een eenvoudige computerprogrammeertaal genaamd Server Side Inclusief (SSI). SHTML is grotendeels vervangen door andere programmeertalen aan de serverzijde, zoals [PHP](/nl/programming/php/).

## SHTML-bestandsindeling

SHTML-bestanden zijn geschreven in platte tekst en gebruiken de [SSI-commando's](https://www.w3.org/Jigsaw/Doc/User/SSI.html) die aan de serverzijde worden uitgevoerd. Deze opdrachten aan de serverzijde kunnen worden gebruikt om zelfs verbinding te maken met de database met behulp van de databasestuurprogramma's en om gebruikersgegevens uit tabellen op te halen.

## SHTML-voorbeeld

Instructies aan de serverzijde worden gebruikt in toepassingen zoals voor paginabezoekerstellers of webpaginakalender. In het volgende voorbeeld worden de eerste vier kolommen van de eerste drie regels van de gebruikersdatabase weergegeven.

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
## Referenties

* [Server Side Inclusief](https://en.wikipedia.org/wiki/Server_Side_Includes)

