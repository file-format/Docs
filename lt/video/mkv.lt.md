{
  "date": "2019-10-11",
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "title": "MKV failo formatas",
  "keywords": [
"mkv",
"matroskos vaizdo įrašas",
"mkv formatu",
"kaip paleisti mkv failus",
"vaizdo įrašą",
"failą",
"formatu"
],
  "description": "Sužinokite apie MKV failo formatą ir API, kurios gali kurti ir atidaryti MKV failus.",
  "linktitle": "MKV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-ltv"
}
},
  "lastmod": "2020-17-11"
}


## Kas yra MKV failas? ##

MKV (Matroska Video) is a multimedia container similar to [MOV](/video/mov/) and [AVI](/video/avi/) format but it supports more than one audio and subtitle track in the same file. An MKV file is the Matroska multimedia container format used for video. MKV is based on Extensible Binary Meta Language and it supports several video and audio compression formats. The major difference between MKV and other video formats is that MKV is a container and not a codec. MKV files are saved with the .mkv file extension. MKV can incorporate audio, video, and subtitles in a single file even if those elements use different types of encoding. For example, you could have an MKV file that contains H.264 video and MP3 or AAC for audio. MKV also supports descriptions, ratings, cover art, and even chapter points. There are several key features that MKV is future-proof. These features include:

- Pagalba greitai ieškantiems.
- Galimybė pasirinkti skirtingus garso ir vaizdo srautus.
- Subtitrų palaikymas (užkoduoti ir minkšti).
- Metaduomenų, skyrių ir meniu palaikymas.
- Galimybė transliuoti internetu.
- Galimybė atkurti klaidingus failus, kurie suteikia galimybę atkurti sugadintus failus.

## Trumpa istorija ##

MKV failas atsirado 2002 m. Rusijoje. Pagrindinis kūrėjas buvo Lasse Kärkkäinen, dirbęs su Matroska įkūrėju Steve'u Lhomme'u ir programuotojų komanda. MKV buvo sukurtas kaip atvirų standartų projektas, o tai reiškia, kad jis yra atvirojo kodo ir juo galima nemokamai naudotis. Laikui bėgant formatas buvo tobulinamas ir 2010 m. tapo WebM daugialypės terpės formato pagrindu.

## Matroska dizainas ##

Matroska prideda šiuos apribojimus prie EBML specifikacijos.

– **EBML antraštės** **docType** turi būti matroska.
– **EBML antraštės** **EBMLMaxIDLength** turi būti 4.
– **EBML antraštės** **EBMLMaxSizeLength** turi būti nuo 1 iki 8 (imtinai).

Visi aukščiausio lygio elementai koduojami 4 oktetais.

– Kalbų kodai: Matroska (1–3 versijos) naudojo kalbų kodus, kurie gali būti 3 raidžių bibliografinė ISO-639-2 forma (pvz., Fre prancūzų kalba), arba gali būti naudojamas papildomas šalies kodas, pvz., fre-ca.  Kanados prancūzams. Nuo 4 versijos Matroska kalbos kodams GALI būti naudojamas ISO 639-2 arba BCP 47, nors rekomenduojamas BCP 47.
- Fiziniai tipai: jie turi skirtingą reikšmę tiek garso, tiek vaizdo failams. Pavyzdžiui, ChapterPhysicalEquiv = 60 reiškia (CD / 12 / 10 / 7 / TAPE / MINIDISC / DAT) garsui ir (DVD / VHS / LASERDISC) vaizdo įrašui.
- Bloko struktūra - Bloko antraštė: bloko antraštėje yra informacija apie takelio numerį, laiko žymes, surišimo tipą ir kt.
- Suvarstymas: tai mechanizmas, leidžiantis sutaupyti vietos, kai saugomi duomenys, kurie paprastai naudojami mažiems duomenų blokams (kadrams). Yra 3 raištelių tipai:
  - "Xiph: rėmelis, kurio dydžio kartotinis yra 255, užkoduotas 0 dydžio pabaigoje. Pavyzdžiui, 765 kodas yra 255;255;255;0."
  - "EBML: rėmelio dydis užkoduotas kaip skirtumas tarp ankstesnio dydžio ir šio dydžio. Pirmasis nėrinių dydis yra be ženklų, bet kiti naudoja diapazono poslinkį, kad gautų ženklą ant kiekvienos vertės."
  - "fiksuotas dydis: dydis išlieka toks pat."
