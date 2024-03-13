{
  "date": "2021-02-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QT Fayl Format - Sürətli Film Faylı",
  "keywords": [
"QT",
"QuickTime video",
"qt formatı",
"qt fayllarını necə oynatmaq olar",
"Sürətli film faylı",
"QTFF",
"video",
"alma"
],
  "description": "QT faylları yarada və aça bilən QT fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "QT",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-q-azt"
}
},
  "lastmod": "2021-02-16"
}

## QT faylı nədir?

.qt uzantısı olan fayl, multimedia fayl məzmununu saxlamaq üçün QuickTime çərçivəsi tərəfindən istifadə edilən multimedia konteyner faylıdır. Apple Inc. tərəfindən hazırlanmış QuickTime Fayl Formatı (QTFF) sonradan oxutmaq üçün audio, video və ya mətni ehtiva edən multimedia konteyner faylıdır. Cihazlar, proqramlar və əməliyyat sistemləri arasında rəqəmsal media mübadiləsi üçün seçilən formatdır. QT faylları həmçinin Apple Inc tərəfindən hazırlanmış [MOV](/video/mov/) formatında saxlanılır. QT fayllarını aça bilən bəzi proqramlara Apple QuickTime pleyer, VLC media pleyer və K-Lite Codec Pack ilə Media Player Classic daxildir.

## QT fayl formatı

QTFF, təhlil və genişləndirmə asanlığı üçün çevik obyektlər toplusunu ifşa edən obyekt yönümlüdür. QT faylındakı hər bir trek rəqəmsal olaraq kodlanmış media axını və ya başqa faylda yerləşən media axınına məlumat istinadını ehtiva edir. Atom adlanan obyektlərdən ibarət iyerarxik məlumat strukturu iz konteynerləri kimi çıxış edir. [QT file format](https://developer.apple.com/documentation/quicktime-file-format) üçün fayl formatı spesifikasiyalar Apple Inc tərəfindən tərtibatçının istinadı üçün rəsmi olaraq mövcuddur.

### Media description

The media description of a QuickTime file is stored separately from the media data. Information such as the number of tracks, video compression format, and timing information is stored in the media description (also known as movie resource, movie atom, or simply the movie). The media data is referenced by an index in this media structure. The media data is the actual sample data, such as video frames and audio samples, used in the movie.

### Atomlar

Atom QuickTime faylının əsas vahididir. İstənilən atomda hər hansı digər sahədən əvvəl iki əsas sahə var: Ölçü və Tip sahələri. Ölçü sahəsi atomun ölçüsünü, tip sahəsi isə atomda saxlanılan məlumatların növünü göstərir. Təbiətinə görə, atomlar iyerarxikdir, yəni bir atom başqalarını ehtiva edə bilən digər atomları ehtiva edə bilər. Nümunə atomunun quruluşu aşağıdakı şəkildə göstərilmişdir.

Hər bir atom iki hissədən, başlıqdan və məlumatdan ibarətdir. Başlıq ölçü və tip sahələrini, məlumat hissəsində isə faktiki məlumatları ehtiva edir. Bundan əlavə, hər bir sahə aşağıda izah olunur:

#### Atom Ölçüsü

Atomun başlığı və məzmunu atomun ölçüsü kimi tanınan 32 bitlik tam ədədlə göstərilir. Ölçü sahəsi 32 bitlik işarəsiz tam ədədlə ifadə olunan baytlarda atomun ölçüsünü ehtiva edir.

#### Atom növü

Atomun növü həmçinin 32 bitlik tam ədədlə göstərilir və bu, əsasən knemonik dəyəri olan dörd simvollu sahə kimi qəbul edilir, məsələn, film atomu üçün moov (0x6D6F6F76) və ya trak (0x7472616B) üçün iz atomu. Atom növü məlum olduqdan sonra onun məlumatlarını şərh etməyə imkan verir.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Fayl strukturu ##

QT/MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV qt olmalıdır alt tiplə müəyyən edilir. MOV faylını tərtib etmək üçün naməlum növ aşkarlanana qədər parçaları təkrarlamaq lazımdır.

Here is a sample example: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. 32 ofsetdə (onaltılıq: 20) ölçüsü 8 olan və **mdat** tipli (onaltılıq: 6D 64 61 74) olan ikinci hissə yerləşir.

Növbəti hissə 32+8#40 (hex: 28) ofsetində yerləşir və ölçüsü 3,263,028 (hex: 00 31 CA 34) və **mdat** (hex: 6D 64 61 74) ofset 44 (hex) ilə yazın. : 2C). Növbəti hissə ofset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) və ölçüsü 21,189 (onaltılıq: 00 00 52 C5) və **moov** (hex: 6D 6F) offsetdə yerləşir. 1,836,019,574 (onaltılıq: 00 31 CA 60). Bu, sonuncu parçadır, ona görə də ümumi fayl ölçüsü 3,263,068+21,189#3,284,257 baytdır.

## İstinadlar ##

* [QT Fayl Format - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)

* [QuickTime Fayl Format - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)


