{
  "date": "2021-05-20",
  "keywords": [
"stml",
"stml-tiedosto",
"stml-tiedostomuoto",
"stml-tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on stml-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "STML - SSI HTML -tiedosto",
  "description": "Opi STML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata STML-tiedostoja.",
  "linktitle": "STML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-stm-fil"
}
},
  "lastmod": "2021-05-20"
}

## Mikä on STML-tiedosto?

Tiedosto, jonka laajennus on .stml, on verkkosivu, jossa on palvelinpuolen ohjeita, jotka suoritetaan, kun käyttäjä lataa sivun verkkoselaimessa. STML-sivut sisältävät palvelinpuolen koodin, joka sisältää palvelimen puolen sisältämiä tehtävien suorittamiseen, joita ei ole mahdollista saavuttaa tavallisella HTML:llä. Vaikka STML on samankaltainen kuin {{HYPERLINKKI}}, se tarjoaa enemmän tehoa suorittamalla komennot palvelimella, joita kutsutaan myös SSI:ksi (Server Side Includes). Uusien ohjelmointikielten, kuten PHP:n, käyttöönoton myötä STML:n käyttö vähenee, vaikka kaikki palvelinpuolen tekniikat tukevat sitä edelleen. STML-tiedostoja voidaan avata missä tahansa tekstieditorissa ja muokata komentojen päivittämistä varten.

## STML-tiedostomuoto

STML perustuu tavalliseen ascii-tekstitiedostomuotoon, joka on ihmisen luettavissa. Se noudattaa kuitenkin syntaksia sellaisena kuin se on määritetty ja käytetty käyttämällä {{HYPERLINKKI}}, jotka suoritetaan palvelinpuolella. Kuten mikä tahansa muu palvelinpuolen komentosarjakieli, STML voi käyttää palvelinpuolen komentoja suorittaakseen tehtäviä, kuten sivun kävijälaskuria, verkkosivukalenteria, tietueiden hakemista tietokannasta ja vastaavia.

## STML-esimerkki

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


