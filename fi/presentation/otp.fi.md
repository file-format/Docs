{
  "date": "2021-01-21",
  "keywords": [
"otp tiedosto",
"otp tiedostomuoto",
"mikä on otp-tiedosto",
"tiedosto",
"otp esimerkki",
"otp tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTP - OpenDocument-esitysmalli",
  "description": "Lisätietoja OTP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OTP-tiedostoja.",
  "linktitle": "OTP",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-ot-fip"
}
},
  "lastmod": "2021-01-21"
}

## Mikä on OTP-tiedosto?

Tiedostot, joiden laajennus on .otp, edustavat OASIS OpenDocument -standardimuodossa olevien sovellusten luomia esitysmallitiedostoja. Tällaisen tiedoston sisältö sisältää esitystietoja diojen muodossa, joissa on tekstiä, kuvia, muotoja, multimediasisältöä, siirtymätehosteita ja muita diaelementtejä. Näitä mallitiedostoja käytetään uusien esitysten nopeaan luomiseen itse malliin tallennettujen tyylitietojen perusteella. OTP-tiedostoja voidaan luoda ja tallentaa useilla eri sovelluksilla, kuten OpenOffice-paketin mukana tulevalla Impressillä ja Microsoft PowerPointilla. OTP-tiedostomuoto on samanlainen kuin Microsoft PowerPoint -mallitiedostot [.pot](/presentation/pot/) ja [.potx](/presentation/potx/).

## OTP-tiedostomuoto

OTP-tiedostomuoto perustuu OpenDocument-standardiin, joka tukee asiakirjan esittämistä yhtenä XML-asiakirjana sekä useiden aliasiakirjojen kokoelmaa yhteen pakattuun pakettiin [ZIP](/compression/zip/)-muodossa. Tiedoston sisältö jaetaan useisiin xml-tiedostoihin, jotka on pakattu yhteen. Nämä useat [XML](/web/xml/)-tiedostot sisältävät tietoja asiakirjan tyylistä, sisällöstä, metatiedoista ja asetuksista, kuten alla on mainittu.

* `content.xml` – Asiakirjan sisältö ja sisällössä käytetyt automaattiset tyylit.

* `styles.xml` – Asiakirjan sisällössä käytetyt tyylit ja itse tyyleissä käytetyt automaattiset tyylit.

* `meta.xml` – Asiakirjan metatiedot, kuten tekijä tai viimeisimmän tallennustoiminnon aika.

* `settings.xml` – Sovelluskohtaiset asetukset, kuten ikkunan koko tai tulostintiedot.


## Viitteet

* [OpenDocument – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


