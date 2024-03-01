{
  "date": "2021-07-29",
  "keywords": [
"pes-tiedosto",
"pes-tiedostomuoto",
"mikä on pes-tiedosto",
"tiedosto",
"pes esimerkki",
"pes tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PES-tiedostomuoto - Brother PE -kirjontamuoto",
  "description": "Opi PES-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PES-tiedostoja.",
  "linktitle": "PES",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-pe-fis"
}
},
  "lastmod": "2021-07-29"
}

## Mikä on PES-kirjontatiedosto?

PES-kirjontatiedosto on suunnittelutiedosto, joka sisältää ohjeet kirjonta-/ompelukoneille. Brother Industries kehitti sen kirjontakoneilleen, mutta se muotoiltiin myöhemmin yleiseksi tiedostomuodoksi. Ompelukoneet käyttävät PES-tiedostoja lukemaan ohjeita kuvioiden ompelemiseen kankaaseen. Nämä tiedostot palvelevat kahta tarkoitusta; Ensinnäkin Brother Industriesin kehittämän PE-Design-sovelluksen suunnittelutiedot ja toiseksi suunnittelun nimen, värit ja kirjontakonekoodit, kuten stop, jump ja trim.

## PES-tiedostomuoto - lisätietoja

PES-tiedosto tallennetaan levylle binääritiedostomuodossa. Se sisältää useita osia, joihin on tallennettu ompelutiedot ennalta määritetyllä menetelmällä. PES-tiedostomuoto on seuraava.

 * Versiotiedot – Antaa versiotiedot ja voi olla mikä tahansa arvo #PES0001, #PES0020, #PES0030, #PES0040, #PES0050, #PES0055, #PES0060
 * PEC-hakuarvo - 4-tavuinen pienipäällinen kokonaisluku, joka seuraa välittömästi versiotietoja ja edustaa hakuarvoa PEC-osalle, joka sisältää suunnittelutiedot.
 * PSE-osio – Sisältää Brother PE-Designin kannalta olennaisia suunnittelutietoja ja voi olla muita ompelusovelluksia
 * PCE-osio - Voi olla missä tahansa PSE-tiedostossa, mutta siihen viitataan PEC-hakuarvolla.

## PES-tiedostoa käyttävien ompelukoneiden tyyppi

PES-tiedostot luodaan ensisijaisesti PE-Design-ohjelmistolla, jota käytetään Brother-ompelukoneiden kanssa. Jotkut muut koneet, jotka voivat tukea PES-tiedostoja, sisältävät Babylock- ja Bernina-kotikirjontakoneet.

## Kuinka muuntaa PSE-tiedostoja?

PE-Design-ohjelmistosovellus voi {{HYPERLINKKI1}} käyttää muita muotoja, kuten .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd tai .xxx. . Se voidaan tehdä PE-Design-sovelluksella avaamalla tiedosto ja valitsemalla Conversion-muoto.

## Viitteet

* [PE-suunnittelu – Käyttöopas](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_FI/index.html#!/)


