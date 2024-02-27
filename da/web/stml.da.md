{
  "date": "2021-05-20",
  "keywords": [
"stml",
"stml fil",
"stml filformat",
"stml filtype",
"fil",
"type",
"hvad er en stml-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "STML - SSI HTML-fil",
  "description": "Lær om STML filformat og API'er, der kan oprette og åbne STML filer.",
  "linktitle": "STML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-stm-dal"
}
},
  "lastmod": "2021-05-20"
}

## Hvad er STML fil?

En fil med filtypenavnet .stml er en webside med instruktioner på serversiden, der udføres, når en bruger indlæser siden i webbrowseren. STML-sider indeholder serversidekode, der indeholder serversideinkludering til at udføre opgaver, som ikke er mulige at opnå med almindelig HTML. Selvom det ligner [HTML](/web/html/), tilbyder STML mere kraft ved at køre kommandoerne på serveren, også kaldet Server Side Includes (SSI). Med introduktionen af nye programmeringssprog med serverside scripting såsom PHP, reduceres brugen af STML, selvom det stadig understøttes af alle serverside teknologier. STML-filer kan åbnes i enhver teksteditor og redigeres til opdatering af kommandoerne.

## STML filformat

STML er baseret på almindeligt ascii-tekstfilformat, der kan læses af mennesker. Det følger dog syntaksen som defineret og udøvet ved hjælp af [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html), der udføres på serversiden. Som ethvert andet scriptsprog på serversiden kan STML bruge kommandoerne på serversiden til at udføre opgaver såsom sidebesøgstæller, websidekalender, hente poster fra database og lignende andre.

## STML eksempel

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


