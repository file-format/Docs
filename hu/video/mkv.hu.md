{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKV fájlformátum",
  "keywords" :[ "mkv", "matroska video", "mkv format", "how to play mkv files", "video", "file", "format" ],
  "description":"További információ az MKV fájlformátumról és az MKV-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Mi az MKV fájl? ##

Az MKV (Matroska Video) a [MOV](/hu/video/mov/) és [AVI](/hu/video/avi/) formátumhoz hasonló multimédiás tároló, de több hang- és feliratsávot is támogat ugyanabban a fájlban. Az MKV-fájl a videóhoz használt Matroska multimédiás tároló formátum. Az MKV az Extensible Binary Meta Language-n alapul, és számos videó- és hangtömörítési formátumot támogat. A fő különbség az MKV és más videoformátumok között az, hogy az MKV egy konténer, nem pedig kodek. Az MKV fájlok mentése .mkv fájlkiterjesztéssel történik. Az MKV hangot, videót és feliratokat egyetlen fájlba foglalhat, még akkor is, ha ezek az elemek különböző típusú kódolást használnak. Például rendelkezhet egy MKV-fájllal, amely H.264-es videót és MP3- vagy AAC-fájlt tartalmaz hanghoz. Az MKV támogatja a leírásokat, az értékeléseket, a borítót és még a fejezetpontokat is. Az MKV számos kulcsfontosságú funkciója a jövő számára is megfelelő. Ezek a funkciók a következők:

- Gyorskeresés támogatása.
- Különböző audio- és videofolyamok kiválasztásának lehetősége.
- Feliratok támogatása (kemény és lágy kódolású).
- Metaadatok, fejezetek és menük támogatása.
- Online streamelési lehetőség.
- Képes helyreállítani a hibás fájlokat, amelyek lehetővé teszik a sérült fájlok lejátszását.

## Rövid története ##

Az MKV fájl 2002-ben származik Oroszországból. A vezető fejlesztő Lasse Kärkkäinen volt, aki a Matroska alapítójával, Steve Lhomme-mal és egy programozócsapattal dolgozott együtt. Az MKV-t nyílt szabványú projektként fejlesztették ki, ami azt jelenti, hogy nyílt forráskódú és ingyenesen használható. Az idő előrehaladtával a formátum javult, és 2010-ben a WebM multimédiás formátum alapja lett.

## Matroska Design ##

Matroska a következő megszorításokkal egészíti ki az EBML specifikációt.

- Az **EBML-fejléc** **docType**-jának „matroska”-nak kell lennie.
- Az **EBML fejléc** **EBMLMaxIDLength** értékének 4-nek kell lennie.
- Az **EBML fejléc** **EBMLMaxSizeLength** értékének 1 és 8 között kell lennie (beleértve).

Az összes legfelső szintű elem 4 oktettben van kódolva.

- Nyelvkódok: A Matroska (1-3 verzió) nyelvi kódokat használt, amelyek lehetnek a 3 betűs bibliográfiai ISO-639-2 formák (például "fre" a franciához), vagy további országkódok is használhatók, például "fre-ca" " a kanadai franciák számára. A Matroska 4-es verziójától kezdve az ISO 639-2 vagy a BCP 47 használható nyelvi kódokhoz, bár a BCP 47 ajánlott.
- Fizikai típusok: Ezek eltérő jelentéssel bírnak mind az audio-, mind a videófájlok esetében. Például a ChapterPhysicalEquiv = 60 jelentése (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) a hanghoz és (DVD / VHS / LASERDISC) a videóhoz.
- Blokkstruktúra - Blokkfejléc: A blokkfejléc információkat tartalmaz a műsorszám számáról, az időbélyegekről, a fűzés típusáról stb.
- Befűzés: Ez egy olyan mechanizmus, amely helytakarékos adattároláskor, amelyet általában kis adattömbökhöz (kockákhoz) használnak. 3 fajta fűzés létezik:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock szerkezet: A **Block szerkezet** ihlette, a fő különbség a **Keyframe** és **Elvethető** jelzők hozzáadása. Ezen kívül minden ugyanaz.

## Matroska szerkezet ##

A Matroska dokumentumnak legalább egy **EBML dokumentumból** kell állnia a **Matroska dokumentumtípus** használatával. Minden **EBML-dokumentumnak** egy **EBML-fejléccel** kell kezdődnie, amelyet a szegmensként meghatározott **EBML-gyökérelem** követ. A Matroska több legfelső szintű elemet határoz meg, amelyek a **szegmensben** előfordulhatnak.

Az EBML elemrendszert használ az EBML-dokumentum összeállításához. A következő a Matroska fájl legfelső szintű elemeinek listája:

- **EBML dokumentum**: a teljes fájl burkolója.
- **EBML-fejléc**: A fájl fejléc-információit tartalmazza, például a DocType-ot.
- **Szegmens**: A legfelső elem, amely az összes többi legfelső szintű elemet tartalmazza.
- **SeekHead**: Más felső szintű elemek szegmenseinek helyzetét tartalmazza.
- **Információ**: Általános információkat tartalmaz a szegmensről.
- **Tracks**: Az információ legfelső szintű eleme, sok leírt zeneszámmal.
- **Fejezetek**: Alapvető menük és partícióadatok meghatározására szolgál.
- **Cluster**: A blokkstruktúrát tartalmazó legfelső szintű elem.
- **Cues**: Legfelső szintű elem, amely tartalmazza a szegmens összes helyi bejegyzését, amely gyors hozzáférést keres.
- **Mellékletek**: Csatolt fájlokat tartalmaz.
- **Címkék**: Ez az elem metaadatokat tartalmaz, amelyek leírják a számokat, kiadásokat, fejezeteket, mellékleteket vagy a szegmens egészét.

A következő táblázat a Matroska-dokumentum szerkezetét mutatja, a legtöbb elem hierarchiában jelenik meg:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML fejléc | | | |
| Szegmens | SeekHead| Keress | SeekID |
| | | | SeekPosition |
| | Info | SegmentUID | |
| | | SzegmensFájlnév | |
| | | PrevUID | |
| | | Előzőfájlnév | |
| | | NextUID | |
| | | KövetkezőFájlnév | |
| | | SegmentFamily | |
| | | fejezetFordítás | |
| | | TimestampScale | |
| | | Időtartam | |
| | | DátumUTC | |
| | | Cím | |
| | | MuxingApp | |
| | | WritingApp | |
| | Pályák | TrackEntry | TrackNumber |
| | | | TrackUID |
| | | | TrackType |
| | | | Név |
| | | | Nyelv |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Videó | FlagInterlaced |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | DisplayWidth |
| | | | | DisplayHeight |
| | | | | Aspect RatioType |
| | | | | Szín |
| | | | Audio | Mintavételi Frekvencia |
| | | | | Csatornák |
| | | | | BitDepth |
| | Fejezetek | EditionEntry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | fejezetAtom | ChapterUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | ChapterFlagHidden |
| | | | | fejezetMegjelenítés | ChapString |
| | | | | | ChapLanguage |
| | Klaszter | Időbélyeg |
| | | SilentTracks |
| | | Pozíció |
| | | PrevSize |
| | | SimpleBlock |
| | | BlockGroup |
| | | EncryptedBlock |
| | Jelzések | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Mellékletek | AttachedFile | FileDescription |
| | | | Fájlnév |
| | | | FileMimeType |
| | | | FileUID |
| | | | FileReferral |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Címkék | Címke | Célok | TargetTypeValue |
| | | | | TargetType |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | Címkenév |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBinary |
| | | | | SimpleTag |


### Kodekek használata ###

Ha nem szeretne új médialejátszót, és inkább a meglévő lejátszóját szeretné használni, telepítenie kell néhány kodeket (a tömörítés/kitömörítés rövidítése). Annak ellenére, hogy a kodekek letöltése egy érvényes lehetőség, ügyeljen a forrásra, mivel ezek rosszindulatú programokat tartalmazhatnak.

## Referenciák ##

- [Matroska a Wikipedia által](https://en.wikipedia.org/wiki/Matroska)

