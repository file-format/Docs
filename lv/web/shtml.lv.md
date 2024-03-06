{
  "date": "2021-05-20",
  "keywords": [
"shtml",
"shtml failu",
"shtml faila formātā",
"shtml faila tips",
"failu",
"veids",
"kas ir shtml fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHTML — servera pusē iekļaujiet HTML failu",
  "description": "Uzziniet par SHTML faila formātu un API, kas var izveidot un atvērt SHTML failus.",
  "linktitle": "SHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-shtm-lvl"
}
},
  "lastmod": "2021-05-20"
}

## Kas ir SHTML fails?

Fails ar paplašinājumu .shtml ir tīmekļa lapa, kas ir rakstīta [HTML](/web/html/) un ietver servera norādījumus. Tas var saturēt arī servera puses elementus, kas ir līdzīgi ASP failiem ātrākai ielādei. Servera puses failos var būt arī izpildāms kods, kas var izraisīt servera ielādi lēnāk nekā parasti. SHTML faili ir līdzīgi HTML, taču tie ļauj izmantot arī vienkāršas servera komandas. Šīs servera komandas tiek izpildītas vienkāršā datorprogrammēšanas valodā ar nosaukumu Server Side Includes (SSI). SHTML lielākoties ir aizstājušas citas servera puses programmēšanas valodas, piemēram, [PHP](/programming/php/) ietver.

## SHTML faila formāts

SHTML faili ir rakstīti vienkāršā tekstā un izmanto [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html), kas tiek izpildīti servera pusē. Šīs servera puses komandas var izmantot, lai pat izveidotu savienojumu ar datu bāzi, izmantojot datu bāzes draiverus, un izgūtu lietotāju datus no tabulām.

## SHTML piemērs

Servera puses norādījumi tiek izmantoti tādās lietojumprogrammās kā lapas apmeklētāju skaitītājs vai tīmekļa lapu kalendārs. Nākamajā piemērā ir parādītas lietotāju datu bāzes pirmo trīs rindu pirmās četras kolonnas.

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
## Atsauces

* [Ietver servera pusi](https://en.wikipedia.org/wiki/Server_Side_Includes)


