{
  "date": "2021-07-15",
  "keywords": [
"TMP",
"uzadılması",
"fayl",
"format",
"sistemi",
"TMP faylı",
"TMP sənədləri",
"TMP faylları",
"Müvəqqəti fayl",
"tətbiq",
"proqramlar"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "TMP - müvəqqəti fayl formatı",
  "description": "TMP fayl formatı və TMP faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "TMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-tm-azp"
}
},
  "lastmod": "2021-07-15"
}

## TMP faylı nədir? ##

TMP faylı proqram proqramı tərəfindən yaradılan müvəqqəti ehtiyat nüsxəsinə, yaddaşa və ya digər fayl sisteminə aiddir. O, bəzən görünməz bir fayl kimi yaradılır və proqramdan çıxdıqda tez-tez məhv edilir. TMP faylları yeni fayl qurularkən məlumatı müvəqqəti saxlamaq üçün də istifadə edilə bilər.

## TMP Fayl Format ##

TMP faylı adətən materialın bir üslubdan digərinə çevrilməsi prosesində bir mərhələ kimi istifadə olunan xam məlumatlardan ibarətdir. Microsoft Word və Apple Safari TMP fayl formatını yarada və istifadə edə bilən iki proqramdır.

Yaradılan TMP sənədləri, nəzəri olaraq, proqram bağlandıqda və ya maşın söndürüldükdə avtomatik olaraq silinməlidir. Praktikada bu həmişə belə olmur. Nəticədə, proqramınızın sənədləri arasında naviqasiya edərkən sistem və ya hər hansı digər proqram tərəfindən aktiv istifadə olunmayan keçici fayllarla rastlaşa bilərsiniz.

### Köməkçi yaddaş ###

Virtual yaddaş əməliyyat sistemlərində istifadə olunur, lakin böyük həcmdə məlumatdan istifadə edən proqramlar müvəqqəti sənədlər hazırlamalı ola bilər.

### Proseslərarası əlaqə ###

Əksər əməliyyat sistemləri borular, rozetkalar və ya əsas yaddaş kimi proqramlar arasında məlumat ötürmək üçün primitivlər təmin edir, lakin ən sadə üsul faylları müvəqqəti fayla köçürmək və müvəqqəti faylın yerini qəbul edən proqrama məsləhət verməkdir.


## Texniki Spesifikasiya ##

Fərqli müvəqqəti sənəd adlarının əldə edilməsi adətən əməliyyat sistemləri və proqram proqramları tərəfindən təmin edilir.
Müvəqqəti fayllar mkstemp və ya tmpfile kitabxana funksiyalarından istifadə edərək POSIX sistemlərində təhlükəsiz şəkildə yaradıla bilər. Bəzi sistemlərə əvvəlki POSIX (keçdiyindən) mktemp tətbiqi daxildir. Bu fayllar adətən Unix platformalarında /TMP-də adi müvəqqəti kataloqda və ya Windows maşınlarında %TEMP% (giriş üçün xüsusidir) tapılır.

Proqram dayandıqda və ya sənəd bağlandıqda, tmpfile ilə yaradılan keçid faylı avtomatik olaraq silinir. GetTempFileName (Windows) və ya tmpnam (POSIX) onu yaradan proqramdan daha uzun müddət davam edəcək müvəqqəti fayl adı yaratmaq üçün istifadə edilə bilər.

## İstinad ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
