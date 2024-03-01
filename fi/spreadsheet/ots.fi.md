{
  "date": "2019-12-16",
  "keywords": [
"OTS",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Excel",
"Laskentataulukko"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi OTS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OTS-tiedostoja.",
  "title": "OTS - OpenDocument Spreadsheet Template -tiedostomuoto",
  "linktitle": "OTS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-ot-fis"
}
},
  "lastmod": "2021-01-19"
}

## Mikä on OTS-tiedosto?

Tiedosto, jonka laajennus on .ots, on OpenDocument Spreadsheet Template -tiedosto, joka luodaan Apache OpenOfficeen sisältyvällä Calc-sovellusohjelmistolla. Calc-sovellusohjelmisto on samanlainen kuin Microsoft Officessa saatavilla oleva Excel. OTS-tiedostomuotoa käytetään luomaan malleja, jotka sisältävät ennalta määritettyjä tyyleihin, kirjasimiin, tietoihin, laskentataulukon asetteluun ja muotoiluun liittyviä asetuksia. OTF-tiedostoissa on mime-type application/vnd.oasis.opendocument.spreadsheet-template. Näitä mallitiedostoja voidaan käyttää lähtökohtana luoda ja tallentaa todellisia datatiedostoja, jotka on tallennettu {{HYPERLINKKI}}. OTS-tiedostoja voidaan käyttää sovellusten, kuten OpenOffice ja LibreOffice, kanssa.

## OTS-tiedostomuoto

OTS-tiedostot tallennetaan OASIS:n OpenDocument XML-pohjaiseen tiedostomuotoon, joka koostuu useiden aliasiakirjojen kokoelmasta ja paketista [ZIP](/compression/zip/)-arkistona. Jokainen zip-arkisto tallentaa osan täydellisestä asiakirjasta ja jokainen aliasiakirja tallentaa asiakirjan tietyn osan. Esimerkiksi yksi aliasiakirja sisältää tyylitiedot ja toinen aliasiakirja dokumentin sisällön. Tyypillisessä ODF-asiakirjassa on seuraavat osat:

### OTS Content.xml

Content.xml-tiedosto sisältää asiakirjan todellisen sisällön. Tämä ei kuitenkaan sisällä binääritietoja, kuten kuvia.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml OTS-tiedostomuodosta

Styles.xml-tiedosto sisältää tyylitietoja, ja sitä käytetään paljon muotoiluun ja asetteluun. Tyylityyppejä ovat:

 * Kappaletyylit
 * Sivutyylit
 * Hahmotyylit
 * Kehystyylejä
 * Listaa tyylejä

### Meta.xml

Meta.xml-tiedosto sisältää tietoja tiedoston metatiedoista, kuten tekijä, viimeinen muokkauspäivä jne.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

settings.xml-tiedosto sisältää asiakirjatason asetukset, kuten zoomauskertoimen ja kohdistimen sijainnin.

## Viitteet ##

* [OpenDocument 1.2 -spesifikaatio](https://www.oasis-open.org/standards#opendocumentv1.2)

* [OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


