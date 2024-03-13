{
  "date": "2019-10-11",
  "keywords": [
"u3d faylı",
"u3d fayl formatı",
"u3d faylı nədir",
"fayl",
"u3d nümunəsi",
"u3d fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "U3D - Universal 3D Fayl Formatı",
  "description": "U3D fayl formatı və U3D fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "U3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-u3-azd"
}
},
  "lastmod": "2019-09-10"
}

## U3D faylı nədir?

**U3D** (Universal 3D) is a compressed file format and data structure for 3D computer graphics. It contains 3D model information such as triangle meshes, lighting, shading, motion data, lines and points with color and structure. The format was accepted as[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard in August 2005. 3D [PDF](/pdf/) sənədləri U3D obyektlərinin daxil edilməsini dəstəkləyir və onlara Adobe Reader proqramında baxıla bilər (versiya 7 və sonrakı).

U3D formatı üçölçülü məlumatların saxlanması və mübadiləsi üçün universal standart yaratmaq məqsədini nəzərə alaraq hazırlanmışdır. Bununla belə, format mübadilə formatı kimi istifadə edilməkdənsə, 3D PDF üçün kodlaşdırmada əsas istifadəsini tapır. Acrobat 3D dəstəklənən 3D fayl növünü PDF-ə çevirəndən sonra U3D və ya PRC formatına çevirir.

## U3D Fayl Format

U3D files are in binary file format that underwent four editions as described by the [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) reference document, resulting in specifications update with each edition. The PDF file standard ISO-32000 accepts U3D as allowed annotation and multimedia type.

U3D-nin ilk buraxılışı həndəsə, rəng, faktura, işıqlandırma, sümüklər və transformasiyaya əsaslanan animasiya kimi 3D qrafika xüsusiyyətlərinin əsas təsvirlərinə yönəldilmişdir. İkinci və üçüncü nəşrlər birinci nəşrdə bəzi səhvləri düzəltdi, üçüncü versiya isə sənaye proqram təminatında ən çox istifadə olunan növdür. Dördüncü nəşrdə daha yüksək dərəcəli primitivlər (əyri səthlər) üçün təriflər verilir. [U3D specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) ECMA saytında istifadəçi arayışı üçün onlayn mövcuddur.

### U3D fayllarında məlumat növləri

Binar faylda aşağıdakı növlər olacaq: U8, U16, U32, U64, I16, I32, F32, F64 və String.

 * U8 : İşarəsiz 8 bitlik tam ədəd
 * U16 : İşarəsiz 16 bitlik tam ədəd
 * U32 : İşarəsiz 32 bitlik tam ədəd
 * U64 : İşarəsiz 64 bitlik tam ədəd
 * I16 : İşarəli 16 bitlik tam ədəd
 * F32: IEEE tək dəqiqlikli float.
 * F64: IEEE ikiqat dəqiqlikli float.
 * Sətir: U3D faylındakı sətirlər sətirdəki simvolların ümumi uzunluğunu təyin edən imzasız 16 bitlik tam ədədlə başlayır. Sətirlər həmişə hərflərə həssas olaraq işlənir.

## U3D Fayl Strukturu

U3D faylı blokların ardıcıllığını ehtiva edir. Hər U3D faylında 3 fərqli blok növü var.

 * Fayl başlıq bloku
 * Bəyannamə bloku
 * Davam bloku

Əgər həmin blokdakı məlumat tələb olunmursa və ya həmin blok növü üçün dekoder mövcud deyilsə, yükləyici blokun sonunu müəyyən edir.

{{< figure src="../u3d.png" alt="U3D Fayl Format" >}}

### Fayl başlığı bloku
Fayl başlığı bloku faylın necə oxunacağını müəyyən etmək üçün yüklənmiş tərəfindən istifadə olunan fayl məlumatını ehtiva edir.

### Bəyannamə Bloku

Bəyannamə blokları fayldakı obyektlər haqqında məlumatları ehtiva edir. Bəyannamə blokundakı obyektlər müəyyən edilməlidir.

### Davam Bloku

Bəyannamə blokunda elan edilmiş obyektlər üçün əlavə məlumat davam blokunda verilir. Hər Davam Bloku Bəyannamə Bloku ilə əlaqələndirilməlidir.


## İstinadlar ##

* [U3D Fayl Format - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)

* [ECMA U3D Fayl Formatının Xüsusiyyətləri](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)


