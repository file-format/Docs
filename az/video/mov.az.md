{
  "date": "2019-10-11",
  "keywords": [
"mov faylı",
"mov fayl formatı",
"mov faylı nədir",
"fayl",
"mov nümunəsi",
"mov fayl uzantısı",
"uzadılması",
"format",
"Tez vaxt",
"MPEG-4"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MOV Faylı - Apple QuickTime Film Fayl Formatıdır",
  "description": "MOV fayl formatı və MOV faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MOV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mo-azv"
}
},
  "lastmod": "2021-07-29"
}

## MOV faylı nədir?

MOV faylı Apple Inc. tərəfindən hazırlanmış, bir və ya daha çox trekdən ibarət video fayl növüdür. Hər bir trek bir film, audio, film klipləri və subtitrləri saxlayır. Bu, müxtəlif növ media elementlərini saxlaya bilən multimedia konteyneridir. MOV video formatı həm Windows, həm də Macintosh sistemləri ilə uyğun gəlir. O, sıxılma üçün kodlanmış MPEG-4 istifadə edir və izlər iyerarxik məlumat strukturunda yerləşdirilən atomlar adlanan obyektlərdə saxlanılır.

## MOV Fayl Formatının Qısa Tarixi

MPEG-4 file format has evolved from QuickTime File Format (**QTFF**) specification in 2001. Beynəlxalq Standartlaşdırma Təşkilatı formatı təsdiqlədi və MPEG-4 Part 1 sistem spesifikasiyası 1999-cu ildə nəşr olundu. 2001-ci ildə [MP4](/video/mp4/) revizyon fayl formatı nəşr olundu.

MP4-ün ilk versiyası 2003-cü ildə MPEG-4 Part 14 (ISO/IEC 14496-14:2003) kimi yenidən işlənmişdir. 2004-cü ildə MP4 bütün zamana əsaslanan media faylları üçün ümumi strukturu müəyyən etmək üçün ümumiləşdirilmişdir. Buna görə də, indi müxtəlif digər multimedia fayl formatları üçün əsas kimi istifadə olunur.

## QuickTime Fayl Format (QTFF) - Ətraflı Məlumat

Rəqəmsal multimedia ilə işləmək üçün QTFF bir çox məlumat növlərini saxlaya bilər. Rəqəmsal media mübadiləsi üçün ideya formatıdır, çünki format istənilən növ media strukturlarını təsvir etmək üçün standartları müəyyən edir. Fayl formatı obyekt yönümlü obyektlərin çevik kolleksiyasından ibarətdir. Filmlərin disklərdə saxlanması üçün QuickTime iki strukturdan istifadə edir, yəni atomlar” və QT atomları”.

### Atomlar

Atom QuickTime faylının əsas vahididir. İstənilən atomda hər hansı digər sahədən əvvəl iki əsas sahə var: Ölçü və Tip sahələri. Ölçü sahəsi atomun ölçüsünü, tip sahəsi isə atomda saxlanılan məlumatların növünü göstərir. Təbiətinə görə, atomlar iyerarxikdir, yəni bir atom başqalarını ehtiva edə bilən digər atomları ehtiva edə bilər. Nümunə atomunun quruluşu aşağıdakı şəkildə göstərilmişdir.

Hər bir atom iki hissədən ibarətdir, başlıq” və məlumat”. Başlıq ölçü və tip sahələrini, məlumat hissəsində isə faktiki məlumatları ehtiva edir. Bundan əlavə, hər bir sahə aşağıda izah olunur:

### Atom Ölçüsü

Atomun başlığı və məzmunu atomun ölçüsü kimi tanınan 32 bitlik tam ədədlə göstərilir. Ölçü sahəsi 32 bitlik işarəsiz tam ədədlə ifadə olunan baytlarda atomun ölçüsünü ehtiva edir.

### Atom növü

Atomun növü həmçinin 32 bitlik tam ədədlə göstərilir və bu, əsasən knemonik dəyəri olan dörd simvollu sahə kimi qəbul edilir, məsələn, film atomu üçün moov (0x6D6F6F76) və ya trak (0x7472616B) üçün iz atomu. Atom növü məlum olduqdan sonra onun məlumatlarını şərh etməyə imkan verir.

### QT Atomları və Atom Konteynerləri

