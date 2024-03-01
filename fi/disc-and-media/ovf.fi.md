{
  "date": "2021-08-10",
  "keywords": [
".ovf-tiedosto",
"tiedosto muoto",
"mikä on .ovf-tiedosto",
"tiedosto",
"tiedostopääte"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi .ovf-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OVF-tiedostoja.",
  "title": "OVF-tiedostomuoto - Avaa virtualisointitiedosto",
  "linktitle": "OVF",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ov-fif"
}
},
  "lastmod": "2022-01-03"
}

## Mikä on OVF-tiedosto?

OVF-tiedosto on tekstitiedosto, joka sisältää tietoja virtuaalikoneessa toimivan ohjelmiston pakkauksesta ja jakelusta. Se on muotoiltu {{HYPERLINKKI}}:n mukaisesti, joka kuvaa kaikki vaatimukset (kuten turvallisuus, siirrettävyys, tehokkuus ja laajennettavuus) sovellusten suorittamiselle virtuaalikoneen. Kansainvälinen standardointijärjestö (ISO) on hyväksynyt OVF:n ISO 17203 -standardiksi.

## OVF-tiedostomuodon lyhyt historia

OVF-tiedostomuodon esitteli DMTF (Distributed Management Task Force), joka luo avoimet hallittavuusstandardit. Se on riippumaton tietystä hypervisorista tai käskysarjaarkkitehtuurista. OVF-paketti sisältää yhden tai useamman virtuaalijärjestelmän, joista jokainen voidaan ottaa käyttöön virtuaalikoneessa.

## OVF-tiedostomuoto - lisätietoja

OVF-paketti koostuu useista tiedostoista, jotka on sijoitettu yhteen hakemistoon. Näistä se sisältää täsmälleen yhden OVF-kuvaustiedoston (tunnisteella .ovf), joka on tallennettu [XML](/web/xml/)-tiedostomuotoon. Se kuvaa pakatut virtuaalikoneen tiedot ja OVF-paketin metatiedot, kuten:

 * nimi
 * laitteistovaatimukset
 * viittaukset muihin OVF-paketin tiedostoihin ja
 * human-readable descriptions

Muita OVF-paketissa olevia tiedostoja ovat yksi tai useampi levykuva ja valinnaisesti varmennetiedostot ja muut aputiedostot.

## Viitteet

* [Avoin virtualisointimuoto - DMTF](https://www.dmtf.org/standards/ovf)

* [OVF-tiedostomuodon tekniset tiedot](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)


