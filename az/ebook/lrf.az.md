{
  "date": "2019-12-12",
  "keywords": [
"LRF",
"fayl",
"uzadılması",
"format",
"elektron kitab",
"Rəqəmsal kitab"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "LRF faylları yarada və aça bilən LRF fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "LRF Fayl Format - Sony Portativ Reader Faylı",
  "linktitle": "LRF",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-lr-azf"
}
},
  "lastmod": "2019-12-12"
}

## LRF faylı nədir?

.lrf uzantısı olan fayl mətn, şəkillər və səhifələmə məlumatları daxil olmaqla, Sony BBeB üçün məlumatları ehtiva edən Geniş Zolaqlı elektron Kitab (BBeB) faylıdır. Fayl başlıq, müəyyən sayda obyekt və obyekt indeksindən ibarət sıxılmış ikili formatda saxlanılır. LRF və LRX faylları mövcud iki BBeB kitab formatını əhatə edir. LRF faylları şifrələnmir və [LRX](/ebook/lrf/) fayllarından tərtib edilə bilər. LRF faylları PDF və HTML daxil olmaqla bir neçə digər fayl növlərindən çevrilə bilər. Əgər kompüteriniz LRF faylını aça bilmirsə, yəqin ki, sizdə LRF fayllarını açmaq və ya redaktə etmək üçün quraşdırılmış proqram yoxdur. LRF fayllarını aça bilən proqramlar Windows üçün Calibre, BookDesigner, Makelrf və Canon Book Creator, Linux üçün Calibre, Calibre və Macintosh üçün Sony Reader-dir.

## Qısa tarix

LRF fayl növü ilk növbədə [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment) tərəfindən Line Rider ilə əlaqələndirilir. Line Rider internet fizika oyuncağıdır və 2006-cı ilin sentyabrında sloveniyalı universitet tələbəsi Boštjan Čadež tərəfindən icad edilmişdir. Sony brendi eBook e-Oxuyucuları (məsələn, Sony PRS-500 oxucuları və Sony Librie) sənədləri və mətnləri üçün LRF fayl uzantısından istifadə edir. Bu xüsusi fayl növü, eləcə də əlaqəli LRS və LRX faylları artıq köhnəlmişdir. Bu üç fayl növü 2010-cu ildə Sony öz elektron kitablarını EPUB formatında satmağa başlayanda dayandırılmış Genişzolaqlı elektron Kitabı (BBeB) təşkil edirdi.

## LRF fayl formatı

LRF fayl formatının ətraflı spesifikasiyası [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat) ünvanında mövcuddur. LRF faylı aşağıdakılardan ibarətdir:
* başlıq

* bir sıra obyektlər

* obyekt indeksi.


Bütün bu dəyərlər Intel (öncə LSB) qaydasındadır.

### LRF başlığı

|Offset (hex) |Ölçü(bayt) |Ad/məna| Nümunə dəyər|
---|---|---|---|
|0 |8| LRF İmzası| 4C 00 52 00 46 00 00 00 = Unicode-də LRF|
|8 |2| versiya?| Əksər fayllarda 999|
|A |2| Psuedo-Şifrələmə |açar baytı 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| NumberOfObjects |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| naməlum| 0|
|24 |1| Bayraqlar| (16 - arxadan önə, 1 = öndən arxaya) 16|
|25 |1| naməlum |(doldurma?) 0|
|26 |2| naməlum| 1600|
|28 |2| naməlum| (doldurma?) 0|
|2A |2| Hündürlük?| 600|
|2C |2| Eni?| 800|
|2E |1| naməlum| 24|
|2F |1| naməlum |(doldurma?) 0|
|30 |0x14| naməlum| sıfırlar|
|44 |4| Yalnız PlaneStream (0x1E) obyektinin obyekt identifikatoru| 0x0042|
|48 |4| naməlum |0x1536|
|4C |2| XMLCompSize| 0x035C|


## İstinadlar

* [LRF Fayl Format](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)

* [BBeB - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/BBeB)


