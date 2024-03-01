{
  "date": "2019-10-11",
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "title": "MKV tiedostomuoto",
  "keywords": [
"mkv",
"matroska video",
"mkv muodossa",
"kuinka toistaa mkv-tiedostoja",
"video",
"tiedosto",
"muoto"
],
  "description": "Opi MKV-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MKV-tiedostoja.",
  "linktitle": "MKV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-fiv"
}
},
  "lastmod": "2020-17-11"
}


## Mikä on MKV-tiedosto? ##

MKV (Matroska Video) is a multimedia container similar to [MOV](/video/mov/) and [AVI](/video/avi/) format but it supports more than one audio and subtitle track in the same file. An MKV file is the Matroska multimedia container format used for video. MKV is based on Extensible Binary Meta Language and it supports several video and audio compression formats. The major difference between MKV and other video formats is that MKV is a container and not a codec. MKV files are saved with the .mkv file extension. MKV can incorporate audio, video, and subtitles in a single file even if those elements use different types of encoding. For example, you could have an MKV file that contains H.264 video and MP3 or AAC for audio. MKV also supports descriptions, ratings, cover art, and even chapter points. There are several key features that MKV is future-proof. These features include:

- Tuki nopealle etsimiselle.
- Mahdollisuus valita erilaisia ääni- ja videovirtoja.
- Tuki tekstityksille (kovakoodattu ja pehmeä koodattu).
- Tuki metadatalle, luvuille ja valikoille.
- Mahdollisuus suoratoistaa verkossa.
- Mahdollisuus palauttaa virheelliset tiedostot, jotka mahdollistavat vioittuneiden tiedostojen toistamisen.

## Lyhyt historia ##

MKV-tiedosto syntyi vuonna 2002 Venäjältä. Pääkehittäjänä toimi Lasse Kärkkäinen, joka työskenteli Matroskan perustajan Steve Lhommen ja ohjelmoijatiimin kanssa. MKV kehitettiin avoimen standardin projektiksi, mikä tarkoittaa, että se on avoimen lähdekoodin ja vapaasti käytettävä. Ajan myötä muotoa parannettiin ja siitä tuli WebM-multimediaformaatin perusta vuonna 2010.

## Matroska Design ##

Matroska lisää seuraavat rajoitukset EBML-spesifikaatioon.

- **EBML-otsikon** **docType** on oltava matroska.
- **EBML-otsikon** **EBMLMaxIDLength**-arvon on oltava 4.
- **EBML-otsikon** **EBMLMaxSizeLength**-arvon on oltava välillä 1–8 (mukaan lukien).

Kaikki huipputason elementit on koodattu 4 oktetilla.

- Kielikoodit: Matroska (versiot 1–3) käytti kielikoodeja, jotka voivat olla joko 3-kirjaimista bibliografista ISO-639-2-muotoa (kuten fre ranskaksi) tai muita maakoodeja, kuten fre-ca.  Kanadan ranskaksi. Matroska-versiosta 4 alkaen kielikoodeihin VOIDAAN käyttää joko ISO 639-2:ta tai BCP 47:ää, vaikka BCP 47:ää suositellaan.
- Fyysiset tyypit: Näillä on eri merkitys sekä ääni- että videotiedostoille. Esimerkiksi ChapterPhysicalEquiv = 60 tarkoittaa (CD / 12 / 10 / 7 / TAPE / MINIDISC / DAT) audiolle ja (DVD / VHS / LASERDISC) videolle.
- Lohkon rakenne - Lohkon otsikko: Lohkon otsikko sisältää tietoa kappaleen numerosta, aikaleimoista, nauhatyypistä jne.
- Nauhoitus: Se on mekanismi, joka säästää tilaa tallennettaessa tietoja, joita tyypillisesti käytetään pienille tietolohkoille (kehyksille). Nauhoja on 3 tyyppiä:
  - "Xiph: Kehys, jonka koon kerrannainen 255 on koodattu 0:lla koon lopussa. Esimerkiksi 765:n koodi on 255;255;255;0."
  - "EBML: Kehyksen koko on koodattu erona edellisen koon ja tämän koon välillä. Pitsien ensimmäinen koko on allekirjoittamaton, mutta toiset käyttävät alueen siirtoa saadakseen merkin jokaiseen arvoon."
  - "kiinteä koko: Koko pysyy samana."
