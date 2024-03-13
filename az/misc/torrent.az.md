{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Torrent fayl formatı - BitTorrent faylı",
  "description":"TORRENT faylları yarada və aça bilən TORRENT faylları və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent-az",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## TORRENT faylı nədir?

TORRENT faylı BitTorrent və digər P2P (peer-to-peer) proqramları tərəfindən məzmunun yüklənməsi və mübadiləsi üçün istifadə olunan mətn faylıdır. Yüklənə bilən məzmuna sənədlər, videolar, oyunlar, filmlər və internetdə mövcud olan digər media daxil ola bilər. Buraya yüklənəcək medianın məzmunu və yeri haqqında metadata məlumatı daxildir. BitTorrent kimi proqram təminatı məlumatların endirilməsi üçün bu fayldan ad, fayl ölçüsü və qovluq strukturu kimi məlumatlardan istifadə edir. Torrent faylları onlayn olaraq [PDF](/pdf/) kimi digər fayl formatlarına çevrilə bilər.

## Torrentinq nədir? Məlumat mübadiləsi üçün TORRENT fayl formatı

Torrentinq BitTorrent şəbəkəsindən istifadə edərək məlumat fayllarının mübadiləsi (endirilməsi və yüklənməsi) anlayışıdır. Başqalarının daxil olmaq və yükləmək üçün məlumatların yükləndiyi adi serverlərdən fərqli olaraq, torrent faylları torrent şəbəkəsindən istifadə edərək götürülür və göndərilir. İstifadəçi BitTorrent kimi proqramlarda .torrent faylını açdıqda, proqram faylın məzmununu bit istiqamətində endirməyə başlayır. Birdən çox istifadəçi eyni fayla sahibdirsə, yükləmə prosesini sürətləndirmək üçün BitTorrent yükləmələri bütün istifadəçilər arasında bölür. Eyni zamanda, faylı yükləyən istifadəçinin kompüteri də onu eyni faylı yükləyən digər istifadəçilərə göndərmək üçün fayl mənbəyinə çevrilir.

### TORRENT faylının strukturu

Torrent faylı faylların siyahısı və yüklənəcək faylın bütün hissələri haqqında metadata məlumatlarının birləşməsidir. O, düymələr şəklində aşağıdakı məlumatları ehtiva edir.

- `announce` — Faylın mövcudluğu haqqında məlumat vermək üçün digər həmyaşıdlara elan edilən izləyicinin URL-i
- `info` — Bu, açarları bir və ya bir neçə faylın paylaşılıb-paylaşılmamasından asılı olan lüğətə xəritə verir:
  - "fayllar—hər biri fayla uyğun gələn lüğətlərin siyahısı (yalnız bir neçə fayl paylaşıldıqda). Hər bir lüğətdə aşağıdakı düymələr var:"
- `uzunluq` — faylın baytla ölçüsü.
- `yol` — sonuncusu faktiki fayl adı olan alt kataloq adlarına uyğun sətirlərin siyahısı
- `uzunluq` — faylın baytlarla ölçüsü (yalnız bir fayl paylaşılan zaman)
- `ad` — faylın saxlanacağı fayl adı
- `parça uzunluğu` — parça başına baytların sayı. Bu adətən 28 KiB = 256 KiB = 262,144 B-dir.
- `parçalar` — hər bir parçanın SHA-1 hashinin birləşməsindən ibarət hash siyahısı.

## Torrenting Təhlükəsiz və Qanunidirmi?

P2P istifadəçiləri arasında məlumat mübadiləsi üçün torrent protokolu təhlükəsizdir, çünki bu, sadəcə olaraq istənilən növ faylın paylaşılması vasitəsidir. Beləliklə, protokolun özü təhlükəli və ya qanunsuz deyil. Bununla belə, şəbəkə vasitəsilə paylaşılan məzmunda paylaşılan sənədlərin hüquqi statusunu poza bilən fayllar və ya media ola bilər. Bu halda, bu cür məlumatların mübadiləsi bu cür faylların açıq şəkildə paylaşılmasında iştirak edən tərəflərə qarşı hüquqi tədbirlərə səbəb ola bilər.

## İstinadlar

* [TORRENT Faylı - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)


