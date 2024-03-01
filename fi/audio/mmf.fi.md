{
  "date": "2021-08-09",
  "keywords": [
"mmf",
"tiedosto",
"laajennus",
"muoto",
"audio",
"smaf",
"mmf laajennus",
"mmf tiedostot",
"mobiili musiikkitiedosto",
"yamaha"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Opi MMF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MMF-tiedostoja.",
  "title": "MMF - Mobile Music -tiedostomuoto",
  "linktitle": "MMF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mm-fif"
}
},
  "lastmod": "2021-08-09"
}

## Mikä on MMF-tiedosto?

MMF on SMAF-tiedostoon liittyvä tiedostopääte. MMF tarkoittaa Mobile Music File -tiedostoa, kun taas SMAF tarkoittaa synteettisen musiikin mobiilisovellusmuotoa. Älypuhelimen MMF-tiedostot sisältävät järjestelmän soittoääniä, ääntä ja voivat sisältää myös grafiikkaa ja tekstinäyttöä. MMF sisältää lisäksi kolmen tyyppisiä instrumenttiparametreja, mukaan lukien FM, PCM ja Stream PCM. Nämä tiedostomuodot ovat yhteensopivia Windows-käyttöjärjestelmän kanssa. MMF-tiedostot luokitellaan datatiedostoiksi. Yleensä Microsoft Mail tukee MMF-tiedostoja. MMF-liitteen sisältävä tiedosto voidaan kopioida mihin tahansa mobiililaitteeseen tai järjestelmäalustalle.

Lisäksi nämä tiedostot ovat kooltaan paljon pienempiä kuin tavalliset MIDI-muotoiset tiedostot. [WAV](/audio/wav/)- ja [MID](/audio/mid/)-tiedostot voidaan muuntaa MMF-muotoon, joka voidaan sitten jakaa ja jakaa äänisisältönä. Nämä tiedostot voidaan vastaanottaa sähköpostitse suoraan puhelimiin ja tietokoneeseen.


## MMF-tiedostomuodon lyhyt historia

Yamaha kehitti SMAF-työkalut äänitiedostoiksi, jotta älypuhelimet voivat tallentaa suuremman määrän ainutlaatuisia soittoääniä. Yamaha esitteli SMAF:n MA-1-, MA-2-, MA-3-, MA-5- ja MA-7 LSI -äänipiirien tuotannossa. Kaikki nämä formaatit tulivat melko tutuiksi matkapuhelimissa Itä-Aasian markkinoilla vuoden 2000 alussa.

Kansainvälisellä tasolla MMF-muoto on Samsungin hyväksymä. MMF-muodon avulla Samsung pystyi suunnittelemaan laajan valikoiman polyfonisia soittoääniä käytettäviksi Samsungin älypuhelimissa.

Yamaha halusi tehdä formaatista entistä suositumman ja niin edelleen Yamaha virallisissa SMAF-tiedostoissa se julkaisi lisää tämän muodon kanssa yhteensopivia työkaluja. Tämän avulla käyttäjät voivat nyt helposti toistaa MMF-tiedostoja tietokoneillaan.


## MMF-tiedostomuodon tiedot ##

MMF-tiedostot on luokiteltu tietoosiin. Jokaisen segmentin kuvaamiseen käytetään 8-tavun ympärillä olevaa etuliiterakennetta.
4-tavuinen nimiö sisältää CNTI:n, OPDA:n, MSTR:n, MTR:n ja ATR:n. Datan koko plus 8 tavua on kappaleen koko; koko tiedoston koko lasketaan summaamalla kaikki osien koot. Jos tiedosto ei ole vaurioitunut, summatun tiedoston koon tulee olla sama kuin ensisijaisen otsikon koko.

### Otsikko ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Tässä on esimerkki MMF-tiedostosta:

!{{HYPERLINKKI1}}

## Viitteet

* [MMF - Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)