- Yksinkertainen lohkorakenne: Se on saanut inspiraationsa **Block-rakenteesta**, ja suurin ero on **Keyframe**- ja **Discardable** -lippujen lisääminen. Muuten kaikki on samaa.

## Matroska-rakenne ##

Matroska-asiakirjan on koostuttava vähintään yhdestä **EBML-asiakirjasta**, joka käyttää **Matroska-asiakirjatyyppiä**. Jokaisen **EBML-asiakirjan** on aloitettava **EBML-otsikolla**, jota seuraa segmentiksi määritelty **EBML-juurielementti**. Matroska määrittelee useita huipputason elementtejä, joita voi esiintyä **segmentissä**.

EBML käyttää elementtijärjestelmää EBML-dokumentin laatimiseen. Seuraava on luettelo Matroska-tiedoston huipputason elementeistä:

- **EBML-asiakirja**: Koko tiedoston kääre.
- **EBML Header**: Se sisältää otsikkotiedot tiedostolle, kuten DocType.
- **Segmentti**: Ylin elementti, joka sisältää kaikki muut ylätason elementit.
- **SeekHead**: Se sisältää muiden huipputason elementtien segmenttien sijainnin.
- **Info**: Se sisältää yleistä tietoa segmentistä.
- **Raidat**: Huipputason tietoelementti, jossa on useita kuvattuja kappaleita.
- **Chapters**: It is used to define basic menus and partition data.
- **Cluster**: ylätason elementti, joka sisältää lohkorakenteen.
- **Cues**: huipputason elementti, joka sisältää kaikki segmentin paikalliset merkinnät, jotka hakevat pääsyä nopeasti.
- **Liitteet**: Tämä sisältää liitetiedostoja.
- **Tagit**: Tämä elementti sisältää metatietoja, jotka kuvaavat kappaleita, painotuksia, lukuja, liitteitä tai segmenttiä kokonaisuutena.

Seuraava taulukko näyttää Matroska-asiakirjan rakenteen, jossa useimmat elementit näytetään hierarkiassa:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML-otsikko | | | |
| Segmentti | SeekHead| Etsi | SeekID |
| | | | SeekPosition |
| | Tietoja | SegmentUID | |
| | | SegmentFilename | |
| | | Edellinen | |
| | | EdellinenTiedostonimi | |
| | | NextUID | |
| | | SeuraavaTiedostonnimi | |
| | | SegmentFamily | |
| | | LukuKäännä | |
| | | TimestampScale | |
| | | Kesto | |
| | | PäivämääräUTC | |
| | | Otsikko | |
| | | MuxingApp | |
| | | WritingApp | |
| | Kappaleet | TrackEntry | TrackNumber |
| | | | TrackUID |
| | | | TrackType |
| | | | Nimi |
| | | | Kieli |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Video | Lippulomitettu |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | DisplayWidth |
| | | | | DisplayHeight |
| | | | | AspectRatioType |
| | | | | Väri |
| | | | Ääni | Näytteenottotaajuus |
| | | | | Kanavat |
| | | | | BitDepth |
| | Luvut | EditionEntry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | ChapterAtom | ChapterUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | LukuAikaLoppu |
| | | | | LukuLippuPiilotettu |
| | | | | LukuNäyttö | ChapString |
| | | | | | ChapLanguage |
| | Klusteri | Aikaleima |
| | | SilentTracks |
| | | Asema |
| | | EdellinenSize |
| | | SimpleBlock |
| | | BlockGroup |
| | | EncryptedBlock |
| | Vihjeitä | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Liitteet | Liitetiedosto | Tiedoston kuvaus |
| | | | Tiedostonimi |
| | | | FileMimeType |
| | | | FileUID |
| | | | Tiedostoviittaus |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Tunnisteet | Tag | Tavoitteet | TargetTypeValue |
| | | | | Kohdetyyppi |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | TagName |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBinary |
| | | | | SimpleTag |


### koodekkien käyttö ###

Jos et halua uutta mediasoitinta ja käytät mieluummin olemassa olevaa soitinta, sinun on asennettava joitain koodekkeja (lyhenne pakkausta/purkua varten). Vaikka koodekkien lataaminen on kelvollinen vaihtoehto, sinun tulee olla varovainen lähteen suhteen, sillä ne voivat sisältää haittaohjelmia.

## Viitteet ##

- {{HYPERLINKKI1}}

