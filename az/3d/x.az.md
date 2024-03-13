{
  "date": "2020-01-11",
  "keywords": [
"x faylı",
"x fayl formatı",
"x faylı nədir",
"fayl",
"x misal",
"x fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X - DirectX 2.0 Fayl Formatı",
  "description": "DirectX X fayl formatı və DirectX X fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "X",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d--azx"
}
},
  "lastmod": "2020-01-11"
}

## X faylı nədir?

A file with .x extension refers to [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy file format that was introduced with Microsoft DirectX 2.0. O, oyunlarda 3D qrafika göstərilməsi üçün istifadə edilib və şəbəkələr, fakturalar, animasiyalar və istifadəçi tərəfindən müəyyən edilmiş obyektlər üçün strukturları müəyyənləşdirir. Autodesk FBX fayl formatı daha müasir format kimi daha yaxşı xidmət etdiyi üçün 2014-cü ildən bu yana köhnəlib. X şablonla idarə olunur və hər hansı istifadə məlumatından azaddır.

Siz Microsoft DirectX və ümumi mətn redaktorlarından istifadə edərək DirectX X fayllarını aça bilərsiniz.

## X fayl formatı

[X file reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) DirectX .x faylları ilə işləmək üçün istifadə olunan API elementləri üçün istinad məlumatını ehtiva edir. Bu format digər proqramlar tərəfindən məlumat şablonları vasitəsilə daha yüksək səviyyəli primitivləri müəyyən etmək üçün istifadə edilən aşağı səviyyəli məlumat primitivlərini təmin edir. DirectX 6.0 .x fayllarından oxumağa və onlara yazmağa imkan verən interfeyslər və üsulları təqdim etdi. DirectX 3.0 bu fayl formatının ikili versiyasını təqdim etdi.

DirectX 9 tərəfindən müəyyən edilən [X file format reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) ikili formatda .x faylları, eləcə də Mətn Kodlaşdırmaları üçün istinad məlumatını ehtiva edir.

### İkili Kodlaşdırma

[binary format](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) DirectX X formatını mətn formatının tokenləşdirilmiş təsviri kimi müəyyən edir. Bu əlamətlər qrammatik quruluş vermək üçün müstəqil ola bilər və ya lazımi məlumatları təmin edən rekord göstəricilər ola bilər.

#### Başlıq

Binar başlığı aşağıdakı təriflərdən istifadə etməklə oxumaq və yazmaq olar.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Mətn Kodlaşdırması

DirectX .x faylları faylın necə istifadə olunduğundan asılı deyil və heç bir proqrama xas deyil. Bu şablona əsaslanan yanaşma .x fayl formatının istənilən müştəri tətbiqi tərəfindən istifadə edilməsinə imkan verir.


#### Başlıq

Dəyişən uzunluqlu başlıq məcburidir və məlumat axınının əvvəlində olmalıdır. Başlıq aşağıdakı məlumatları ehtiva edir.

|Növü |Alt Növ |Ölçü |Mündərici |Məzmun mənası|
---|---|---|---|---|
|Sehrli Nömrə (tələb olunur)| | 4 bayt |xof |
|Versiya nömrəsi (tələb olunur) |Əsas rəqəm |2 bayt |03 |Əsas versiya 3|
| |Minor Number |2 bayt |02 |Kiçik versiya 2|
|Format növü (tələb olunur)| |4 bayt |txt  |Mətn faylı|
| | | |bin | İkili Fayl|
| | | |tzip| MSZip Sıxılmış Mətn Faylı|
| | | |bzip| MSZip Sıxılmış İkili Fayl|
|Float ölçüsü (tələb olunur)| |4 bayt| 0064| 64-bit üzən |
| | | |0032 |32-bit üzənlər|


## İstinadlar

 * [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
 * [DirectX 9 Fayl Format Referansı](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