- Paprasta bloko struktūra: ją įkvėpė **Blokų struktūra**, o pagrindinis skirtumas yra **Keyframe** ir **Discardable** vėliavėlių pridėjimas. Išskyrus tai, viskas yra taip pat.

## Matroska struktūra ##

Matroska dokumentą turi sudaryti bent vienas **EBML dokumentas**, naudojant **Matroska dokumento tipą**. Kiekvienas **EBML dokumentas** turi prasidėti **EBML antrašte**, po kurios seka **EBML šakninis elementas**, kuris apibrėžiamas kaip segmentas. Matroska apibrėžia kelis aukščiausio lygio elementus, kurie gali atsirasti **segmente**.

EBML naudoja elementų sistemą, kad sudarytų EBML dokumentą. Toliau pateikiamas aukščiausio lygio elementų sąrašas Matroska faile:

- **EBML dokumentas**: viso failo įvynioklis.
- **EBML antraštė**: joje yra failo, pvz., DocType, antraštės informacija.
– **Segmentas**: viršutinis elementas, kuriame yra visi kiti aukščiausio lygio elementai.
- **SeekHead**: joje yra kitų aukščiausio lygio elementų segmentų padėtis.
- **Informacija**: joje pateikiama bendra informacija apie segmentą.
- **Tracks**: aukščiausio lygio informacijos elementas su daugybe aprašytų takelių.
- **Chapters**: It is used to define basic menus and partition data.
- **Cluster**: aukščiausio lygio elementas, kuriame yra bloko struktūra.
- **Cues**: aukščiausio lygio elementas, kuriame yra visi segmente esantys įrašai, kurių greitis siekia pasiekti.
- **Priedai**: yra pridedamų failų.
– **Žymos**: šiame elemente yra metaduomenų, apibūdinančių takelius, leidimus, skyrius, priedus arba visą segmentą.

Šioje lentelėje parodyta Matroska dokumento struktūra su dauguma elementų, rodomų hierarchijoje:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML antraštė | | | |
| Segmentas | SeekHead| Ieškok | SeekID |
| | | | SeekPosition |
| | Informacija | SegmentUID | |
| | | SegmentFilename | |
| | | AnkstesnisUID | |
| | | Ankstesnis failo pavadinimas | |
| | | KitasUID | |
| | | KitasFailo pavadinimas | |
| | | SegmentFamily | |
| | | SkyriusVersti | |
| | | TimestampScale | |
| | | Trukmė | |
| | | DataUTC | |
| | | Pavadinimas | |
| | | MuxingApp | |
| | | WritingApp | |
| | Takeliai | TrackEntry | TrackNumber |
| | | | TrackUID |
| | | | TrackType |
| | | | Vardas |
| | | | Kalba |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Vaizdo įrašas | FlagInterlaced |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | DisplayWidth |
| | | | | Ekrano aukštis |
| | | | | AspectRatioType |
| | | | | Spalva |
| | | | Garsas | Mėginių ėmimo dažnis |
| | | | | Kanalai |
| | | | | BitDepth |
| | Skyriai | EditionEntry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | SkyriusAtom | SkyriusUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | SkyriusLaikasPabaiga |
| | | | | SkyriusVėliavaPaslėptas |
| | | | | SkyriusEkranas | ChapString |
| | | | | | ChapLanguage |
| | Klasteris | Laiko žyma |
| | | SilentTracks |
| | | Padėtis |
| | | Ankstesnis dydis |
| | | SimpleBlock |
| | | BlockGroup |
| | | EncryptedBlock |
| | Užuominos | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Priedai | AttachedFile | Failo aprašymas |
| | | | Failo pavadinimas |
| | | | FileMimeType |
| | | | FileUID |
| | | | FileReferral |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Žymos | Žyma | Tikslai | TargetTypeValue |
| | | | | TargetType |
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


### Kodekų naudojimas ###

Jei nenorite naujo daugialypės terpės grotuvo ir norite naudoti esamą grotuvą, turėsite įdiegti keletą kodekų (suglaudinimo / išskleidimo trumpinys). Nors kodekų atsisiuntimas yra tinkamas pasirinkimas, turėtumėte būti atsargūs dėl šaltinio, nes juose gali būti kenkėjiškų programų.

## Nuorodos Nr.

- [Matroska by Wikipedia](https://en.wikipedia.org/wiki/Matroska)

