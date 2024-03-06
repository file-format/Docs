{
  "date": "2021-01-20",
  "keywords": [
"xslt",
"Fails",
"Pagarinājums",
"Faila formāts",
"Faila paplašinājums",
"Paplašināma stila lapu valoda"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLT faila formāts",
  "description": "Uzziniet par XSLT faila formātu un API, kas var izveidot un atvērt XSLT failus.",
  "linktitle": "XSLT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xsl-lvt"
}
},
  "lastmod": "2021-01-20"
}

## Kas ir XSLT fails?

Fails ar paplašinājumu .xslt ir paplašināmās stila lapas valodas transformācijas fails, ko izmanto, lai pārveidotu un veidotu XML failu, izmantojot XSL instrukcijas. Formāts tiek izmantots, lai pārveidotu XML dokumentus standarta izvades formātos, piemēram, teksta dokumentā vai .html tīmekļa lapā. Šī transformācija izveido jaunu dokumentu, pamatojoties uz esošā XML dokumenta saturu. XSLT padara to teorētiski spējīgu veikt patvaļīgus aprēķinus.

## XSLT faila formāts

XLST faila formātā ir pārveidošanas instrukcijas vienkārša teksta formātā, ko var skatīt jebkurā teksta redaktorā. Ir bijuši trīs valodas labojumi.

* "XSLT 1.0" — XSLT 1.0 tika publicēts kā W3C ieteikums 1999. gada novembrī.

* `XSLT 2.0` — tajā ir iekļautas tādas modifikācijas kā virkņu manipulācijas, izmantojot regulāras izteiksmes, funkcijas un operatorus, lai manipulētu ar datumiem, laikiem un ilgumiem, vairāki izvaddokumenti, grupēšana un bagātāka tipa sistēma un spēcīga tipa pārbaude.

* `XSLT 3.0` — tas kļuva par daļu no W3C ieteikuma 2017. gada 8. jūnijā, un galvenās jaunās funkcijas ietver straumēšanas pārveidošanu, pakotnes, lai uzlabotu lielu stilu lapu modularitāti, uzlabota dinamisko kļūdu apstrāde ar, piemēram, xsl:try instrukciju, un karšu un masīvu atbalsts, kas ļauj XSLT apstrādāt gan JSON, gan XML.


### XSLT piemērs

Šis piemērs ir ņemts no [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## Atsauces Nr.

* [XSLT — Wikipedia](https://en.wikipedia.org/wiki/XSLT)

* [XSLT Elements](https://en.wikipedia.org/wiki/XSLT_elements)


