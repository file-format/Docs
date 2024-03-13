{
  "date": "2021-07-29",
  "keywords": [
"shx faylı",
"shx fayl formatı",
"shx faylı nədir",
"fayl",
"shx nümunəsi",
"shx fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SHX - Shapefile Shape Index Format",
  "description": "SHX fayl formatı və SHX fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "SHX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-azx"
}
},
  "lastmod": "2021-07-29"
}

## SHX faylı nədir?
SHX faylı sürətlə irəli və geri axtarmağa imkan verən xüsusiyyət həndəsəsinin mövqe indeksi olan forma indeksi formatına aiddir. SHX birbaşa giriş ofset faylıdır. Bu faylda heç bir məlumat yoxdur, yalnız ilk yüz baytın dublikat nüsxəsi, qeyd nömrəsi və shp-də həmin qeydin başlanğıc baytına ofset. Nəzərə alın ki, .shx uzantılı fayl [SHP](/gis/shp/) və [DBF](/database/dbf/)-ni birləşdirmir.

## SHX fayl formatı
SHX formatı xüsusiyyət həndəsəsinin mövqe indeksini və SHP faylına bənzər 100 bayt başlığı, ardınca aşağıdakı iki sahəni ehtiva edən istənilən sayda 8 baytlıq sabit uzunluqlu qeydləri ehtiva edir:
| Bayt | Növ | Endianness | İstifadə |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | böyük | Record ofset (16-bit sözlərlə) |
| 4–7 | int32 | böyük | Qeyd uzunluğu (16 bitlik sözlərlə) |

Bu indeks əvvəlcə forma indeksində geriyə doğru axtarmaq və sonra rekord ofsetini oxumaqla şəkl faylında geriyə doğru axtarmağa imkan verir. Bu ofset SHP faylında düzgün mövqe axtarmaq üçün istifadə edilə bilər. Siz həmçinin irəli axtara bilərsiniz; eyni metoddan istifadə edən ixtiyari sayda qeydlər. Baxmayaraq ki, bir SHP faylı ilə birlikdə tam indeks yaratmaq mümkündür, lakin bu, SHP faylını tez pozmaq şansını artıra bilər.


## İstinadlar

* [Shapefile - Wikipedia tərəfindən)](https://en.wikipedia.org/wiki/Shapefile)



