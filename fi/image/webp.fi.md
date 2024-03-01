{
  "date": "2019-10-11",
  "keywords": [
"webp-tiedosto",
"webp-tiedostomuoto",
"mikä on webp-tiedosto",
"tiedosto",
"webp esimerkki",
"webp tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WEBP - Googlen rasterikuvatiedostomuoto",
  "description": "Opi WEBP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WEBP-tiedostoja.",
  "linktitle": "WEBP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-webp"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on WEBP-tiedosto?

Googlen esittelemä WebP on moderni rasteriverkkokuvatiedostomuoto, joka perustuu häviöttömään ja häviölliseen pakkaamiseen. Se tarjoaa saman kuvanlaadun ja pienentää samalla kuvan kokoa huomattavasti. Koska useimmat web-sivut käyttävät kuvia tehokkaana esityksenä datasta, WebP-kuvien käyttö verkkosivuilla johtaa verkkosivujen nopeampaan lataamiseen. Googlen mukaan häviöttömät WebP-kuvat ovat kooltaan 26 % pienempiä kuin [PNGs](/image/png/), kun taas WebP-häviölliset kuvat ovat 25-34 % pienempiä kuin vastaavat [JPEG](/image/jpeg/)-kuvat. Kuvia verrataan WebP:n ja muiden kuvatiedostomuotojen välillä SSIM-indeksin (Strukturaalinen samankaltaisuus) perusteella. WebP on [WebM](https://en.wikipedia.org/wiki/WebM)-multimediasäilömuodon sisarprojekti.

## WebP-ominaisuuksien yleiskatsaus ##

WebP-kuvat käyttävät pakkausprosessia, joka perustuu ympäröivien lohkojen pikselien ennustamiseen, jolloin pikseleitä käytetään useita kertoja yhdessä tiedostossa. Se tukee animoituja kuvia, ja sen odotetaan tukevan lisää ominaisuuksia tulevaisuudessa. Google on asettanut saataville lähdekoodin [online](https://developers.google.com/speed/webp/download) kooderilleen ja dekooderilleen, jotta sitä voidaan käyttää tarvittaessa. WebP-kuva tukee:

* **Häviöllinen pakkaus:** Häviöllinen pakkaus perustuu [VP8](https://en.wikipedia.org/wiki/VP8) avainkehysten koodaukseen. VP8 on videon pakkausmuoto, jonka On2 Technologies on luonut VP6- ja VP7-muotojen seuraajaksi.

* ** Häviötön pakkaus:** Häviöttömän pakkausmuodon on kehittänyt WebP-tiimi.

* **Läpinäkyvyys:** 8-bittinen alfakanava on hyödyllinen graafisille kuville. Alfa-kanavaa voidaan käyttää yhdessä häviöllisen RGB:n kanssa. Tämä ominaisuus ei ole tällä hetkellä käytettävissä missään muussa muodossa.

* **Animaatio:** Se tukee tosivärisiä animoituja kuvia.

* **Metatiedot:** Siinä voi olla EXIF- ja XMP-metatietoja (esimerkiksi kameroiden käyttämät).

* **Väriprofiili:** Siinä voi olla upotettu ICC-profiili.


Häviöllinen WebP-pakkaus käyttää ennakoivaa koodausta kuvan koodaamiseen, samaa menetelmää, jota VP8-videokoodekki käyttää avainkehysten pakkaamiseen videoissa. Ennustava koodaus käyttää vierekkäisten pikselilohkojen arvoja ennustamaan lohkon arvot ja koodaa sitten vain eron.

Häviötön WebP-pakkaus käyttää jo nähtyjä kuvafragmentteja uusien pikselien rekonstruoimiseksi tarkasti. Se voi myös käyttää paikallista palettia, jos mielenkiintoista vastaavuutta ei löydy.

## Tiedosto muoto ##

WebP-tiedostomuoto perustuu RIFF-dokumenttimuotoon (resurssinvaihtotiedostomuoto). WebP-säilö tukee enemmän ja enemmän ominaisuuksia kuin vain yhden VP8-avainkehykseksi koodatun kuvan sisältämistä. RIFF-tiedoston peruselementti on pala, joka koostuu:


|Kenttä|Kuvaus
---|---|
|Chunk FourCC: 32 bittiä|nelimerkkinen ASCII-koodi, jota käytetään kappaleen tunnistamiseen
|Chunk Size: 32 bits (uint32)|The size of the chunk not including this field, the chunk identifier or paddi-fing
|Osan hyötykuorma: Osan koko tavua|Tietojen hyötykuorma. Jos kappaleen koko on pariton, lisätään yksi täytetavu ~-~-, jonka pitäisi olla 0 ~-~-
|ChunkHeader ('ABCD')|Käytetään kuvaamaan yksittäisten kappaleiden FourCC- ja Chunk Size -otsikkoa, jossa ABCD on kappaleen FourCC. Tämän elementin koko on 8 tavua.

### WebP-otsikko ###

WebP-tiedoston otsikko on seuraava:

* RIFF-otsikko - 32 bittiä, jotka edustavat ASCII-merkkejä 'R' 'I' 'F' 'F'

* Tiedoston koko - 32 bittiä (uint32), joka edustaa tiedoston kokoa tavuina alkaen offsetista 8. Tämän kentän enimmäisarvo on 2^32 miinus 10 tavua ja siten koko tiedoston koko on enintään 4 GiB miinus 2 tavua .

* 'WEBP' - 32 bittiä, jotka edustavat ASCII-merkkejä 'W' 'E' 'B' 'P'


### Häviöinen tiedostomuoto ###

WebP-kuvat käyttävät häviöllistä tiedostomuotoa, jos kuva perustuu häviölliseen koodaukseen eikä vaadi lisäominaisuuksia, kuten läpinäkyvyyttä, animointia, alfaa jne. Häviölliset kuvat ovat pienempiä ja myös vanhemmat sovellukset tukevat niitä.

WebP-tiedosto koostuu tässä tapauksessa:

* 12 tavua WebP-tiedoston otsikko

* VP8 pala


{{HYPERLINKKI}} havainnollistaa VP8-bittivirran muotomäärityksiä.

### Häviötön tiedostomuoto ###

Tätä asettelua käytetään, kun kuva perustuu häviämättömään koodaukseen eikä ulkoisen muodon tarjoamia lisäominaisuuksia tarvita. Vanhemmat sovellukset eivät kuitenkaan välttämättä pysty lukemaan tällaisia tiedostoja.

WebP-tiedosto koostuu tässä tapauksessa:

* 12 tavua WebP-tiedoston otsikko

* VP8L pala


## Viitteet ##

* [WebP Developer's Reference - Google](https://developers.google.com/speed/webp/)

* [WebP-tiedostomuoto - Wikipedia](https://en.wikipedia.org/wiki/WebP)


