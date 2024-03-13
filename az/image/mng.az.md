{
  "date": "2019-10-11",
  "keywords": [
"mng faylı",
"mng fayl formatı",
"mng faylı nədir",
"fayl",
"mng misal",
"mng fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MNG Fayl Format - Çox Şəkil Şəbəkə Qrafik Fayl Format",
  "description": "MNG fayl formatı və MNG fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-mn-azg"
}
},
  "lastmod": "2019-09-10"
}

## MNG faylı nədir?

.mng uzantılı fayl [PNG](/image/png/) şəkil formatına bənzəyən, lakin animasiya şəkillərini dəstəkləyən Çoxşəkilli Şəbəkə Qrafikası fayl formatıdır. PNG formatının əlavə animasiya funksiyası ilə həddən artıq yüklənməsinin qarşısını almaq üçün hazırlanmışdır. MNG də [GIF](/image/gif/) fayllarına bənzəyir, lakin daha çox sıxılma istifadə edir və tam alfa funksiyasını dəstəkləyir. MNG faylları üçün qeyri-rəsmi MIME media növü video/x-mng-dir. MNG faylları ImageMagik və IrfanView kimi proqramlarda açıla bilər.

## MNG fayl formatı

MNG fayl formatı PNG formatına bənzəyir və PNG spesifikasiyalarında müəyyən edilmiş eyni yığın strukturundan istifadə edir. MNG dekoderi deşifrəetmə təlimatları üçün hər hansı xüsusi bayraqlar göstərmədən PNG məlumat axınının şifrəsini açmağı bacarmalıdır. MNG bir neçə təsviri bir yerdə çərçivə şəklində qruplaşdırır, bəzi şəkillər bir yerdən digərinə keçmək üçün sprite kimi istifadə olunur. Mexanizm təsvir məlumatlarını təkrar ötürmədən təkrar istifadə etməyə imkan verir. Tərtibatçının istinadı üçün [MNG specifications](http://www.libpng.org/pub/mng/spec/) istinad edilə bilər.

### MNG İmzası

MNG məlumat axını aşağıdakıları ehtiva edən 8 baytlıq imza ilə başlayır:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Bu PNG imzasına bənzəyir, lakin PNG əvəzinə MNG ehtiva edir.

### MNG Çərçivəsi

MNG çərçivəsi daha kiçik şəkillərin iki ölçülü təsvirindən ibarətdir. Hər bir kiçik təsvirə satır və sütun indeksi birləşməsindən istifadə etməklə daxil olmaq olar. Format ikiölçülü müstəvilər seriyasından ibarət olan üçölçülü voksel məlumatlarını saxlamağa qadirdir. Hər bir təyyarə PNG və ya Delta-PNG məlumat axını ilə təmsil olunur. Hər bir Delta-PNG məlumat axını şəkili əsas PNG şəklindən fərqlər kimi müəyyən edir. Bu, hər biri üçün tam PNG məlumat axını istifadə etməkdənsə, sonrakı şəkilləri təmsil etmək üçün daha yığcam bir yol təqdim edir.

## İstinadlar ##

* [MNG](http://www.libpng.org/pub/mng/)

* [MNG Format v 1.0](http://www.libpng.org/pub/mng/spec/)


