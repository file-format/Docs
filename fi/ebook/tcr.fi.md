{
  "date": "2021-03-09",
  "keywords": [
"TCR",
"Psion",
"laajennus",
"muoto",
"e-kirja"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi TCR-tiedostomuodosta Psion 3 -sarjalle ja API-liittymille, jotka voivat luoda ja avata tcr-tiedostoja.",
  "title": "TCR - Psion Series 3 eBook File",
  "linktitle": "TCR",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-tc-fir"
}
},
  "lastmod": "2021-03-09"
}

## Mikä on TCR-tiedosto?

90-luvun alussa otettiin käyttöön TCR-tiedostomuoto muinaisille **Psion Series 3** -kämmentietokoneille. Yritys käytti alustakohtaista pakkaustaan ja tällä muodolla on hyvin rajallinen tuki tekstin muotoilulle. Se on ZVR-pohjainen tiedostomuoto ja tarjoaa suhteellisen paremman pakkaussuhteen kuin PalmDOC. Se toimii myös erittäin hyvin FontMachinen kanssa. Vaikka TCR-tiedostomuoto kuuluu lopetetulle laitteelle, tämä tiedostomuoto voidaan silti lukea joillakin eReaders-lukulaitteilla. Tätä tiedostomuotoa voi tarkastella myös työpöydällä Sumatra PDF:llä ja Caliber-sovelluksella Windowsissa ja Linuxissa.

## Tekniset yksityiskohdat

Koska TCR-tiedostomuoto perustuu ZVR-kompressoriin, joka pystyy pienentämään monia tiedostoja noin 50 % niiden alkuperäisestä koosta. Ylin käyttämä pakkausmalli on hieman vanha. Pakattu tiedosto alkaa sanakirjalla, joka sisältää 256 mahdollista symbolia, jotka saattavat näkyä pakatussa tiedostossa. Sanakirja sisältää kiinteän vaihtoehtoisen merkkijonon jokaiselle näistä symboleista. Pakkauksen purkamisesta on tullut erittäin nopeaa jopa OPL:ssä, ja se voi alkaa missä tahansa pakatun tiedoston kohdassa.

## Ongelmia avattaessa TCR-tiedostoa ##

Jos et pysty avaamaan ja suorittamaan TCR-tiedostoa; se ei tarkoita, etteikö laitteellesi olisi asennettu sopivaa ohjelmistoa. Jotkin muut ongelmat voivat estää tiedostoa toimimasta oikein. Mahdolliset ongelmat voivat olla jokin seuraavista:

- TCR-tiedoston korruptio.
- Väärät linkit TCR-tiedostoon rekisterimerkinnöissä.
- Deleted description of the TCR from the Windows registry
- Vioittunut TCR-muotoa tukevan sovelluksen asennus
- Tartunnan saanut TCR-tiedosto, joka sisältää ei-toivottuja haittaohjelmia.
- Tietokoneella ei ole riittävästi laitteistoresursseja TCR-tiedoston käyttämiseen.
- Ajurit, joita tietokone käyttää TCR-tiedoston avaamiseen, ovat vanhentuneita.




## Viitteet

* [TCR - MobileRead](https://wiki.mobileread.com/wiki/TCR)

* [ZVR Compressed Text File Reader](https://iay.org.uk/zvr/)


