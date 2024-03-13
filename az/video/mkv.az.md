{
  "date": "2019-10-11",
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "title": "MKV fayl formatı",
  "keywords": [
"mkv",
"matroska video",
"mkv formatı",
"mkv fayllarını necə oynamaq olar",
"video",
"fayl",
"format"
],
  "description": "MKV fayl formatı və MKV faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MKV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-azv"
}
},
  "lastmod": "2020-17-11"
}


## MKV faylı nədir? ##

MKV (Matroska Video) is a multimedia container similar to [MOV](/video/mov/) and [AVI](/video/avi/) format but it supports more than one audio and subtitle track in the same file. An MKV file is the Matroska multimedia container format used for video. MKV is based on Extensible Binary Meta Language and it supports several video and audio compression formats. The major difference between MKV and other video formats is that MKV is a container and not a codec. MKV files are saved with the .mkv file extension. MKV can incorporate audio, video, and subtitles in a single file even if those elements use different types of encoding. For example, you could have an MKV file that contains H.264 video and MP3 or AAC for audio. MKV also supports descriptions, ratings, cover art, and even chapter points. There are several key features that MKV is future-proof. These features include:

- Sürətli axtarışa dəstək.
- Müxtəlif audio və video axınlarını seçmək imkanı.
- Altyazılar üçün dəstək (sərt kodlu və yumşaq kodlu).
- Metadata, fəsillər və menyular üçün dəstək.
- Onlayn yayım imkanı.
- Zədələnmiş faylları oynatmaq imkanı verən səhv faylları bərpa etmək imkanı.

## Qısa tarix ##

MKV faylı 2002-ci ildə Rusiyada yaranıb. Aparıcı tərtibatçı Matroska-nın qurucusu Stiv Lhomme və proqramçılar komandası ilə işləyən Lasse Kärkkäinen idi. MKV açıq standartlar layihəsi kimi hazırlanmışdır, yəni açıq mənbədir və istifadəsi pulsuzdur. Vaxt keçdikcə format təkmilləşdi və 2010-cu ildə WebM multimedia formatının əsasına çevrildi.

## Matroska Dizayn ##

Matroska EBML spesifikasiyasına aşağıdakı məhdudiyyətləri əlavə edir.

- **EBML Başlığı**-nın **docType** 'matroska' olmalıdır.
- **EBML Başlığı**-nın **EBMLMaxIDLength** 4 olmalıdır.
- **EBML Başlığı**-nın **EBMLMaxSizeLength** 1 və 8 (daxil olmaqla) arasında olmalıdır.

Bütün yuxarı səviyyəli elementlər 4 oktetdə kodlanır.

- Dil kodları: Matroska (versiya 1-dən 3-ə qədər) 3 hərfli biblioqrafik ISO-639-2 forması (fransızca üçün fre kimi) və ya fre-ca kimi əlavə ölkə kodu ola bilən dil kodlarından istifadə olunur. Kanada Fransız dili üçün. Matroska 47 versiyasından başlayaraq dil kodları üçün ISO 639-2 və ya BCP 47 istifadə oluna bilər, baxmayaraq ki, BCP 47 tövsiyə olunur.
- Fiziki Növlər: Bunlar həm audio, həm də video faylları üçün fərqli məna daşıyır. Məsələn, ChapterPhysicalEquiv = 60 audio üçün (CD / 12 / 10 / 7 / TAPE / MINIDISC / DAT) və video üçün (DVD / VHS / LASERDISC) deməkdir.
- Blok strukturu - Blok başlığı: Blok başlığında trek nömrəsi, vaxt ştampları, bağlama növü və s. ilə bağlı məlumatlar var.
- Bağlama: Bu, adətən kiçik məlumat blokları (çərçivələri) üçün istifadə olunan məlumatları saxlayarkən yerə qənaət etmək mexanizmidir. 3 növ bağlama var:
  - "Xiph: Ölçüsü 255-dən çox olan çərçivə ölçüsünün sonunda 0 ilə kodlanır. Məsələn, 765 kodu 255;255;255;0-dır."
  - "EBML: Çərçivə ölçüsü əvvəlki ölçü ilə bu ölçü arasındakı fərq kimi kodlanır. Krujevadakı ilk ölçü imzasızdır, lakin digərləri hər bir dəyərdə işarə almaq üçün diapazondan istifadə edirlər."
  - "sabit ölçülü: Ölçü eyni qalır."
