{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru MKV",
  "keywords" :[ "mkv", "matroska video", "formát mkv", "jak přehrávat soubory mkv", "video", "soubor", "formát" ],
  "description":"Další informace o formátu souboru MKV a rozhraních API, která mohou vytvářet a otevírat soubory MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Co je soubor MKV? ##

MKV (Matroska Video) je multimediální kontejner podobný formátu [MOV](/cs/video/mov/) a [AVI](/cs/video/avi/), ale podporuje více než jednu stopu zvuku a titulků ve stejném souboru. Soubor MKV je formát multimediálního kontejneru Matroska používaný pro video. MKV je založen na Extensible Binary Meta Language a podporuje několik formátů komprese videa a zvuku. Hlavní rozdíl mezi MKV a jinými video formáty je ten, že MKV je kontejner a ne kodek. Soubory MKV se ukládají s příponou .mkv. MKV může začlenit zvuk, video a titulky do jednoho souboru, i když tyto prvky používají různé typy kódování. Můžete mít například soubor MKV, který obsahuje video H.264 a zvuk ve formátu MP3 nebo AAC. MKV také podporuje popisy, hodnocení, přebaly a dokonce i body kapitol. Existuje několik klíčových funkcí, díky kterým je MKV připraveno na budoucnost. Mezi tyto funkce patří:

- Podpora rychlého hledání.
- Schopnost vybrat různé audio a video streamy.
- Podpora pro titulky (pevně kódované a softwarově kódované).
- Podpora pro metadata, kapitoly a nabídky.
- Možnost streamovat online.
- Schopnost obnovit chybné soubory, které poskytují možnost přehrávání poškozených souborů.

## Stručná historie ##

Soubor MKV vznikl v roce 2002 v Rusku. Hlavním vývojářem byl Lasse Kärkkäinen, který spolupracoval se zakladatelem Matrosky Stevem Lhommem a týmem programátorů. MKV byl vyvinut jako projekt otevřených standardů, což znamená, že je open source a je zdarma k použití. Postupem času byl formát vylepšen a v roce 2010 se stal základem multimediálního formátu WebM.

## Design Matroska ##

Matroska přidává do specifikace EBML následující omezení.

- **docType** **EBML Header** musí být 'matroska'.
- **EBMLMaxIDLength** **EBML Header** musí být 4.
- **EBMLMaxSizeLength** **EBML Header** musí být mezi 1 a 8 (včetně).

Všechny prvky nejvyšší úrovně jsou kódovány ve 4 oktetech.

- Jazykové kódy: Matroska (verze 1 až 3) používala jazykové kódy, které mohou mít buď 3písmennou bibliografickou formu ISO-639-2 (jako "fre" pro francouzštinu), nebo mohl být použit další kód země jako "fre-ca" “ pro kanadskou francouzštinu. Počínaje verzí Matroska 4 MŮŽE být pro jazykové kódy použit buď ISO 639-2 nebo BCP 47, ačkoli se doporučuje BCP 47.
- Fyzické typy: Tyto typy mají různý význam pro audio i video soubory. Například ChapterPhysicalEquiv = 60 znamená (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) pro zvuk a (DVD / VHS / LASERDISC) pro video.
- Struktura bloku - Záhlaví bloku: Záhlaví bloku obsahuje informace týkající se čísla stopy, časových razítek, typu šněrování atd.
- Šněrování: Jedná se o mechanismus pro úsporu místa při ukládání dat, který se obvykle používá pro malé bloky dat (rámce). Existují 3 typy šněrování:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- Struktura SimpleBlock: Je inspirována **Strukturou bloku** s hlavním rozdílem v přidání příznaků **Keyframe** a **Discardable**. Kromě toho je vše při starém.

## Matroska struktura ##

Dokument Matroska musí být složen alespoň z jednoho **Dokumentu EBML** s použitím **Typu dokumentu Matroska**. Každý **dokument EBML** musí začínat **záhlavím EBML** následovaným **kořenovým prvkem EBML**, který je definován jako segment. Matroska definuje několik prvků nejvyšší úrovně, které se mohou vyskytovat v rámci **Segmentu**.

EBML používá k sestavení dokumentu EBML systém prvků. Níže je uveden seznam prvků nejvyšší úrovně v souboru Matroska:

- **Dokument EBML**: Obálka pro celý soubor.
- **Záhlaví EBML**: Obsahuje informace o záhlaví souboru, jako je DocType.
- **Segment**: Nejvyšší prvek, který obsahuje všechny ostatní prvky nejvyšší úrovně.
- **SeekHead**: Obsahuje pozici segmentů ostatních prvků nejvyšší úrovně.
- **Info**: Obsahuje obecné informace o segmentu.
- **Stopy**: Prvek informací nejvyšší úrovně s mnoha popsanými skladbami.
- **Kapitoly**: Používá se k definování základních nabídek a dat oddílů.
- **Cluster**: Prvek nejvyšší úrovně obsahující strukturu bloku.
- **Narážky**: Prvek nejvyšší úrovně, který obsahuje všechny místní položky segmentu, které urychlují hledání přístupu.
- **Přílohy**: Obsahuje přiložené soubory.
- **Tags**: Tento prvek obsahuje metadata popisující stopy, edice, kapitoly, přílohy nebo segment jako celek.

Následující tabulka ukazuje strukturu dokumentu Matroska s většinou prvků zobrazených v hierarchii:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Hlavička EBML | | | |
| Segment | SeekHead| Hledat | SeekID |
| | | | SeekPosition |
| | Informace | SegmentUID | |
| | | SegmentFilename | |
| | | PrevUID | |
| | | Předchozí název_souboru | |
| | | DalšíUID | |
| | | DalšíNázevSouboru | |
| | | SegmentRodina | |
| | | KapitolaTranslate | |
| | | Měřítko časového razítka | |
| | | Doba trvání | |
| | | DatumUTC | |
| | | Název | |
| | | MuxingApp | |
| | | Aplikace pro psaní | |
| | Skladby | TrackEntry | TrackNumber |
| | | | TrackUID |
| | | | TrackType |
| | | | Jméno |
| | | | Jazyk |
| | | | CodecID |
| | | | CodecPrivate |
| | | | Název kodeku |
| | | | Video | FlagInterlaced |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | Výška pixelu |
| | | | | DisplayWidth |
| | | | | DisplayHeight |
| | | | | AspectRatioType |
| | | | | Barva |
| | | | Audio | Vzorkovací frekvence |
| | | | | Kanály |
| | | | | BitDepth |
| | Kapitoly | EditionEntry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | KapitolaAtom | ChapterUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | KapitolaČasKonec |
| | | | | ChapterFlagHidden |
| | | | | Zobrazení kapitoly | ChapString |
| | | | | | ChapLanguage |
| | Cluster | Časové razítko |
| | | SilentTracks |
| | | Pozice |
| | | Předchozí Velikost |
| | | SimpleBlock |
| | | BlockGroup |
| | | EncryptedBlock |
| | Narážky | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Přílohy | AttachedFile | Popis souboru |
| | | | Název souboru |
| | | | FileMimeType |
| | | | FileUID |
| | | | Referenční soubor |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Štítky | Štítek | Cíle | TargetTypeValue |
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


### Používání kodeků ###

Pokud nechcete nový přehrávač médií a dáváte přednost použití stávajícího přehrávače, budete muset nainstalovat některé kodeky (zkratka pro kompresi/dekompresi). I když je stahování kodeků platnou možností, měli byste si dávat pozor na zdroj a ty mohou obsahovat malware.

## Reference ##

- [Matroska od Wikipedie](https://en.wikipedia.org/wiki/Matroska)

