
{
  "date": "2023-01-05",
  "keywords": [
"pov faylı",
"pov fayl formatı",
"pov faylı nədir",
"fayl",
"pov nümunəsi",
"pov fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "POV fayl formatı və POV fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "title": "POV - Görmə Faylının Davamlılığı",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-azv"
}
},
  "lastmod": "2023-01-05"
}

## POV faylı nədir?

POV faylı POV-Ray şüa izləmə proqramı üçün təlimatları ehtiva edən düz mətn faylıdır. Bu təlimatlar POV-Ray üçün xüsusi olan xüsusi skript dilində yazılmışdır. O, göstəriləcək səhnəni, o cümlədən 3D obyektləri, materiallar, işıqlandırma və səhnənin görünüşünü müəyyən edən digər xassələri müəyyənləşdirir. POV faylları POV-Ray üçün xüsusi olan və mürəkkəb və təfərrüatlı 3D səhnələr yaratmaq üçün istifadə edilə bilən xüsusi skript dilindən istifadə edir. POV faylı üçün fayl uzantısı adətən .pov və ya .povray olur. POV-Ray-də POV faylını açdığınız zaman proqram fayldakı təlimatları oxuyur və onlardan səhnənin göstərilən görüntüsünü yaratmaq üçün istifadə edir.

.pov faylları tez-tez rəssamlar və dizaynerlər tərəfindən film, televiziya, video oyunlar və marketinq materialları daxil olmaqla müxtəlif proqramlar üçün 3D qrafika və animasiya yaratmaq üçün istifadə olunur.

## POV fayl formatı

**.pov faylı** adətən bir sıra **#include** ifadələri ilə başlayır, bunlardan səhnədə istifadə oluna bilən əvvəlcədən təyin edilmiş rənglərin, teksturaların və digər resursların kitabxanalarını daxil etmək üçün istifadə olunur. Sonra fayl bir sıra bloklardan istifadə edərək səhnənin obyektlərini, materiallarını və digər xüsusiyyətlərini müəyyənləşdirir. .pov faylında təyin edə biləcəyiniz bir çox başqa növ obyektlər, materiallar və digər xüsusiyyətlər var və siz daha mürəkkəb və təfərrüatlı səhnələr yaratmaq üçün döngələrdən və şərti ifadələrdən istifadə edə bilərsiniz.

## POV üçün proqram təminatı

.pov fayl formatı POV-Ray şüa izləmə proqramı tərəfindən istifadə olunur, buna görə də .pov fayllarının açılması üçün əsas proqram POV-Ray proqramının özüdür. Siz POV-Ray proqramının son versiyasını https://www.povray.org/ ünvanındakı rəsmi internet saytından yükləyə bilərsiniz.

POV-Ray ilə yanaşı, .pov fayllarını aça və redaktə edə bilən bir sıra digər proqramlar da var, o cümlədən:

- BRL-CAD: .pov fayllarını idxal və ixrac edə bilən açıq mənbəli 3D modelləşdirmə proqramı
- MeshLab: .pov fayllarını idxal və ixrac edə bilən 3D mesh emal proqramı
- Blender: .pov fayllarını idxal və ixrac edə bilən məşhur açıq mənbəli 3D qrafika proqramı

.pov fayllarını aça bilən başqa proqram proqramları da ola bilər, ona görə də yuxarıdakı proqramlarla .pov faylını aça bilmirsinizsə, fayl görüntüləyicisi və ya çevirici alətdən istifadə etməyə cəhd edə bilərsiniz.

## POV nümunəsi

Məsələn, burada tək mavi silindrli səhnəni təyin edən nümunə .pov faylı var:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

Bu misalda kamera bloku səhnədəki kameranın mövqeyini və oriyentasiyasını, işıq_mənbəsi” bloku işıq mənbəyini elan edir və onun mövqeyini və rəngini, silindr” bloku isə silindr obyektini elan edir və onun son nöqtələrini təyin edir, radius və material xüsusiyyətləri. Bu .pov faylını POV-Ray proqramında açdığınız zaman o, tək mavi silindr şəklini verəcəkdir.

## İstinadlar
 * [POV-Ray - Vikipediya](https://en.wikipedia.org/wiki/POV-Ray)
 * [Sənədləşdirmə POV-Ray Vebsaytı](http://www.povray.org/documentation/)

