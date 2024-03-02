{
  "date": "2021-01-20",
  "keywords": [
"xslt",
"Comhad",
"Síneadh",
"Formáid Chomhaid",
"Síneadh Comhad",
"Teanga Stílbhileog Leathnaithe"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid XSLT",
  "description": "Foghlaim faoi fhormáid comhaid XSLT agus APIs ar féidir leo comhaid XSLT a chruthú agus a oscailt.",
  "linktitle": "XSLT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xsl-gat"
}
},
  "lastmod": "2021-01-20"
}

## Cad is comhad XSLT ann?

Is comhad a bhfuil iarmhír .xslt air ná comhad Trasfhoirmithe Teanga Stílbhileog In-Imlíne a úsáidtear chun comhad XML a athrú agus a stíl ag baint úsáide as treoracha XSL. Úsáidtear an fhormáid chun doiciméid XML a athrú go formáidí caighdeánacha aschuir ar nós doiciméad téacs nó leathanach gréasáin .html. Cruthaíonn an claochlú seo doiciméad nua bunaithe ar ábhar an doiciméid XML atá ann cheana féin. Tá XSLT ag déanamh go teoiriciúil go bhfuil sé in ann ríomhanna treallach a dhéanamh.

## Formáid Chomhaid XSLT

Tá treoracha claochlaithe i bhformáid gnáth-théacs i bhformáid comhaid XLST ar féidir a fheiceáil in aon eagarthóir téacs. Tá trí athbhreithniú déanta ar an teanga.

* Foilsíodh `XSLT 1.0` - XSLT 1.0 mar mholadh W3C i mí na Samhna 1999.

* `XSLT 2.0` - Cuimsíonn sé modhnuithe cosúil le ionramháil teaghrán ag baint úsáide as nathanna rialta, feidhmeanna agus oibreoirí chun dátaí, amanna agus tréimhsí a ionramháil, doiciméid aschuir iolracha, grúpáil, agus córas cineál níos saibhre agus seiceáil cineál láidir.

* `XSLT 3.0` - Tháinig sé mar chuid de Mholadh W3C an 8 Meitheamh 2017 agus áirítear ar na príomhghnéithe nua claochlú sruthú, Pacáistí chun modúlacht na stílbhileoga móra a fheabhsú, láimhseáil feabhsaithe ar earráidí dinimiciúla le, mar shampla, treoir xsl:triail, agus tacaíocht do léarscáileanna agus eagair, ag cur ar chumas XSLT JSON chomh maith le XML a láimhseáil.


### Sampla XSLT

Tógtar an sampla seo a leanas ó [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Tagairtí ##

* [XSLT - Le Vicipéid](https://ga.wikipedia.org/wiki/XSLT)

* [Eilimintí XSLT](https://en.wikipedia.org/wiki/XSLT_elements)


