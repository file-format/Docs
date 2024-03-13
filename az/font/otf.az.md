{
  "date": "2020-08-20",
  "keywords": [
"otf faylı",
"otf fayl formatı",
"otf faylı nədir",
"fayl",
"otf misal",
"otf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTF - TrueType şrift fayl formatı",
  "description": "OTF fayl formatı və OTF faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "OTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-ot-azf"
}
},
  "lastmod": "2020-09-21"
}

## OTF faylı nədir?

.otf uzantısı olan fayl OpenType şrift formatına aiddir. OTF şrift formatı daha genişlənir və rəqəmsal tipoqrafiya üçün [TTF](/font/ttf/) formatlarının mövcud xüsusiyyətlərini genişləndirir. Microsoft və Adobe tərəfindən hazırlanmış OTF özündə PostScript və TrueType şrift formatlarının xüsusiyyətlərini birləşdirir. Bu, OTF formatını əksər yazı sistemlərinə uyğunlaşdırır və buna görə də əsas kompüter platformalarında vahid şəkildə istifadə olunur. OpenType şrift formatı Mac OS X və Windows 2000 və sonrakı versiyalar tərəfindən dəstəklənir.

## Qısa tarix

The requirement of OpenType fonts originated as a requirement for a more expressive font format that could handle fine typography. In addition, it was aimed to meet the requirements of complex behaviour of many of the world's writing systems. Microsoft attempted to license Apple's advanced typography technology, known as GX Typography, in the early 1990's. This didn't go well and as a result, Microsoft started enhancing its owns TrueType font technology in 1994. Dəyişikliklər həmçinin Adobe-nin 1-ci Tip (PostScript) şrift formatlarının xüsusiyyətlərinə cavab verən daha uyğun şrift formatını təqdim etmək üçün də daxil edilmişdir.

Adobe, 1996-cı ildə Microsoft-a həm Apple-ın TrueType, həm də öz Type 1 şrift formatlarını əvəz etmək səylərinə qoşuldu. Bu, məhdudiyyətləri aradan qaldırmaq və yeni genişləndirmələr əlavə etmək üçün hər iki əsas şrift formatının birləşməsi ilə nəticələndi. Bu yeni texnologiya eyni il **OpenType** adı ilə təqdim edildi.

## OTF Fayl Formatının Xüsusiyyətləri

OTF specifications are available publicly by Microsoft and can be referred to from developer's perspective. Like TTF, it uses the same 'sfnt' container structure and is compatible with the TrueType specifications. Data inside an OpenType font file is used for different purposes such as calculating the text layout, defining glyphs as TrueType or Compact Font Format (CFF) outlines, providing monochromatic or color bitmaps or SVG documents as alternate glyph descriptions, and meta-data information.

### OTF Məlumat Növləri
OTF faylları Big Endian-da olan aşağıdakı məlumat növlərindən istifadə edir.

|Məlumat növü| Təsvir|
---|---|
|uint8| 8 bitlik işarəsiz tam ədəd.|
|int8| 8 bitlik işarəli tam ədəd.|
|uint16| 16 bitlik işarəsiz tam ədəd.|
|int16| 16 bit işarəli tam ədəd.|
|uint24| 24 bitlik işarəsiz tam ədəd.|
|uint32| 32-bit işarəsiz tam ədəd.|
|int32| 32 bit işarəli tam ədəd.|
|Sabit| 32-bit imzalı sabit nöqtə nömrəsi (16.16)|
|FWORD| şrift dizayn vahidlərində kəmiyyəti təsvir edən int16.|
|UFWORD| şrift dizayn vahidlərində kəmiyyəti təsvir edən uint16.|
|F2DOT14| Aşağı 14 bit fraksiya ilə 16 bit imzalanmış sabit nömrə (2.14).|
|LONGDATETIME| Tarix və vaxt, 1 yanvar 1904-cü il, UTC, gecə 12:00-dan etibarən saniyələrlə göstərilir. Dəyər işarələnmiş 64 bitlik tam ədəd kimi təmsil olunur.|
|Etiket| Cədvəl, dizayn-variasiya oxu, skript, dil sistemi, xüsusiyyət və ya baza xəttini müəyyən etmək üçün istifadə edilən dörd uint8s massivi (uzunluq = 32 bit)|
|Ofset16| Cədvəl üçün qısa ofset, uint16 ilə eyni, NULL ofset = 0x0000|
|Offset32| Cədvəl üçün uzun ofset, uint32 ilə eyni, NULL ofset = 0x00000000|
|Versiya16Nöqtə16| Əsas və kiçik versiya nömrələri ilə dolu 32 bit dəyər. (Cədvəl Versiya Nömrələrinə baxın.)|

### OTF cədvəlləri kataloqu

OTF faylı cədvəl kataloqu ilə başlayır. Bu kataloq şrift faylındakı cədvəllərin ən yüksək səviyyəli toplusudur. Fayldakı şriftlərin sayından asılı olaraq, cədvəl kataloqu faylın müxtəlif yerində yerləşə bilər. Məsələn, şrift faylında yalnız bir şrift varsa, cədvəl kataloqu faylın 0 baytından başlayır. Birdən çox OpenType Şrift kolleksiyası olduqda,
cədvəl kataloqunun başlanğıcı TTCHeader-də göstərilir.

|Növü |Adı |Təsviri|
---|---|---|
|uint32 |sfntVersion| 0x00010000 və ya 0x4F54544F ('OTTO')|
|uint16| numTables |Cədvəllərin sayı.|
|uint16|	searchRange	|Maximum power of 2 less than or equal to numTables, times 16 ((2\**floor(log2(numTables))) * 16, burada **” eksponentasiya operatorudur).|
|uint16 |entrySelector Log2 maksimum gücü 2 ədəddən az və ya ona bərabərdir (log2(searchRange/16), mərtəbəyə bərabərdir(log2(numTables))).|
|uint16	|rangeShift	|numTables times 16, minus searchRange ((numTables * 16) - axtarış aralığı).|
|tableRecord| tableRecords[numTables] |Cədvəl qeydləri massivi—şriftdə hər üst səviyyəli cədvəl üçün bir|


### Cədvəl qeydi

Şriftdəki hər bir yuxarı səviyyəli cədvəl üçün aşağıdakı sahələrdən ibarət Cədvəl Qeydi var.

|Növü| Adı| Təsvir|
---|---|---|
|Etiket| tableTag| Cədvəl identifikatoru.|
|uint32| yoxlama cəmi| Bu cədvəl üçün yoxlama məbləği.|
|Offset32| ofset| Şrift faylının əvvəlindən ofset.|
|uint32| uzunluq Bu cədvəlin uzunluğu.|

OpenType şrift faylındakı hər bir cədvəl cədvəl teqləri kimi tanınan adlarla təmsil olunur. Massivdəki bütün qeydlərin etiketə görə artan qaydada çeşidlənməsi mütləqdir.

## İstinadlar
 * [Microsoft tərəfindən OpenType Font Xüsusiyyətləri](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType İcmal](https://learn.microsoft.com/en-us/typography/truetype/)

