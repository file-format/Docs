{
  "date": "2019-10-11",
  "keywords": [
"exif-tiedosto",
"exif-tiedostomuoto",
"mikä on exif-tiedosto",
"tiedosto",
"exif esimerkki",
"exif tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EXIF",
  "description": "Opi EXIF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata EXIF-tiedostoja.",
  "linktitle": "EXIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-exi-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on EXIF-tiedosto?
EXIF stands for “Exchangeable Image File Format”, the definition first given by [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) in 1985. Standardia hallinnoi Japan Electronics and Information Technology Industries Association (JEITA) tästä lähtien. EXIF on standardi kuva- ja ääniformaateille, joita käytetään pääasiassa digitaalikameroissa ja skannereissa.

EXIF-standardi sisältää kuvatiedoston merkinnät ja metatiedot. Metatiedot voivat sisältää tietoja, kuten kameran malli, suljinaika, päivämäärä ja aika, aukko, valmistaja, valotusaika, X-resoluutio, Y-resoluutio jne. Normaalisti EXIF-tiedot piilotetaan oletuksena. EXIF-tietojen tarkastelemiseksi on valittava näkymän ominaisuudet kuvankatselusovelluksessa. Exif-metatiedot voivat sisältää myös pikkukuvia sekä teknisiä ja ensisijaisia kuvatietoja yhdessä kuvatiedostossa.

## Historia ja versiot ##

* Lokakuussa 1995 JEIDA loi version 1. Tässä versiossa JEIDA määritteli rakenteen, joka koostuu kuvadatamuodosta ja attribuuttitiedoista sekä perustunnisteista.

* Marraskuu 1997, versio 1.1 otettiin käyttöön useimpien version 1 tagien kanssa, mutta siihen lisättiin myös säännöksiä valinnaisista attribuuttitiedoista ja muototoiminnasta.

* Kesäkuu 1998, versio 2, jossa on sRGB-väriavaruus, pakatut pikkukuvat ja äänitiedostot.

* Joulukuu 1998, versio 2.1 parannetulla tallennus- ja ominaisuustiedoilla.

* Helmikuu 2002, versio 2.2, parannettu versio 2.1, johon on lisätty tulostuksen viimeistely.

* Syyskuu 2003, versio 2.21 valinnaisella väriavaruudella, joka tunnetaan nimellä Adobe RGB.


## EXIF-tiedostomuoto

EXIF käyttää seuraavia tiedostomuotoja, joihin on lisätty tiettyjä metatietoja.

1. {{HYPERLINKKI}} - diskreetti kosinimuunnos (DCT) pakatuille kuvatiedostoille.
1. [TIFF](/image/tiff/) Versio 6.0 (RGB tai YCbCr) pakkaamattomille kuvatiedostoille.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) äänitiedostoille (Lineaarinen [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) tai ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM pakkaamattomalle äänidatalle ja [IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) pakattua äänidataa varten).

### EXIF:n käyttämä merkki ###

Merkki 0xFFE0~~0xFFEF on Application Marker, jota käyttäjäsovellus käyttää. Esimerkiksi vanhemmat digikamerat käyttävät JFIF:ää (JPEG File Interchange Format) kuvien tallentamiseen. JFIF käyttää APP0 (0xFFE0) -merkkiä digikameran asetustietojen ja pikkukuvan lisäämiseen. Lisäksi EXIF käyttää myös sovellusmerkkiä tietojen lisäämiseen, mutta EXIF käyttää APP1 (0xFFE1) -merkkiä välttääkseen ristiriidan JFIF-muodon kanssa. Jokainen EXIF-tiedostomuoto alkaa tästä muodosta.


|SOI-merkki|APP1-merkki|APP1-tiedot|Muu merkki
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Se alkaa SOI (0xFFD8) Markerista, joten se on JPEG-tiedosto. Sitten APP1 Marker seuraa välittömästi. Kaikki EXIF-tiedot tallennetaan tälle APP1-tietoalueelle. Ylätaulukon SSSS-osa tarkoittaa APP1-tietoalueen kokoa (EXIF-tietoalue). Huomaa, että koko SSSS sisältää myös itse kuvaajan koon. SSSS:n jälkeen APP1-tiedot alkavat. Ensimmäinen osa on erityinen tieto tunnistusta varten, onko käytössä EXIF vai ei, ASCII-merkki EXIF ja 2 tavua 0x00. APP1-merkkialueen jälkeen muut JPEG-merkit seuraavat.

### Exif-tietorakenne ###

EXIF-tietojen karkea rakenne (APP1) on esitetty alla. Kuten edellä mainittiin, EXIF-tiedot alkavat ASCII-merkistä EXIF ja 2 tavusta 0x00, sitten EXIF-tiedot seuraavat. EXIF käyttää TIFF-muotoa tietojen tallentamiseen.


|FFE1|APP1-merkki
---|---|
|SSSS|APP1-tiedot|APP1-tietojen koko
|45786966 0000|Exif-otsikko
|49492A00 08000000|TIFF-otsikko
|XXXX. . . .|IFD0 (pääkuva)|Hakemisto
|LLLLLLLL|Linkki IFD1:een
|XXXX. . . .|IFD0:n tietoalue
|XXXX. . . .|Exif SubIFD|hakemisto
|00000000|Linkin loppu
|XXXX. . . .|Exif SubIFD:n tietoalue
|XXXX. . . .|IFD1(pikkukuva)|Hakemisto
|00000000|Linkin loppu
|XXXX. . . .|IFD1:n tietoalue
|FFD8XXXX. . . XXXXFFD9|Pikkukuva

#### TIFF-otsikko ####

8-tavuisen [TIFF](/image/tiff/)-tiedoston otsikko sisältää seuraavat tiedot:

`Tavut 0-1:` Tiedostossa käytetty tavujärjestys. Lailliset arvot ovat:II(4949.H)MM (4D4D.H).

II-muodossa tavujärjestys on aina vähiten merkitsevästä tavusta merkittävimpään tavuun, sekä 16- että 32-bittisille kokonaisluvuille. Tätä kutsutaan little-endian tavujärjestykseksi. MM-muodossa tavujärjestys on aina merkittävimmästä vähiten merkitsevään, sekä 16- että 32-bittisille kokonaisluvuille. Tätä kutsutaan big endian tavujärjestykseksi.

`Tavut 2-3:` Satunnainen mutta huolellisesti valittu numero (42), joka edelleen tunnistaa tiedoston TIFF-tiedostoksi. Tavujärjestys riippuu tavujen 0-1 arvosta.

Tavut 4-7: Ensimmäisen IFD:n siirtymä (tavuina). Hakemisto voi olla missä tahansa tiedoston kohdassa otsikon jälkeen, mutta sen on alettava sanan rajalla. Erityisesti kuvatiedostohakemisto voi seurata kuvaamaansa kuvadataa. Lukijoiden on seurattava osoittimia minne tahansa ne johtavatkin. Termiä tavupoikkeama käytetään tässä asiakirjassa aina viittaamaan sijaintiin suhteessa TIFF-tiedoston alkuun. Tiedoston ensimmäisen tavun siirtymä on 0.

#### Kuvatiedostohakemisto ####

IFD sisältää tietoa kuvasta sekä osoittimia todellisiin kuvatietoihin. Se koostuu 2-tavuisesta hakemistomerkintöjen määrästä (eli kenttien määrästä), jota seuraa 12-tavuisten kenttämerkintöjen sarja , jota seuraa seuraavan IFD:n 4-tavuinen siirtymä (tai 0, jos ei yhtään). TIFF-tiedostossa on oltava vähintään yksi IFD ja jokaisessa IFD:ssä on oltava vähintään yksi merkintä.

##### IFD-merkintä #####

Jokainen 12-tavuinen IFD-merkintä on seuraavassa muodossa.


|Bytes|Kuvaus
---|---|
|0-1|tunniste, joka tunnistaa kentän
|2-3|Kenttätyyppi
|4-7|Määrätyn tyypin määrä
|8-11|Arvon siirtymä, kentän arvon tiedostosiirtymä (tavuina). Arvon odotetaan alkavan sanan rajalla; vastaava arvopoikkeama on siten parillinen luku. Tämä tiedostosiirtymä voi osoittaa minne tahansa tiedostossa, jopa kuvatietojen jälkeen

TIFF-kenttä on looginen kokonaisuus, joka koostuu TIFF-tunnisteesta ja sen arvosta. Tämä looginen konsepti toteutetaan IFD-merkinnänä, johon lisätään todellinen arvo, jos se ei mahdu arvo/offset-osaan, IFD-merkinnän 4 viimeistä tavua. Termit TIFF-kenttä ja IFD-merkintä ovat vaihdettavissa useimmissa yhteyksissä.

#### Pikkukuva ####

Exif format contains thumbnail of image (except Ricoh RDC-300Z). Usually it is located next to the IFD1. Pikkukuville on kolme muotoa; JPEG-muoto (JPEG käyttää YCbCr-muotoa), RGB TIFF -muoto, YCbCr TIFF-muoto.

##### JPEG-muodossa pikkukuva #####

If the value of Compression(0x0103) Tag in IFD1 is '6', thumbnail image format is JPEG. Most of Exif image uses JPEG format for thumbnail. In that case, you can get offset of thumbnail by JpegIFOffset(0x0201) Tag in IFD1, size of thumbnail by JpegIFByteCount(0x0202) Tag. Data format is ordinary JPEG format, starts from 0xFFD8 and ends by 0xFFD9. Näyttää siltä, että JPEG-muoto ja 160x120 pikselin koko ovat suositeltuja pikkukuvamuotoja Exif2.1:lle tai uudemmalle.

##### TIFF-muodossa pikkukuva #####

Jos Compression(0x0103) -tunnisteen arvo IFD1:ssä on '1', pikkukuvamuoto ei ole pakkaus (kutsutaan TIFF-kuvaksi). Pikkukuvatietojen aloituskohta on StripOffset(0x0111) Tag, pikkukuvan koko on StripByteCounts(0x0117) -tunnisteen summa.

## Viitteet ##

* [EXIF - Wikipedia](https://en.wikipedia.org/wiki/Exif)

* [EXIF-tiedostomuoto](https://www.media.mit.edu/pia/Research/deepview/exif.html)


