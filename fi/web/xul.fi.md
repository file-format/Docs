{
  "date": "2021-05-24",
  "keywords": [
"xul",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"XML-käyttöliittymän kieli"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XUL - XML-käyttöliittymän kielitiedosto",
  "description": "Opi XUL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XUL-tiedostoja.",
  "linktitle": "XUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xu-fil"
}
},
  "lastmod": "2021-05-24"
}

## Mikä on XUL-tiedosto?

Tiedosto, jonka laajennus on .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) tarkoittaa XML-käyttöliittymän kieltä) on [XML](/web/xml/)-pohjainen merkintäkielitiedosto käyttöliittymien luomiseen. Mozilla on kehittänyt sen kehittäjille luodakseen graafisia käyttöliittymäelementtejä, jotka ovat samanlaisia kuin muut verkkosivujen luomiseen käytetyt merkintäkielet. Mozilla on käyttänyt XUL:a laajasti Firefox-selaimessaan, jossa se käytti Mozilla-koodikantaa. XUL-renderöinti suoritetaan käyttämällä
{{HYPERLINKKI}}). Firefox-haarukat, kuten Pale Moon, Basilisk ja Waterfox, säilyttävät tuen XUL-lisäosille. XUL-tiedostot tunnistetaan MIME-tyypillä: application/vnd.mozilla.xul+xml.

## XUL tiedostomuoto

XUL-tiedostot on kirjoitettu pelkällä tekstillä XML-tiedostomuotoon perustuen ja renderöidään Gecko-moottorilla. XUL-rakenteen kolme pääosaa ovat:

 * Sisältö - Tämä sisältää ikkunan määritykset ja niiden sisältämät käyttöliittymäelementit.
 * Skin - Se sisältää kaikki tyylisivut, kuvat ja muut teemaan liittyvät tiedostot. Ikkunan ulkonäkö kuvataan tyylisivuilla.
 * Locale - Ikkunassa näkyvä teksti tallennetaan erikseen, ja käyttäjät voivat käyttää useita kielitiedostoja.

### XUL-esimerkki

Seuraava esimerkki luo kolme painiketta, jotka on pinottu päällekkäin pystysuunnassa.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Viitteet

* [XUL - Wikipedia](https://en.wikipedia.org/wiki/XUL)

* [XUL-arkistoitu dokumentaatio - Mozilla](https://wiki.mozilla.org/XUL:Home_Page)


