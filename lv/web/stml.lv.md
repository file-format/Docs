{
  "date": "2021-05-20",
  "keywords": [
"stml",
"stml failu",
"stml faila formātā",
"stml faila tips",
"failu",
"veids",
"kas ir stml fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "STML — SSI HTML fails",
  "description": "Uzziniet par STML faila formātu un API, kas var izveidot un atvērt STML failus.",
  "linktitle": "STML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-stm-lvl"
}
},
  "lastmod": "2021-05-20"
}

## Kas ir STML fails?

Fails ar paplašinājumu .stml ir tīmekļa lapa ar servera puses instrukcijām, kas tiek izpildītas, kad lietotājs ielādē lapu tīmekļa pārlūkprogrammā. STML lapās ir servera puses kods, kurā ir ietverti servera puses elementi, lai veiktu uzdevumus, kurus nav iespējams sasniegt ar vienkāršu HTML. Lai gan STML ir līdzīgs [HTML](/web/html/), tas piedāvā lielāku jaudu, palaižot komandas serverī, ko sauc arī par servera puses iekļaušanu (SSI). Ieviešot jaunas programmēšanas valodas ar servera puses skriptiem, piemēram, PHP, STML izmantošana ir samazināta, lai gan to joprojām atbalsta visas servera puses tehnoloģijas. STML failus var atvērt jebkurā teksta redaktorā un rediģēt, lai atjauninātu komandas.

## STML faila formāts

STML pamatā ir vienkāršs ASCII teksta faila formāts, kas ir lasāms cilvēkiem. Tomēr tas atbilst sintaksei, kas noteikta un izmantota, izmantojot [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html), kas tiek izpildīta servera pusē. Tāpat kā jebkura cita servera puses skriptu valoda, STML var izmantot servera puses komandas, lai veiktu tādus uzdevumus kā lapas apmeklētāju skaitītājs, tīmekļa lapu kalendārs, izgūtu ierakstus no datu bāzes un līdzīgus citus uzdevumus.

## STML piemērs

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


