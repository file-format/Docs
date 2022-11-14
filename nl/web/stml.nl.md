{
  "date" : "2021-05-20",
  "keywords" :[ "stml","stml-bestand", "stml-bestandsformaat", "stml-bestandstype", "bestand", "type", "wat is een stml-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI HTML-bestand",
  "description":"Meer informatie over STML-bestandsindeling en API's die STML-bestanden kunnen maken en openen.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Wat is een STML-bestand?

Een bestand met de extensie .stml is een webpagina met instructies aan de serverzijde die worden uitgevoerd wanneer een gebruiker de pagina in de webbrowser laadt. STML-pagina's bevatten server-side code die server-side bevat om taken uit te voeren die niet mogelijk zijn met gewone HTML. Hoewel het vergelijkbaar is met [HTML](/nl/web/html/), biedt STML meer kracht door de opdrachten op de server uit te voeren, ook wel Server Side Inclusief (SSI) genoemd. Met de introductie van nieuwe programmeertalen met server-side scripting zoals PHP, wordt het gebruik van STML verminderd, hoewel het nog steeds wordt ondersteund door alle server-side-technologieën. STML-bestanden kunnen in elke teksteditor worden geopend en bewerkt om de opdrachten bij te werken.

## STML-bestandsindeling

STML is gebaseerd op een gewoon ascii-tekstbestandsformaat dat voor mensen leesbaar is. Het volgt echter de syntaxis zoals gedefinieerd en uitgeoefend met behulp van de [SSI-commando's](https://www.w3.org/Jigsaw/Doc/User/SSI.html) die aan de serverzijde worden uitgevoerd. Net als elke andere scripttaal aan de serverzijde, kan STML de opdrachten aan de serverzijde gebruiken om taken uit te voeren zoals paginabezoekersteller, webpaginakalender, records ophalen uit de database en soortgelijke andere.

## STML-voorbeeld

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

