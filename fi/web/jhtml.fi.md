{
  "date": "2019-10-11",
  "keywords": [
"jhtml",
"jhtml-tiedosto",
"jhtml-tiedostomuoto",
"jhtml-tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on jhtml-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JHTML - Java HTML -tiedosto",
  "description": "Opi JHTML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JHTML-tiedostoja.",
  "linktitle": "JHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-jhtm-fil"
}
},
  "lastmod": "2021-06-09"
}

## Mikä on JHTML-tiedosto?

Tiedosto, jonka pääte on .jhtml, on [HTML](/web/html/)-tiedosto, jossa on [Java](/programming/java/)-koodi ja joka suoritetaan palvelimella, kun asiakas pyytää tätä sivua selaimessa. Palvelin käsittelee pyynnöt, suorittaa funktion sisältämät Java-toiminnot ja palauttaa sivun asiakkaan selaimeen. JHTML-sivuille upotetut Java-objektit toimivat palvelimella käsittelemään tämän tyyppisiä sivuja koskevia pyyntöjä. JHTML-tiedostot voivat myös käyttää tietokannan tietoja JDBC (Java [Database](/database/) Connectivity) -yhteyden avulla. JHTML-tiedostoja voidaan avata millä tahansa tekstieditorilla ja katsella verkkoselaimissa, kuten Google Chrome, Firefox ja Safari.

## JHTML tiedostomuoto

JHTML on ATG:n oma tekniikka, ja se voidaan luoda käyttämällä ATG (Art Technology Group) Dynamo Document Editor -ohjelmaa. JHTML-tiedostot on kirjoitettu vain tekstitiedostomuodossa käyttäen tavallista HTML- ja Java-koodia. Nämä sisältävät tavallisia HTML-tageja Java-objekteihin viittaavien patentoitujen tunnisteiden lisäksi. Kun käyttäjä pyytää tällaista sivua, HTTP-palvelin välittää pyynnön Java-sovelluspalvelimelle. JHTML-sivu muunnetaan ensin .java-tiedostoksi ja käännetään [.class](/programming/class/)-tiedoston luomiseksi, joka suoritetaan servlet-tiedostona. Tämä luo standardi HTTP- ja HTML-tietojen virran, joka palautetaan takaisin pyytävälle selaimelle näytettäväksi käyttäjälle. Tästä on apua tietokantaan liittyvien kyselyjen suorittamisessa palvelimella ja lopullisen kertyneen tuloksen palauttamisessa asiakkaan selaimeen.

## Viitteet

* [HTML-dokumentin yleinen rakenne](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


