{
  "date": "2021-05-20",
  "keywords": [
"shtml",
"shtml fil",
"shtml filformat",
"shtml filtype",
"fil",
"type",
"hvad er en shtml-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHTML - Server Side Inkluder HTML-fil",
  "description": "Lær om SHTML-filformat og API'er, der kan oprette og åbne SHTML-filer.",
  "linktitle": "SHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-shtm-dal"
}
},
  "lastmod": "2021-05-20"
}

## Hvad er en SHTML fil?

En fil med filtypen .shtml er en webside, der er skrevet i [HTML](/web/html/) og inkluderer serverinstruktioner. Det kan også indeholde server-side-inkluderer svarende til ASP-filer for hurtigere indlæsning. Serversidefilerne kan også indeholde eksekverbar kode, der kan få serveren til at indlæse langsommere end normalt. SHTML-filer ligner HTML, men de tillader også brugen af simple serverkommandoer. Disse serverkommandoer udføres i et simpelt computerprogrammeringssprog kaldet Server Side Includes (SSI). SHTML er stort set blevet afløst af andre programmeringssprog på serversiden, såsom [PHP](/programming/php/) inkluderer.

## SHTML filformat

SHTML-filer er skrevet i almindelig tekst og bruger [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html), der udføres på serversiden. Disse kommandoer på serversiden kan bruges til endda at oprette forbindelse til databasen ved hjælp af databasedriverne og hente brugerdata fra tabeller.

## SHTML eksempel

Instruktioner på serversiden bruges i applikationer såsom til sidebesøgstæller eller websidekalender. Følgende eksempel viser de første fire kolonner i de første tre linjer i brugerdatabasen.

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
## Referencer

* [Server Side Includes](https://en.wikipedia.org/wiki/Server_Side_Includes)


