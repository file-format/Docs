{
  "date": "2021-24-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MKS tiedostomuoto",
  "keywords": [
"mks",
"matroska video",
"mkv muodossa",
"tiedosto",
"muoto",
"video"
],
  "description": "Opi MKS-tiedostomuodosta vain Matroskan luomille tekstityksille ja API:ista, jotka voivat luoda ja avata MKS-tiedostoja.",
  "linktitle": "MKS",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-fis"
}
},
  "lastmod": "2021-25-02"
}

## Mikä on MKS-tiedosto?

The MKS files are generally known as Matroska files containing subtitles only. Although the Matroska is a general file container, it avoids keeping the information of specific formats. Since subtitles are being used in some of the audio or video containers, Matroska is paying attention to store some common subtitle formats. It helps Matroska to be consistent with the growth rate. You need to follow the points as given below to store the subtitles in Matroska:

- .mks. laajennusta käyttää Matroska-tiedosto (sisältää vain tekstityksen).
- **CodecPrivate** käytetään tallentamaan kaikki koodekkeihin liittyvät tiedot, jotka ovat maailmanlaajuisia koko streamille.
- Poista aloitus- ja lopetusaikaleimat, joita käytetään aikaleiman alkuperäisessä tallennusmuodossa. Käytä sen sijaan Lohkojen aikaleimaa ja kestoa.
- Voit käyttää mitä tahansa läpinäkyvän kerroksen kanssa, myös videota.

## Yleiset tekstitysmuodot

Here are some brief notes about more common subtitle formats stored in Matroska:

### Kuvat Tekstitykset
VobSub-tekstitysmuoto on ensimmäinen kuvan tekstitysmuoto, joka tuodaan Matroskaan. Tämä muoto luodaan viemällä tekstitykset DVD-levyltä. Raidat tulee erottaa tallennuksen aikana Matroskaan, jos VobSub koostuu useista virroista.

### SRT Tekstitykset
The SRT is the most simple and basic of all subtitle formats. It consists of four parts as given below:
 
 1. Numero, joka ilmaisee tekstityksen järjestyksen.
 2. Tekstityksen ilmestymis- ja katoamisaika näytöllä.
 3. Itse tekstitys.
 4. Tyhjä rivi, joka osoittaa seuraavan tekstityksen alun.
 
### SSA/ASS tekstitykset
Sub Station Alpha (SSA) on suosittu tekstityseditori SubStation Alpha käyttämä tiedostomuoto. Fanit käyttävät laajasti SSA-tekstitystä. Se pystyy näyttämään moderneja ominaisuuksia, kuten karaokea, sijoittelua, tyyliä jne.
 
### WebVTT Tekstitykset
World Wide Web Consortium (W3C) kehitti WebVTT:n, jonka lyhenne on Web Video Text Tracks Format. Tätä muotoa käytetään ulkoisten tekstirataresurssien merkitsemiseen HTML-elementin yhteydessä.

### HDMV-esitysgrafiikkatekstitys
HDMV-esitysgrafiikkatekstitysmuoto (HDMV PGS) on sarja bittikarttoja, emmekä voi sanoa sitä tekstinä ollenkaan. Toisin sanoen, voit sanoa, että se on vain ajoitettu graafisten kuvien sarja. Tietojen poimimiseksi PGS:n muuntaminen SRT:ksi on välttämätön prosessi.

### HDMV-tekstitys
HDMV-teksti tunnetaan Blu-säteillä käytettävänä tekstitysmuotona. Matroska sallii vain UTF-8-merkkijoukon When tallentaa TextST-tekstitykset.

### Digital Video Broadcasting (DVB) -tekstitys
DVB-tekstitysmuoto otettiin käyttöön säätelemään useiden kielten tekstitysten lähetystä ja näyttöä TV-signaaleissa. Tyypillinen tekstitysmuoto mahdollistaisi myös kaikkien katsojien katsovan DVB-tekstitettyä lähetystä riippumatta siitä, mikä on lähetysjärjestelmien valmistaja.


## Viitteet ##

- [Matroska Subtitles](https://www.matroska.org/technical/subtitles.html)

