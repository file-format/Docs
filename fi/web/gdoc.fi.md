{
  "date": "2022-01-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDOC-tiedosto – Google-dokumenttien pikakuvake",
  "description": "Tutustu GDOC-tiedostoon ja sovellusliittymiin, jotka voivat luoda ja avata GDOC-tiedostoja.",
  "linktitle": "GDOC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-gdo-fic"
}
},
  "lastmod": "2022-01-23"
}

## Mikä on GDOC-tiedosto?

GDOC-tiedosto on pikakuvaketiedosto, joka osoittaa tiedostoon, joka sijaitsee Google Drivessa, pilvipohjaisessa asiakirjojen tallennuspalvelussa. Kun Google Drive -asiakasohjelma on asennettu tietokoneeseen ja sen sisällä luodaan dokumentti, asema luo dokumentin online-pilvitallennustilaan ja kirjoittaa tämän asiakirjan [URL](/web/url/) GDOC-tiedostoon paikallisessa Google Drive -kansiossa. Kun tätä pikakuvaketiedostoa kaksoisnapsautetaan, oletusselain avaa asiakirjan sijainnista [URL](/web/url/). Jos tämä pikakuvaketiedosto siirretään pois tästä kansiosta, linkki online-asiakirjaan on rikki.

## GDOC-tiedostomuoto - lisätietoja

GDOC-tiedosto sisältää pikakuvakkeen online-asiakirjaan, joka on kirjoitettu [JSON](/web/json/)-tiedostomuodossa. GDOC-tiedostoja avaava selain lukee URL-tiedot ja avaa linkitetyn asiakirjan näytettäväksi, jos käyttäjä on kirjautunut tälle Google-tilille, johon asiakirja on tallennettu. GDOC-tiedostot eivät sisällä asiakirjan sisältöä.

### GDOC-tiedostoesimerkki

GDOC-tiedosto voidaan avata tekstieditorilla ja sen sisältö näyttää seuraavalta.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Kuten voidaan nähdä, sisältö on muotoiltu JSON-muodossa, jolla on asiakirjan URL-osoite ja siihen liittyvä asiakirjatunnus.

## Viitteet

* [Google Docs not opening either gdoc or docx files](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en)

