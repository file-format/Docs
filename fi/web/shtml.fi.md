{
  "date": "2021-05-20",
  "keywords": [
"shtml",
"shtml-tiedosto",
"shtml-tiedostomuoto",
"shtml-tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on shtml-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHTML - Palvelinpuoli sisältää HTML-tiedoston",
  "description": "Opi SHTML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SHTML-tiedostoja.",
  "linktitle": "SHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-shtm-fil"
}
},
  "lastmod": "2021-05-20"
}

## Mikä on SHTML-tiedosto?

Tiedosto, jonka pääte on .shtml, on verkkosivu, joka on kirjoitettu kielellä [HTML](/web/html/) ja sisältää palvelinohjeet. Se voi myös sisältää palvelinpuolen osia, jotka ovat samankaltaisia kuin ASP-tiedostot latautumisen nopeuttamiseksi. Palvelinpuolen tiedostot voivat sisältää myös suoritettavaa koodia, joka voi saada palvelimen latautumaan tavallista hitaammin. SHTML-tiedostot ovat samanlaisia kuin HTML, mutta ne mahdollistavat myös yksinkertaisten palvelinkomentojen käytön. Nämä palvelinkomennot suoritetaan yksinkertaisella tietokoneohjelmointikielellä nimeltä Server Side Includes (SSI). SHTML on suurelta osin korvattu muilla palvelinpuolen ohjelmointikielillä, kuten [PHP](/programming/php/) sisältää.

## SHTML-tiedostomuoto

SHTML-tiedostot on kirjoitettu pelkällä tekstillä ja käyttävät [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html), jotka suoritetaan palvelinpuolella. Näitä palvelinpuolen komentoja voidaan käyttää jopa muodostamaan yhteys tietokantaan käyttämällä tietokantaohjaimia ja hakemaan käyttäjien tietoja taulukoista.

## SHTML esimerkki

Palvelinpuolen ohjeita käytetään sovelluksissa, kuten sivujen kävijälaskuri tai web-sivukalenteri. Seuraava esimerkki näyttää käyttäjätietokannan kolmen ensimmäisen rivin neljä ensimmäistä saraketta.

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
## Viitteet

* [Server Side Includes](https://en.wikipedia.org/wiki/Server_Side_Includes)


