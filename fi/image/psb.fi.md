{
  "date": "2019-10-11",
  "keywords": [
"psb-tiedosto",
"psb-tiedostomuoto",
"mikä on psb-tiedosto",
"tiedosto",
"psb esimerkki",
"psb tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSB - Photoshop Big Image File Format",
  "description": "Opi PSB-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata PSB-tiedostoja.",
  "linktitle": "PSB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-fib"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on PSB-tiedosto?
Adobe Photoshop tallentaa tiedostot kahdessa muodossa. Tiedostot, joiden koko on 30 000 x 30 000 pikseliä, tallennetaan PSD-laajennuksella ja tiedostot, jotka ovat suurempia kuin PSD, jopa 300 000 x 300 000 pikseliä, tallennetaan PSB-laajennuksella, joka tunnetaan nimellä Photoshop Big. Tarkemmin sanottuna PSB-tiedostot voivat olla jopa 4 EB:n kokoisia (yli 4,2 miljardia Gt), joiden korkeus ja leveys on jopa 300 000 pikseliä. PSD-levyt voivat toisaalta olla enintään 2 Gt ja kuvan mitat 30 000 pikseliä.

PSB is also known as large format size for photoshop and supports all the photoshop features like layers, effects and filters.Photoshop can convert PSB file to [PSD](/image/psd/), [JPG](/image/jpeg/), [PNG](/image/png/), [EPS](/page-description-language/eps/), [GIF](/image/gif/) and other formats as well. Photoshop large document format is available once the feature of file handling pane of Photoshop’s preferences dialog box is enabled.

## Tiedostomuodon tiedot ##

Photoshop-tiedostomuoto on jaettu viiteen suureen osaan, joissa on useita pituusmerkkejä osioiden välillä liikkumista varten.

|Tiedostomuoto
---|
|Tiedoston otsikko
|Väritilan tiedot
| Kuvaresurssit
| Kerros- ja maskitiedot
|((((
Kuvatiedot
)))

### Tiedoston otsikko ###

Tiedoston otsikon kiinteä pituus on 26 tavua ja se sisältää kuvan perusominaisuudet.

BYTE Signature [4] – vastaa '8BPS'.

WORD-versio [2] – versionumero, PSD # 1, PSB # 2.

BYTE Varattu [6] – Varattu ja aina nolla.

WORD-kanavat [2] – Kuvan värikanavien määrä alfakanavat mukaan lukien. Sen arvo vaihtelee välillä 1-56.

PITKÄT rivit [4] – Kuvan korkeus pikseleinä, PSD 1-30 000, PSB 1-300 000.

PITKÄT Sarakkeet [4] – Kuvan leveys pikseleinä, PSD 1-30 000, PSB 1-300 000.

WORD Depth [2] – Bittien määrä kanavaa kohti. Tuetut arvot ovat 1,8,16 ja 32.

WORD Mode [2] – tiedoston väritila.

#### Tilan kuvaus ####


|Tila|Kuvaus
---|---|
|0|Bittikartta (yksivärinen)
|1|Harmaasävy
|2|Indeksoitu
|3|RGB
|4|CMYK
|7|Monikanava
|8|Duotone (puolisävy)
|9|Lab

### Väritilan tiedot ###

Tiedoston otsikkoosion jälkeen seuraa väritilan tietoosio. Lohko alkaa LONG-numerolla, joka ilmoittaa lohkon pituuden tavuina. Väritilatietojen rakenne on seuraava:

4 tavua – Seuraavien väritietojen pituus.

Muuttuva – Väritiedot

Jos otsikko-osion tilakentän arvo ei ole Indeksoitu väri tai kaksisävy, lohkon pituus on 0 eikä pituuskentän jälkeen ole dataa.

Indeksoitujen värikuvien pituus on 768 tavua, joka sisältää 256 väripaletin. Kaksoisäänen tiedot sisältävät näytön parametreja ja muita asiaan liittyviä tietoja.

### Kuvaresurssit ###

Väritilan dataosan jälkeen kolmas lohko on kuvaresurssiosio. Ensimmäiset neljä tavua ovat LONG-luku, joka määrittää lohkon pituuden, jota seuraa sarja resurssilohkoja. Kuvaresurssilohkon rakenne on seuraava:

BYTE-tyyppi [4] – Allekirjoitus '8BIM

WORD ID [2] – Kuvaresurssin tunnus. Siellä on luettelo resurssitunnuksista, jotka näkyvät viitelinkistä.

BYTE Name [Variable] – Nimi: Pascal-merkkijono, jonka pituus on parillinen. ***

LONG Size [4] – Seuraavien resurssitietojen todellinen koko.

BYTE Data [Variable} – Resurssitiedot. Se on pehmustettu tasaisen koon saamiseksi.

Joitakin resurssimuotoja selitetään lyhyesti alla:

**Grid and Guides Resource Format:** Grid and Guides -tiedot tallennetaan resurssilohkoon. Nämä resurssilohkot sisältävät 16-tavuisen ruudukon ja opasotsikon, jota seuraa 5-tavuinen opastietolohko.

**Pikkukuvan resurssimuoto:** Pikkukuvatiedot tallennetaan esikatselun kuvaresurssilohkoon, joka koostuu 28-tavuisesta otsikosta ja JFIF-pikkukuvasta RGB-muodossa.

**Värinäytteiden resurssimuoto:** Värinäytteiden tiedot tallennetaan kuvaresurssilohkoon, jossa on 8-tavuinen otsikko, jota seuraa muuttuvapituinen värinäytteenottotietojen lohko.

### Kerros- ja maskitiedot ###

Neljäs lohko on kerros- ja maskitietolohko ja sisältää tietoa kerroksista ja maskeista. Ensin tallennetaan kerrostiedot ja sitten maskitiedot.

**Kerrostiedot:** Tasotiedot alkavat LONG-arvolla, joka osoittaa tasotietojen pituuden. Sen jälkeen on WORD-arvojen määrä, joka näyttää seuraavien tasotietueiden määrän.

[8] – kerrosten pituus

[2] – Kerrosten määrä

[Muuttuja] – Tietoja jokaisesta tasosta.

[Muuttuja] – Kanavan kuvatiedot.** **

**Maskin tiedot:** Maskin rakenne on seuraavassa muodossa:


|Tietorakenne|Kentän nimi| Kuvaus
---|---|---|
|SANA| Peittokuvan väriavaruus| (Ei dokumentoitu)
|BYTE[8]| Värikomponentit| 4x2 tavun värikomponentit
|SANA| Opacity| 0#läpinäkyvä, 1#läpinäkyvä
|BYTE| Kiltti| 0#käänteinen, 1#suojattu, 128#käytä tallennettua arvoa
|BYTE| pehmuste| asetettu nollaan

### Kuvatiedot ###

Viimeinen osa sisältää kuvan pikselitiedot. Kuvadata tallennetaan sarjana tasoihin eli ensin kaikki punaiset tiedot, sitten kaikki vihreät tiedot jne. WORD jokaisen rivin alussa näyttää kunkin skannausrivin koon tavuina.

[2] – Pakkausmenetelmä:

[Muuttuja] – Kuvatiedot tasojärjestyksessä, esim. RRRR, GGGG, BBBB jne.

Pakkausmenetelmät:

0 – Raw Kuvatiedot

1 – RLE Pakattu

2 – Vetoketju ilman ennustetta

3 – Vetoketju ennusteella

## Viite ##

* [PSB-tiedostomuoto – Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

* [PSB – Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