- SimpleBlock Structure: O, **Blok strukturundan** ilhamlanıb, əsas fərq **Keyframe** və **Discardable** bayraqlarının əlavə edilməsidir. Bundan başqa, hər şey eynidir.

## Matroska strukturu ##

Matroska sənədi **Matroska Sənəd Növü** istifadə edərək ən azı bir **EBML Sənədindən** ibarət olmalıdır. Hər bir **EBML Sənədi** **EBML Başlığı** ilə başlamalıdır, ardınca Seqment kimi müəyyən edilən **EBML Kök Elementi** olmalıdır. Matroska **Seqment** daxilində baş verə biləcək bir neçə Yüksək Səviyyəli Elementləri müəyyən edir.

EBML EBML Sənədini tərtib etmək üçün Elementlər sistemindən istifadə edir, Aşağıdakılar Matroska faylındakı Üst Səviyyə elementlərinin siyahısıdır:

- **EBML Sənədi**: Bütün fayl üçün sarğı.
- **EBML Başlığı**: O, DocType kimi fayl üçün başlıq məlumatını ehtiva edir.
- **Seqment**: Bütün digər yüksək səviyyəli elementləri ehtiva edən üst element.
- **SeekHead**: O, digər Yüksək Səviyyəli Elementlərin Seqmentlərinin mövqeyini ehtiva edir.
- **Məlumat**: Seqment haqqında ümumi məlumatı ehtiva edir.
- **Tracks**: Çoxlu trekləri təsvir edən yüksək səviyyəli məlumat elementi.
- **Chapters**: It is used to define basic menus and partition data.
- **Klaster**: Blok strukturunu ehtiva edən Üst Səviyyə Elementi.
- **İstiqamətlər**: Girişi sürətləndirən Seqmentə aid bütün qeydləri ehtiva edən Yüksək Səviyyəli Element.
- **Qoşmalar**: Bura əlavə edilmiş fayllar daxildir.
- **Teqlər**: Bu elementdə Tracks, Nəşrlər, Fəsillər, Qoşmalar və ya bütövlükdə Seqmenti təsvir edən metadata var.

Aşağıdakı cədvəldə iyerarxiyada göstərilən elementlərin əksəriyyəti ilə Matroska sənədinin strukturu göstərilir:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML Başlığı | | | |
| Seqment | SeekHead| Axtar | SeekID |
| | | | SeekPosition |
| | Məlumat | SegmentUID | |
| | | SegmentFilename | |
| | | ƏvvəlkiUID | |
| | | Əvvəlki Fayl adı | |
| | | NextUID | |
| | | NextFayl adı | |
| | | SegmentAilə | |
| | | ChapterTranslate | |
| | | TimestampScale | |
| | | Müddət | |
| | | DateUTC | |
| | | Başlıq | |
| | | MuxingApp | |
| | | WritingApp | |
| | Tracks | TrackEntry | TrackNömrə |
| | | | TrackUID |
| | | | TrackType |
| | | | Adı |
| | | | Dil |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Video | FlagInterlaced |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | DisplayWidth |
| | | | | DisplayHeight |
| | | | | AspectRatioType |
| | | | | Rəng |
| | | | Audio | Sampling Tezliyi |
| | | | | Kanallar |
| | | | | BitDepth |
| | Fəsillər | EditionEntry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | BuraxılışFlagOrdered |
| | | | ChapterAtom | ChapterUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | ChapterFlagHidden |
| | | | | BölümDisplay | ChapString |
| | | | | | ChapLanguage |
| | Klaster | Vaxt möhürü |
| | | SilentTracks |
| | | Vəzifə |
| | | ƏvvəlkiÖlçü |
| | | SimpleBlock |
| | | Blok Qrupu |
| | | EncryptedBlock |
| | Istekalar | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Qoşmalar | AttachedFile | Fayl təsviri |
| | | | Fayl adı |
| | | | FileMimeType |
| | | | FileUID |
| | | | FileReferral |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Teqlər | Tag | Hədəflər | TargetTypeValue |
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


### Kodeklərdən istifadə ###

Əgər siz yeni media pleyerini istəmirsinizsə və mövcud pleyerinizdən istifadə etməyi üstün tutursunuzsa, bəzi kodekləri (sıxılma/dekompressiya üçün qısa) quraşdırmalı olacaqsınız. Kodekləri yükləmək düzgün seçim olsa da, mənbəyə diqqətli olmalısınız və bunlarda zərərli proqram ola bilər.

## İstinadlar ##

- [Matroska by Wikipedia](https://en.wikipedia.org/wiki/Matroska)

