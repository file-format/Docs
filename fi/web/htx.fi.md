{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTX-tiedosto - HTML-laajennustiedostomuoto",
  "description": "Tiedostomuoto-oppaasi oppiaksesi, mikä on HTX-tiedosto ja API:t, jotka voivat luoda ja avata HTX-tiedoston.",
  "linktitle": "HTX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-fix"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on HTX-tiedosto?

HTX-tiedosto on itse asiassa HTML-tiedosto, joka sisältää datamuuttujia tietokantakyselyn tulosten näyttämiseksi verkkosivuna. Useimmiten Microsoft FrontPage Web -kehitysohjelmistolla luodut HTX-tiedostot tallennetaan samaan kansioon kuin vastaava Internet Database Connector (.IDC) -tiedosto.

HTX-tiedostoja voidaan avata sovelluksilla, kuten Microsoft FrontPage, ja millä tahansa tekstieditorilla, kuten Notepad, TextEdit tai Atom.

## HTX tiedostomuoto

HTX-tiedostot tallennetaan pelkkänä tekstitiedostona koodilla tietojen hakemista tietokannasta ja muuttujien tallentamista näyttöä varten.


### HTX-tiedostoesimerkki

Esimerkki HTX-tiedostosta on seuraava, joka määrittää sivun otsikon kyselyrajoituksen näyttämiseksi ja sivulla näytettävät asiakirjat käyttäjälle näytettäväksi.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

Tämän mallikoodin tulos on seuraava.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Kuten voidaan nähdä, HTX-tiedosto on malli, joka muotoilee kuinka tulokset palautetaan ja näytetään loppukäyttäjille. Se on kirjoitettu HTML-muodossa joidenkin IIS-laajennusten ja indeksointipalvelun kanssa. Nämä laajennukset sisältävät muuttujien nimiä ja muita koodeja tulosten käsittelyä varten.

## Viitteet

* [Tulokset muotoilemalla .Htx-tiedostoa](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)


