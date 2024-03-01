{
  "date": "2019-10-11",
  "keywords": [
"psd tiedosto",
"psd tiedostomuoto",
"mikä on psd-tiedosto",
"tiedosto",
"psd esimerkki",
"psd tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSD - Photoshop-kuvatiedostomuoto",
  "description": "Opi PSD-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PSD-tiedostoja.",
  "linktitle": "PSD",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-fid"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on PSD-tiedosto?

PSD, Photoshop Document, edustaa Adobe Photoshopin alkuperäistä tiedostomuotoa, jota käytetään grafiikan suunnitteluun ja kehittämiseen. PSD-tiedostot voivat sisältää kuvakerroksia, säätökerroksia, kerrosmaskeja, huomautuksia, tiedostotietoja, avainsanoja ja muita Photoshop-kohtaisia elementtejä. Photoshop-tiedostojen oletustunniste on .PSD, ja niiden enimmäiskorkeus ja -leveys on 30 000 pikseliä ja pituusrajoitus kaksi gigatavua.

## PSD-tiedostomuodon tekniset tiedot ##

PSD-tiedoston tiedot tallennetaan big endian tavujärjestyksessä. Tämä tarkoittaa lyhyiden ja pitkien kokonaislukujen vaihtamista, kun luet tai kirjoitat Windows-alustalla. Photoshop-tiedostomuoto on jaettu viiteen suureen osaan. Siinä on monia pituusmerkkejä, joiden avulla voidaan siirtyä osasta toiseen. Pituusmerkit on yleensä täytetty tavuilla pyöristääkseen lähimpään 2 tai 4 tavun väliin. Viisi pääosaa ovat:

* Tiedoston otsikko

* Väritilan tiedot

* Kuvaresurssit

* Kerros- ja maskitiedot

* Kuvatiedot


Yhdenmukaisuuden vuoksi tiedot tulee kirjoittaa kaikkiin näihin osion kenttiin, koska Photoshop saattaa yrittää lukea koko osan. Se tarkoittaa myös, että ohitettuihin kenttiin kirjoitetaan nollia tiedostoon kirjoitettaessa. Pituuseroteltujen osien pituuskenttää tulee käyttää päätettäessä, milloin lukeminen lopetetaan. Useimmissa tapauksissa pituuskenttä osoittaa seuraavien tavujen määrän, ei tietueita. Seuraavat seikat on muistettava tiedostoa luettaessa.

* Kaikkien taulukoiden "Pituus"-sarakkeen arvot ovat tavuina.

* Kaikki Unicode-merkkijonoksi määritellyt arvot koostuvat seuraavista:

* 4 tavun pituinen kenttä, joka edustaa merkkijonon merkkien määrää (ei tavuja).

* Unicode-arvojen merkkijono, kaksi tavua per merkki.


### Tiedoston otsikko ###

Tiedoston otsikko sisältää kuvan perusominaisuudet.

|Pituus|Kuvaus
---|---|
|4|Allekirjoitus: aina yhtä kuin '8BPS' . Älä yritä lukea tiedostoa, jos allekirjoitus ei vastaa tätä arvoa.
|2|Version: always equal to 1. Älä yritä lukea tiedostoa, jos versio ei vastaa tätä arvoa. (~*~*PSB~*~* versio on 2.)
|6|Varattu: on oltava nolla.
|2|Kuvan kanavien määrä, mukaan lukien alfakanavat. Tuettu alue on 1-56.
|4|Kuvan korkeus pikseleinä. Tuettu alue on 1–30 000.
|4|Kuvan leveys pikseleinä. Tuettu alue on 1–30 000.
|2|Syvyys: bittien määrä kanavaa kohti. Tuetut arvot ovat 1, 8, 16 ja 32.
|2|Tiedoston väritila. Tuetut arvot ovat: Bitmap # 0; Harmaasävy # 1; Indeksoitu # 2; RGB # 3; CMYK # 4; Monikanava #7; Duuotone # 8; Lab #9.

### Väritilan tietoosio ###

Väritilan tietoosio on rakennettu seuraavasti:


|Pituus|Kuvaus
---|---|
|4|Seuraavien väritietojen pituus
|muuttuja|Väritiedot

Väritilan tiedot ovat saatavilla vain indeksoiduille väreille ja kaksisävyille, jotka on määritetty Tiedostootsikko-osan tilakentässä. Kaikissa muissa tiloissa tätä osaa edustavat 4-tavuiset nollatut arvot. Indeksoitujen värikuvien pituus on 768 ja väritiedot sisältävät kuvan väritaulukon ei-lomitetussa järjestyksessä. Duuotone-kuvien väritiedot sisältävät duotone-määrityksen (jonka muotoa ei ole dokumentoitu). Muut Photoshop-tiedostoja lukevat sovellukset voivat käsitellä kaksisävyistä kuvaa harmaana kuvana ja vain säilyttää kaksisävytietojen sisällön tiedostoa lukiessaan ja kirjoittaessaan.

### Kuvaresurssit -osio ###

Tiedoston kolmas osa sisältää kuvaresursseja. Se alkaa pituuskentällä, jota seuraa joukko resurssilohkoja.


|Pituus|Kuvaus
---|---|
|4|Kuvaresurssiosan pituus. Pituus voi olla nolla.
|Muuttuja|Kuvaresurssit (Kuvaresurssilohkot)

Kuvaresursseja käytetään kuviin liittyvien ei-pikselitietojen, kuten kynätyökalupolkujen, tallentamiseen. Niitä kutsutaan resurssilohkoiksi, koska ne sisältävät tietoja, jotka on tallennettu Macintoshin resurssiin Photoshopin varhaisissa versioissa. Kuvaresurssilohkojen perusrakenne on seuraava:


|Pituus|Kuvaus
---|---|
|4|Allekirjoitus: '8BIM
|2|Resurssin yksilöllinen tunniste. Kuvaresurssien tunnukset sisältävät luettelon Photoshopin käyttämistä resurssitunnuksista.
|Muuttuja|Nimi: Pascal-merkkijono, täytetty koon tasaamiseksi (nollanimi koostuu kahdesta tavusta 0)
|4|Seuraavan resurssitietojen todellinen koko
|Muuttuja|Resurssitiedot, jotka on kuvattu yksittäisiä resurssityyppejä koskevissa osioissa. Se on pehmustettu, jotta koko olisi tasainen.

Kuvaresurssit käyttävät useita vakiotunnusnumeroita.

### Kerros- ja maskitiedot ###

Photoshop-tiedoston neljäs osa sisältää tietoja tasoista ja maskeista, kuten kerrosten lukumäärästä, tasojen kanavista, sekoitusalueista, säätötasojen näppäimistä, tehostetasoista ja maskin parametreista. Jos tasoja tai maskeja ei ole, tämä osa esitetään nollatulla 4-tavuisella kentällä. Erityistä huomiota on kiinnitettävä osien pituuteen tätä jaksoa luettaessa nollattujen arvojen vuoksi. Kerros- ja maski-osion järjestely on seuraava:


|Pituus|Kuvaus
---|---|
|4|Tason ja maskin tietoosion pituus. (PSB:n pituus on 8 tavua.)
|Muuttuja|Tasotiedot
|Variable|Global kerrosmaskin tiedot
|Variable|Sarja merkittyjä lohkoja, jotka sisältävät erityyppisiä tietoja.

#### Tason tiedot ####

Seuraava taulukko näyttää kerrostietojen korkean tason organisoinnin.


|Pituus|Kuvaus
---|---|
|4|Length of the layers info section, rounded up to a multiple of 2. (PSB:n pituus on 8 tavua.)
|2|Kerrosten määrä. Jos se on negatiivinen luku, sen absoluuttinen arvo on kerrosten lukumäärä ja ensimmäinen alfakanava sisältää läpinäkyvyystiedot yhdistetylle tulokselle.
|Muuttuja|Tiedot jokaisesta tasosta. Kohdassa Tasotietueet kuvataan näiden tietojen rakennetta kullekin tasolle.
|Muuttuja|Kanavan kuvatiedot. Sisältää yhden tai useamman kuvatietotietueen jokaiselle tasolle. Tasot ovat samassa järjestyksessä kuin kerrostiedoissa

### Kuvatiedot ###

Kuvan pikselitiedot sisältyvät tiedoston Kuvatiedot-osioon. Tietojen järjestys Image Data -osiossa on tasojärjestyksessä eli ensin kaikki punaiset tiedot, sitten kaikki vihreät tiedot jne. Jokainen taso tallennetaan skannausrivijärjestyksessä, ilman padtavuja. Kuvadata-osio on järjestetty muotoon kuten seuraavassa taulukossa näkyy.

|Pituus|Kuvaus
---|---|
|2|Compression method: *0 = Raw image data * 1 = RLE-pakattu kuvatiedot alkavat kaikkien skannausrivien (rivit * kanavat) tavumäärästä, ja jokainen määrä tallennetaan kaksitavuisena arvona. RLE-pakatut tiedot seuraavat, ja jokainen skannausrivi pakataan erikseen. RLE-pakkaus on sama pakkausalgoritmi, jota käyttävät Macintoshin ROM-rutiini PackBits ja TIFF-standardi. *2 = ZIP ilman ennustetta *3 = ZIP ennusteella.
|Muuttuja|Kuvatiedot. Tasojärjestys = RRR GGG BBB jne.

## Viitteet ##

* [PSD-tiedostomuodon tekniset tiedot – Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)

* [Adobe Photoshop -tiedostomuoto](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


