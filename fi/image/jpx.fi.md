{
  "date": "2021-02-10",
  "keywords": [
"jpx tiedosto",
"jpx tiedostomuoto",
"mikä on jpx-tiedosto",
"tiedosto",
"jpx esimerkki",
"jpx tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPX - Kuvatiedostomuoto",
  "description": "Opi JPX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JPX-tiedostoja.",
  "linktitle": "JPX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-fix"
}
},
  "lastmod": "2021-02-10"
}

## Mikä on JPX-tiedosto? ##

Tiedosto, jonka tunniste on .jpx, on JPEG 2000 -tiedostomuodon laajennus. Se käyttää ensisijaisesti JPEG 2000 -pakkausta ja tarjoaa myös edistyneitä ominaisuuksia, kuten useita kerroksia kuvalle, erilaisia väriavaruuksia, peittävyyttä ja pirstoutuneita koodivirtoja. JPX sallii myös muut pakkaukset, kuten JBIG, CCITT Group3, CCITT Group4 jne. JPEG 2000 -pakkauksen lisäksi. JPX-tiedostomuoto hyväksyttiin [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html)-standardiksi, mutta se ei saanut lämmintä vastaanottoa [JPEG](/image/jpeg/)-tiedostomuodon laajan käytön vuoksi. Sovelluksia, jotka voivat avata JPX-tiedostoja, ovat Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 ja CorelDraw Graphics Suite 2020.

## Lyhyt historia

In 2000, the Joint Photographic Experts Group committee designed JP2 with the objective to improve their own discrete cosine transform-based JPEG standard with this new wavelet-based method. The JPEG committee aimed to provide their baseline methods free of license fees.in the JP2 license gaining competition among 20 companies, they won by a whisker. JPEG 2000 has been declared as an ISO standard, though most web browser are not ready to give a hand to JPEG 2000 since 2017. Vuonna 2004 ISO/IEC 15444-2 -muoto hyväksyttiin julkisesti JP2-tiedostomuodon laajennukseksi.

## JPX tiedostomuoto

JPX-tiedostomuoto muotoiltiin vastaamaan sovellusten vaatimuksia, jotka tarvitsivat tietorakenteita, jotka ylittävät [JP2](/image/jp2/)-tiedostomuodon määrittämät toiminnot. JP2-tiedosto, jonka laajennukset eivät ole yhteensopivia, voi aiheuttaa hämmennystä markkinoilla, koska jotkut lukijat voivat tulkita joitain JP2-tiedostoja, mutta eivät toisia. JPX on vastaus tällaisten ongelmien välttämiseen sovelluksissa.

### Tiedoston tunnistus

JPX-tiedostot tallennetaan nimellä [JPF](/image/jpf/), kun ne tallennetaan perinteiseen tietokonetiedostojärjestelmään. Tästä syystä JPX-termiä käytetään vähiten JPF:ään verrattuna. JPX-tiedosto alkaa seuraavilla tavuilla:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Tiedoston organisaatio

Kuten JP2, JPX-tiedosto on kokoelma laatikoita, joilla on binäärirakenne ja laatikot on järjestetty vierekkäiseen järjestykseen. Ensimmäinen laatikko antaa tiedoston alun ensimmäisellä tavulla ja viimeisen laatikon viimeinen tavu edustaa tiedoston viimeistä tavua.
JPX-tiedoston laatikon binäärirakenne on identtinen tiedostomuodossa [JP2](/image/jp2/) määritetyn kanssa.

### CodeStreamin tallennus JPX-muodossa

JPX-tiedostomuoto mahdollistaa kuvan koodivirran jakamisen osiin. Tämä mahdollistaa kuvan yksittäisen ruudun muokkaamisen ja muokatun ruudun kirjoittamisen tiedoston loppuun kirjoittamatta koko tiedostoa uudelleen. Alkuperäinen [JP2](/image/jp2/)-tiedostomuoto rajoittaa koko koodivirran tallentamisen tiedoston viereiseen osaan, mikä voi olla ongelmallista kuvankäsittelysovelluksissa, jotka saattavat haluta muokata yhtä kuvan ruutua ja saavuttaa yllä olevan JPX-tuen. tiedosto muoto. Kuvan koodivirran pirstoutuminen tekee JPX-tiedostomuodosta paremman kuin JP2-tiedostomuoto. Lisäksi JPX-tiedostomuoto mahdollistaa useiden koodivirran yhdistämisen ja tuottaa renderöidyn tuloksen. Koodivirrat voidaan yhdistää kompositioiksi ja animaatioiksi.

## Viitteet ##

* [JPEG 2000:n yleiskatsaus](https://jpeg.org/jpeg2000/)


