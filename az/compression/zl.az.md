{
  "date": "2019-12-09",
  "keywords": [
"zl faylı",
"zl fayl formatı",
"zl faylı nədir",
"fayl",
"zl nümunəsi",
"zl fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZL - ZLIP sıxılmış fayl formatı",
  "description": "ZL faylları yarada və aça bilən ZL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "ZL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-z-azl"
}
},
  "lastmod": "2021-04-14"
}

## ZL faylı nədir?

.zl uzantılı fayl, faylları sıxmaq üçün DEFLATE sıxılma alqoritminin variantından istifadə edən ZLIP sıxılmış fayl formatıdır. O, CPU tipindən, əməliyyat sistemindən, fayl sistemindən və simvol dəstindən müstəqildir və buna görə də məlumat mübadiləsi üçün istifadə edilə bilər. ZLIP sıxılmasının texniki spesifikasiyası [IETF site](https://tools.ietf.org/html/rfc1950)-də mövcuddur və tərtibatçının nöqteyi-nəzərindən istinad edilə bilər.

## ZL fayl formatı

Zlib axını aşağıdakı quruluşa malikdir:

 * `CMF (Compression Method and flags)` - Bu bayt sıxılma üsulundan asılı olaraq 4 bitlik sıxılma metoduna və 4 bitlik məlumat sahəsinə bölünür.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
 * `CM (Sıxılma metodu)` - Faylda istifadə olunan sıxılma metodunu müəyyən edir. Onun dəyərləri və müvafiq sıxılma üsulu aşağıdakı kimidir.

| CM Dəyəri| Sıxılma|
|---|---|
|CM = 8|32K-a qədər pəncərə ölçüsü ilə DEFLATE|
|CM = 15|Ehtiyatdadır|

 * `CINFO (Sıxılma məlumatı)` - CM = 8 üçün CINFO LZ77 pəncərə ölçüsünün əsas-2 loqarifmidir, mənfi səkkiz (CINFO=7 32K pəncərə ölçüsünü göstərir).

 * `FLG (FaGs)` - Bu bayraq baytı aşağıdakı kimi bölünür:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## İstinadlar ##

* [Zlib Fayl Formatının Xüsusiyyətləri](https://tools.ietf.org/html/rfc1950)


