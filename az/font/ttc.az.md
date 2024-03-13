{
  "date": "2021-02-25",
  "keywords": [
"ttc faylı",
"ttc fayl formatı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "TTC - TrueType Kolleksiya Fayl Formatı",
  "description": "TrueType Collection (TTC) faylı çoxsaylı şriftləri bir faylda birləşdirir. Həm Apple, həm də Microsoft Mac və Windows əməliyyat sistemlərində TTF-dən istifadə edirdilər.",
  "linktitle": "TTC",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-azc"
}
},
  "lastmod": "2021-02-25"
}

## TTC faylı nədir?
TTC qısaldılmış TrueType Collection True Type formatının uzantısıdır. TTC faylı bir neçə şrift faylını özündə birləşdirə bilər. Bu fayllar bir çox qlifləri paylaşan çoxsaylı şriftləri birləşdirmək üçün faydalıdır. Windows 2000-dən əvvəl TTC faylları Windows-un Çin, Yapon və Koreya versiyalarında istifadə olunurdu, lakin sonradan dəstək bütün regionlar üçün əlçatan oldu.


## Şrift Kolleksiyası Faylının Strukturu 
TTC faylı TTC Başlıq cədvəlindən, Cədvəl Kataloqlarından və çoxsaylı OpenType cədvəllərindən ibarətdir. TTC Başlığı faylın əvvəlində tapılmalıdır. Hər bir şrift üçün tam cədvəl kataloqu mövcud olmalıdır. TableDirectory formatı kolleksiya olmayan faylda olduğu kimi olmalıdır. TTC faylı daxilindəki bütün qovluqlardakı cədvəl sayları TTC faylının başlanğıcından hesablanır.
TTC faylındakı cədvəllərə müvafiq şriftlərin cədvəl kataloqu vasitəsilə istinad edilir. OpenType cədvəllərindən bir neçəsi TTC-yə əlavə edilmiş hər şrift üçün bir dəfə olmaqla bir neçə dəfə görünməlidir. Digər cədvəllər TTC faylında bir neçə şriftlə paylaşıla bilər.

### TTC Başlığı
Bu günə qədər TTC Başlıq cədvəlinin iki versiyası mövcuddur:
- Versiya 1.0 rəqəmsal imzasız TTC faylları üçün istifadə olunur.
- Versiya 2.0 rəqəmsal imzalı və ya olmayan TTC faylları üçün istifadə edilə bilər.
Hər iki versiyanın TTC Başlıq cədvəlləri bunlardır:

**TTC Başlıq Versiyası 1.0:**

|Növ|Ad|Təsvir|
---|---|---|
|TAG|ttcTag|Şrift Kolleksiyasının ID sətri: 'ttcf' (CFF və ya CFF2 konturları, həmçinin TrueType konturları olan şriftlər üçün istifadə olunur)|
|uint16|majorVersion|TTC Başlığının əsas versiyası, = 1.|
|uint16|minorVersion|TTC Başlığının kiçik versiyası, = 0.|
|uint32|numFonts|TTC-də şriftlərin sayı|
|Offset32|tableDirectoryOffsets[numFonts]|Faylın əvvəlindən hər bir şrift üçün TableDirectory-ə ofsetlər massivi|

**TTC Başlıq Versiyası 2.0:**

|Növ|Ad|Təsvir|
---|---|---|
|TAG|ttcTag |Şrift Kolleksiyası ID sətri: 'ttcf'|
|uint16| majorVersion |TTC Başlığının əsas versiyası, = 2.|
|uint16| minorVersion |TTC Başlığının kiçik versiyası, = 0.|
|uint32| numFonts |TTC-də şriftlərin sayı|
|Offset32| tableDirectoryOffsets[numFonts] |Faylın əvvəlindən hər bir şrift üçün TableDirectory-ə ofsetlər massivi|
|uint32| dsigTag |DSIG cədvəlinin mövcud olduğunu göstərən etiket, 0x44534947 ('DSIG') (imza yoxdursa null)|
|uint32| dsigLength |DSIG cədvəlinin uzunluğu (baytla) (imza yoxdursa null)|
|uint32| dsigOffset |DSIG cədvəlinin TTC faylının əvvəlindən ofseti (baytla) (imza yoxdursa null)|

## İstinadlar
 * [OpenType Şrift Faylı](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
 * [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

