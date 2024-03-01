{
  "date": "2019-10-11",
  "keywords": [
"u3d tiedosto",
"u3d tiedostomuoto",
"mikä on u3d-tiedosto",
"tiedosto",
"u3d esimerkki",
"u3d tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "U3D - yleinen 3D-tiedostomuoto",
  "description": "Opi U3D-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda U3D-tiedostoja.",
  "linktitle": "U3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-u3-fid"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on U3D-tiedosto?

**U3D** (Universal 3D) is a compressed file format and data structure for 3D computer graphics. It contains 3D model information such as triangle meshes, lighting, shading, motion data, lines and points with color and structure. The format was accepted as[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard in August 2005. 3D-dokumentit [PDF](/pdf/) tukevat U3D-objektien upottamista, ja niitä voi tarkastella Adobe Readerissa (versio 7 ja uudemmat).

U3D-muoto kehitettiin pitäen mielessä tavoitteena luoda universaali standardi kolmiulotteiseen tiedon tallentamiseen ja vaihtoon. Muotoa kuitenkin käytetään pääasiassa 3D-pdf-koodauksessa sen sijaan, että sitä käytettäisiin vaihtomuotona. Acrobat 3D muuntaa tuetun 3D-tiedostotyypin joko U3D:ksi tai PRC:ksi PDF-tiedostoksi muunnettaessa.

## U3D-tiedostomuoto

U3D files are in binary file format that underwent four editions as described by the [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) reference document, resulting in specifications update with each edition. The PDF file standard ISO-32000 accepts U3D as allowed annotation and multimedia type.

U3D:n ensimmäinen painos keskittyi 3D-grafiikkaominaisuuksien, kuten geometrian, värien, tekstuurien, valaistuksen, luuston ja muunnospohjaisen animaation, tärkeimpiin esityksiin. Toisessa ja kolmannessa painoksessa korjattiin joitakin virheitä ensimmäisessä painoksessa, ja kolmas versio oli yleisimmin käytetty tyyppi alan ohjelmistoissa. Neljäs painos sisältää määritelmät korkeamman asteen primitiivisille (kaareville pinnoille). [U3D specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) ovat saatavilla verkossa käyttäjien viitteeksi ECMA:n verkkosivustolla.

### Tietotyypit U3D-tiedostoissa

Binääritiedosto sisältää seuraavat tyypit: U8, U16, U32, U64, I16, I32, F32, F64 ja String.

 * U8: Etumerkitön 8-bittinen kokonaisluku
 * U16: Etumerkitön 16-bittinen kokonaisluku
 * U32: Etumerkitön 32-bittinen kokonaisluku
 * U64: Etumerkitön 64-bittinen kokonaisluku
 * I16: Etumerkillinen 16-bittinen kokonaisluku
 * F32: Yksittäinen IEEE-tarkkuuskelluke.
 * F64: IEEE kaksinkertainen tarkkuus kelluke.
 * Merkkijono: U3D-tiedoston merkkijonot alkavat etumerkittömällä 16-bittisellä kokonaisluvulla, joka määrittää merkkijonon merkkien kokonaispituuden. Merkkijonot käsitellään aina isot ja pienet kirjaimet huomioiden.

## U3D-tiedostorakenne

U3D-tiedosto sisältää sarjan lohkoja. Jokaisessa U3D-tiedostossa on 3 erityyppistä lohkoa.

 * Tiedoston otsikkolohko
 * Ilmoituslohko
 * Jatkolohko

Lataaja määrittää lohkon lopun, jos kyseisen lohkon tietoja ei vaadita tai jos dekooderia kyseiselle lohkotyypille ei ole saatavilla.

{{< figure src="../u3d.png" alt="U3D-tiedostomuoto" >}}

### Tiedoston otsikkolohko
Tiedoston otsikkolohko sisältää tiedostotietoja, joita ladattu käyttää määrittääkseen, kuinka tiedosto luetaan.

### Ilmoituslohko

Ilmoituslohkot sisältävät tietoa tiedoston objekteista. Ilmoituslohkon objektit on määriteltävä.

### Jatkolohko

Lisätietoa Declaration-lohkossa ilmoitetuista objekteista on jatkolohkossa. Jokainen jatkolohko on liitettävä ilmoituslohkoon.


## Viitteet ##

* [U3D-tiedostomuoto – Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)

* [ECMA U3D -tiedostomuodon tekniset tiedot](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)


