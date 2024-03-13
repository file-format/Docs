{
  "date": "2021-02-25",
  "keywords": [
"bdf faylı",
"bdf fayl formatı",
"bdf faylı nədir",
"fayl",
"bdf nümunəsi",
"bdf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "BDF - Glyph Bitmap Distribution Format",
  "description": "BDF fayl formatı və BDF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "BDF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-bd-azf"
}
},
  "lastmod": "2021-02-25"
}

## BDF faylı nədir?
BDF faylları insan tərəfindən oxuna bilən formadır və adətən ASCII kodlaşdırmasında paylanır. Fayl tam şriftlə əlaqəli qlobal məlumatla başlayır, ardınca fərdi qliflər üçün məlumat və bitmaplar. İçindəki məlumatlar bir ölçülü oriyentasiya üçün şrift üçün göstərilir. Birdən çox istiqamətdə istifadə ediləcək ölçülər bir faylda ola bilər. BDF faylında hər bir element faylda ayrıca mətn sətirində yerləşir. Xəttdəki elementləri ayırmaq üçün boşluqlardan istifadə olunur.

## BDF fayl formatı
Glyph Bitmap Distribution Format üçün BDF şortları; Adobe-ə məxsus olan bitmap tipli şriftləri saxlamaq üçün fayl formatıdır. Məzmun kompüter və insanların oxuya biləcəyi mətn faylı formasını alır. BDF xüsusilə Unix X Window mühitlərində istifadə olunur. O, geniş şəkildə daha səmərəli olacağı güman edilən PCF şrift formatı və OpenType və TrueType şriftləri ilə əvəz edilmişdir.
### BDF fayl strukturu
BDF şrift faylı üç bölmədən ibarətdir:

- şriftdəki bütün qliflərə aid olan qlobal bölmə.
- hər qlif üçün ayrıca girişi olan bölmə.
- ENDFONT bəyanatı.

## Misal
Budur, ASCII baş hərfi 'A' üçün bir qlifdən ibarət şrift nümunəsi. Onun qlobal bəyannamələri STARTFONT xətti ilə başlayır və CHARS xətti ilə bitir
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## İstinadlar
 * [Glif Bitmap Paylama Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
 * [Glif Bitmap Paylanma Formatının (BDF) Spesifikasiyası](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

