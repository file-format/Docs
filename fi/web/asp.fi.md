{
  "date": "2019-10-11",
  "keywords": [
"asp",
"asp tiedosto",
"asp tiedostomuoto",
"asp tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on asp-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASP - Active Server Pages -tiedostomuoto",
  "description": "Opi ASP-tiedostosta ja sovellusliittymistä, jotka voivat luoda ja avata niitä.",
  "linktitle": "ASP",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-fip"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on ASP-tiedosto?

ASP on lyhenne sanoista Active Server Pages, joka on kehityskehys web-sivujen luomiseen. Se mahdollistaa tietokonekoodin suorittamisen sisäisellä palvelimella palvelemaan verkkopyyntöjä. Kun verkkoselain luo pyynnön ASP-tiedostoa varten, palvelin lukee tiedoston ja suorittaa sen sisältämän koodin/komentosarjan **[HTML](/web/html/)**-tuloksen luomiseksi, joka palautetaan selaimeen näytettäväksi.

Toisin kuin HTML-sivut, jotka ovat palvelimen palvelemia staattisia sivuja, ASP-tiedostot luovat ajon aikana dynaamista sisältöä, johon saattaa liittyä tietopyyntöjä tietokannasta. ASP-sivuilla käytetään yleensä .asp-laajennusta .html:n sijaan. Koska ASP-tiedoston sisällä oleva koodi/komentosarja suoritetaan palvelinpuolella, pyytävä selain ei näe koodia, jota käytetään tarjotun sivun rakentamiseen. Kaikki nykyaikaiset selaimet pystyvät näyttämään tuloksena luotuja sivuja. ASP:llä rakennettuja sivuja isännöidään Microsoft Internet Information Services (IIS) -palvelimilla.

## ASP-tiedostomuodon lyhyt historia
ASP on käynyt läpi vain muutaman version, kunnes sen korvasi ASP.NET, joka on nykyaikaisempi ja tehokkaampi tapa kehittää ja hallita palvelinsivuja. ASP-tuki sisältyy oletusarvoisesti Internet Information Services (IIS) -palveluiden ohella. ASP julkaistiin kolmessa eri versiossa parannuksilla jokaiseen.

* ASP 1.0 julkaistiin joulukuussa 1996 osana IIS 3.0:aa

* ASP 2.0 julkaistiin syyskuussa 1997 osana IIS 4.0:aa

* ASP 3.0 julkaistiin marraskuussa 2000 osana IIS 5.0:aa


## ASP toiminnalliset objektit

ASP-tiedostot käyttävät palvelinpuolen objekteja käyttäjien pyyntöjen käsittelemiseen ja käyttäjille tarjottavien tulossivujen luomiseen. Jokaisella objektilla on joukko kokoelmia, ominaisuuksia ja menetelmiä pyyntöjen ja vastausten käsittelemiseksi. Näitä kohteita ovat:

### Pyydä objektia

Kun selain pyytää sivua palvelimelta, sitä kutsutaan pyynnöksi. Request-objektia käytetään vierailijan tietojen saamiseen.

### Vastausobjekti

ASP Response -objektia käytetään lähettämään tuloste käyttäjälle palvelimelta.

### Palvelinobjekti

ASP-palvelinobjektia käytetään palvelimen ominaisuuksien ja menetelmien käyttöön. Se mahdollistaa yhteydet tietokantoihin (ADO), tiedostojärjestelmään ja palvelimelle asennettujen komponenttien käytön.

### Istuntoobjekti

Istuntoobjekti on kuin linkki palvelimelta sivua pyytävän käyttäjän selaimen ja itse palvelimen välillä. Tämä saavutetaan ASP:n luomalla evästeellä, joka lähetetään käyttäjän tietokoneelle. Istunto-objekti tallentaa tietoja käyttäjäistunnosta tai muuttaa sen asetuksia. Tiedot tallennetaan istuntoobjektiin jaetaan kaikille sovelluksen sivuille. Yleisiä istuntomuuttujiin tallennettuja tietoja ovat nimi, tunnus ja asetukset. Palvelin luo uuden istuntoobjektin jokaiselle uudelle käyttäjälle ja tuhoaa istuntoobjektin istunnon vanhentuessa.

### Sovellusobjekti

Sovellusobjekti sisältää tietoja, joita monet sovelluksen sivut käyttävät (kuten tietokantayhteystiedot). Tietoihin pääsee miltä tahansa sivulta. Tietoja voidaan myös muuttaa yhdessä paikassa ja muutokset näkyvät automaattisesti kaikilla sivuilla. Sovellusobjektia käytetään muuttujien tallentamiseen ja käyttämiseen miltä tahansa sivulta, aivan kuten Istunto-objektia.

### ASPERror Object

ASPERror-objekti toteutettiin ASP 3.0:ssa, ja se on saatavilla IIS5:ssä ja myöhemmissä versioissa. ASPERror-objektia käytetään näyttämään yksityiskohtaisia tietoja kaikista ASP-sivun komentosarjojen virheistä.

**Huomaa:** ASPERror-objekti luodaan, kun Server.GetLastError kutsutaan, joten virhetietoihin pääsee käsiksi vain käyttämällä Server.GetLastError-menetelmää.

## Viitteet

* [ASP – W3C](https://www.w3schools.com/asp/default.asp)

* [Yksinkertaisten ASP-sivujen luominen](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))