QT atomları ümumi təyinatlı saxlama formatını təmin edir və Ölçü, Növ, Atom ID və Uşaq atomlarının sayı sahələrindən ibarət genişləndirilmiş başlığa malikdir. QT atomları bir atom konteynerinə bükülür, kilid sayına malik bir başlığa malik unikal məlumat strukturu. Hər atom konteynerində QT atomu olan bir kök atom var. QT atomunun quruluşu aşağıdakı şəkildə göstərilmişdir.

QT atom konteynerinin başlığında aşağıdakı məlumatlar var:

Qorunan: 0 dəyəri olan 10 baytlıq element.

Kilid sayı: 0 dəyəri olan 16 bitlik tam ədəd.

QT atom başlıqlarında aşağıdakı məlumatlar var:

**Ölçü -** QT atom başlığı və məzmunu baytlarda 32 bitlik tam ədədlə göstərilir. Bir yarpaq atomu vəziyyətində, bu sahə tək bir atomun ölçüsünü ehtiva edir.

**Tip -** Atomun növü 32 bitlik tam ədədlə göstərilir. Əgər kök atomdursa, dəyər 'sean' olaraq təyin olunur.

**Atom ID -** Bu, atom ID-sini göstərən 32 bitlik tam ədəddir və bütün qardaşlar üçün unikal olmalıdır. Kök atom həmişə atom identifikatorunun dəyərini 1 olaraq alır.

** Qorundu -** 0-a təyin edilməli olan 16 bitlik tam ədəd.

**Uşaqların sayı -** Atomun uşaq atomlarının sayını göstərən 16 bitlik tam ədəd.

** Qorundu -** 0-a təyin edilməli 32 bitlik tam ədəd.

## MOV fayllarının fayl strukturu

MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV qt olmalıdır alt tiplə müəyyən edilir. MOV faylını tərtib etmək üçün naməlum növ aşkarlanana qədər parçaları təkrarlamaq lazımdır.

Here is a `sample example`: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. 32 ofsetdə (onaltılıq: 20) ölçüsü 8 olan və **mdat** tipli (onaltılıq: 6D 64 61 74) olan ikinci hissə yerləşir.

Növbəti hissə 32+8#40 (hex: 28) ofsetində yerləşir və ölçüsü 3,263,028 (hex: 00 31 CA 34) və **mdat** (onaltılıq: 6D 64 61 74) ofset 44 (hex) yazır. : 2C). Növbəti hissə ofset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) və ölçüsü 21,189 (onaltılıq: 00 00 52 C5) və **moov** (hex: 6D 6F) offsetdə yerləşir. 1,836,019,574 (onaltılıq: 00 31 CA 60). Bu, sonuncu parçadır, ona görə də ümumi fayl ölçüsü 3,263,068+21,189#3,284,257 baytdır.

## MOV faylını necə çevirmək olar?

MOV fayllarını digər məşhur video fayl formatlarına çevirmək üçün çoxlu media pleyerləri və proqram video redaktorları mövcuddur. MOV fayllarını digər formatlara çevirə bilən bəzi media pleyerlərinə aşağıdakılar daxildir:

 * VideoLAN VLC media player
 * Eltima Elmedia Pleyeri

VideoLAN VLC media player və Eltima Elmedia Player daxil olmaqla bir neçə media pleyer və video redaktoru MOV fayllarını digər formatlara çevirə bilər. Bu proqramlar MOV fayllarını aşağıdakı video formatlarına çevirə bilər.

 * MPEG-4 Video - [MP4](/video/mp4/)
 * WebM Video - [WEBM](/video/webm/)
 * Video Nəqliyyat Yayımı - [TS](/video/ts/)
 * Qabaqcıl Sistemlər Format - [ASF](/video/ts/)
 * Ogg Vorbis Audio - [OGG](/audio/ogg/)
 * MP3 Audio - [MP3](/audio/mp3/)
 * Pulsuz Lossless Audio Codec - [FLAC](/audio/flac/)
 * WAVE Audio - [WAV](/audio/wav/)

## MOV faylları üçün açıq mənbə API

 * [MOV-u MP4-ə çevirmək üçün Native API-yə reaksiya verin](https://github.com/taltultc/react-native-mov-to-mp4)
 * [MOV fayllarını təmir etmək üçün Python API](https://github.com/nrosenstein-stuff/movrepair)
 * [MOV-ni GIF-ə çevirmək üçün Ruby API](https://github.com/skygroundmedia/convert-mov-to-gif)

## İstinadlar

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)


