{
  "date": "2019-10-11",
  "keywords": [
"M4V",
"tiedosto",
"laajennus",
"muoto",
"MPEG-4",
"Digitaalinen oikeuksien hallinta",
"DRM",
"Omena",
"video"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4V",
  "description": "Opi M4V-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata M4V-tiedostoja.",
  "linktitle": "M4V",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-fiv"
}
},
  "lastmod": "2019-09-14"
}

## Mikä on M4V-tiedosto?

**M4V** file format, developed by Apple, is a video container optionally protected with Digital Rights Management (DRM) copy protection to protect privacy or copy. Videos and audio tracks are wrapped around by container files to indexing and organizing playback streams. In addition, containers also provide the feature of chapters similar to those on DVDs. Apple uses M4V to encode videos in its iTunes Store. It protects unauthorized reproduction through Apple’s FairPlay copy protection by allowing M4V files to be played on only authorized computers having the accounts used to purchase the video. However, if DRM-protection is removed from M4V files, these files can be played in other video players by changing the extension from .m4v to .mp4, which is why M4V files are associated with MPEG-4. M4V käyttää H.264:ää videolle ja **[AAC](/audio/aac/)** ja Dolby Digitalia äänen koodaukseen ja dekoodaukseen.

## M4V-tiedostorakenne ##

M4V files have continuous chunks with 8 byte header, 4 byte chunk size and 4 byte chunk type in each chunk. First chunk is “ftype” and has a sub-type at offset 8. M4V määritellään alatyypillä, jonka on oltava M4V_. Muut palotyypit ovat ennalta määritettyjä allekirjoituksia: ftyp, mdat, moov, pnot, udta, uuid, moof, ilmainen, ohita, jP2, leveä , load, ctab, imap, matt, kmat, clip, crgn, sync, chap, tmcd, scpt, ssrc,  KUVA. Toistamme paloja, kunnes tuntematon tyyppi havaitaan, muodostamme M4V-tiedoston.

Here is an examination of a sample: A sample m4v file’s binary data is inspected through Hex Viewer and it can be observed that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **M4V_** (hex: 4D 34 56 20) which points to M4V (MPEG-4) file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Siirtymässä 32 (heksa: 20) sijaitsee toinen pala, jonka koko on 30 322 (heksa: 00 00 76 72, big-endian, alempi tavu ensin) ja tyyppi **moov** (heksa: 6D 6F 6F 76). Seuraava pala sijaitsee offsetissa 32+30,322#30,354 (heksa: 00 00 76 92), ja sen koko on 8 (heksa: 00 00 00 08) ja tyyppi **free** (heksa: 66 72 65 65).
### M4V:ssä käytetyt koodekit ###

#### Videokoodekki H.264 ####

H.264 on videon pakkausstandardi, joka muuntaa digitaalisen videon muotoon, joka vaatii vähemmän tilaa, kun sitä tarvitaan lähetystä tai tallennusta varten. M4V käyttää H.264:ää videon pakkaamiseen. Sen sovellusalueet vaihtelevat DVD:stä, televisiosta, videoneuvotteluista ja videoiden suoratoistosta Internetin kautta. H.264 koostuu kahdesta pääosasta: Encoder – joka pakkaa videon, Dekooderi – joka purkaa pakatun videon takaisin. Alla olevassa kuvassa koodaus- ja dekoodausprosessit on korostettu, ja muut prosessit käsitellään H.264-standardissa.

##### Videon koodaus- ja dekoodausprosessi H.264:ssä #####

Pakatun H.264-bittivirran tapauksessa videokooderi suorittaa ennustus-, muunnos- ja koodausprosessin. Samanaikaisesti dekooderi suorittaa käänteisen dekoodaus-, käänteismuunnos- ja rekonstruointiprosessin tuottaakseen takaisin videotiedoston. H.264 kestää puolet MPEG:n koosta.

#### Äänikoodekki ####

Advanced Audio Coding (AAC) on audiokoodekki häviölliseen digitaaliseen äänenpakkaukseen, ja sitä käytetään M4V-säiliössä. AAC on [MP3](/audio/mp3/)-muodon seuraaja, ja sen laatu on parempi kuin MP3 samalla bittinopeudella. AAC-muoto heittää pois joitakin tietoja pakkausprosessin aikana, mikä on vähemmän tärkeää. AAC on muuttuvan bittinopeuden (VBR) lohkopohjainen koodekki, jossa jokainen lohko dekoodaa 1024 aikatason näytteeksi.

### Referenssit ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)

* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)


