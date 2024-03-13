{
  "date": "2021-06-09",
  "keywords": [
"cda",
"fayl",
"uzadılması",
"format",
"cda faylı nədir",
"musiqi",
"cda fayl formatı",
"cda fayl formatının spesifikasiyası"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "CDA faylları yarada, çevirə və aça bilən CDA fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "CDA - CD Audio Track Qısayol Faylı",
  "linktitle": "CDA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-cda"
}
},
  "lastmod": "2021-06-09"
}

## CDA faylı nədir?

.cda uzantılı fayl audio CD-dəki hər bir audio trek üçün Microsoft Windows tərəfindən yaradılan kiçik stub fayldır. Bu fayllar istifadəçilərə xüsusi audio treklərə daxil olmaq imkanı verən trek vaxtları və Windows qısayolu kimi tipik məlumatları ehtiva edir. CDA faylları musiqi deyil, onlar yaddaşda bir yerdə mövcud olan musiqi faylına işarə edir. CD-də yerləşən audio faylın qısa yolu kimi deyə bilərik.

## CDA fayl formatı

CDA fayl formatı kompüterə hansı audio faylı CD-də səsləndirəcəyini söyləmək üçün istifadə olunur. Beləliklə, CDA faylları təmsil etdikləri CD-dən ayrılaraq yararsız hala gəlir. CDA faylları adətən RIFF resursları kimi qəbul edilir. CDDA adlı və .cda faylının cari versiyasında FMT adlı yalnız bir məlumat blokunu ehtiva edən yalnız bir yığın var. Bu blok 24 bayt uzunluğundadır. Windows tərəfindən yaradılmış identifikator Windows 95 və Windows 98 ilə əlaqəli CD sürücüsü tərəfindən istifadə olunur və onun pleyeri FreeDB və ya CDDB-yə qoşula bilmir. Bu məlumatı cdplayer.ini faylına əl ilə daxil etməli olduğunuz mahnının başlığını və ifaçının adını göstərə bilməsi üçün.

### CDA faylının təşkili

Aşağıdakı cədvəl tipik ofsetlər haqqında məlumatları göstərir:
| ofset | uzunluq | məzmun |
---|---|---|
| 0x00 | 4 | 4 ASCII simvolu RIFF |
| 0x04 | 4 | aşağıdakı parçanın ölçüsü: həmişə 36 (44 - 8), 4 baytda (Intel sifarişi) |
| 0x08 | 4 | chunk identifier: the 4 ASCII characters "CDDA"-az |
| 0x0C | 4 | 3 ASCII simvolu fmt və ardınca boşluq |
| 0x10 | 4 | parçanın uzunluğu: həmişə 24, 4 baytda (Intel sifarişi) |
| 0x14 | 2 | version of the CD format, on 2 bytes (Intel order). In May 2006, always equal to 1. |
| 0x016 | 2 | number of the range, on 2 bytes (Intel order). The first track has the number 1. |
| 0x18 | 4 | cdplayer.exe üçün Windows tərəfindən hesablanmış identifikator. |
| 0x1c | 4 | diapazon ofseti, kadrların sayında (Intel sifarişi) |
| 0x20 | 4 | trekin müddəti, kadrların ümumi sayı (Intel sifarişi) |
| 0x24 | 1 | sıra mövqeyi: çərçivələr |
| 0x25 | 1 | diapazon mövqeyi: saniyə |
| 0x26 | 1 | diapazon mövqeyi: dəqiqə |
| 0x27 | 1 | null bayt (ikili dəyər 0) |
| 0x28 | 1 | trekin müddəti: kadrlar |
| 0x29 | 1 | trekin müddəti: saniyə |
| 0x2a | 1 | trekin müddəti: dəqiqə |
| 0x2b | 1 | null bayt (ikili dəyər 0) |

## İstinadlar

* [.cda faylı - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/.cda_file)


