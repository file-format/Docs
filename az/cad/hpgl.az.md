{
  "date": "2020-07-28",
  "keywords": [
"HPGL",
"Fayl Format",
"Açıq",
"Oxuyun",
"Yaradın",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "HPGL fayl formatı və HPGL fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "HPGL Fayl Format - Fayl Format Mütəxəssislərindən öyrənin!",
  "linktitle": "HPGL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-hpg-azl"
}
},
  "lastmod": "2020-07-28"
}

## HPGL faylı nədir?

HPGFL (Hewlett-Packard Graphics Language) faylı HP tərəfindən hazırlanmış plotter nəzarəti üçün təlimat dəstindən ibarətdir. HP plotterləri vektor və rastr məzmununu kağız üzərində çəkmək və çap etmək üçün bu fayldan istifadə edir.

### HPGL Komandanlığı

HPGL əmri aşağıdakılardan ibarətdir.
 * İki simvoldan ibarət əlifbanın əmr bölməsi
 * Parametr bölməsi
 * Terminator bölməsi

Fayldakı hər bir parametr bir neçə parametr olduqda ayırıcı ilə bölünməlidir.

### HPGL Komanda Nümunəsi

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Koordinat sistemi

Koordinat sistemləri hər hansı xüsusi yeri tapmaq üçün 2 ölçülü ölçmə göstəricilərindən ibarətdir. HPGL bu məqsədlə həm Plotter koordinat sistemindən, həm də istifadəçi koordinat sistemindən istifadə edir.

#### Plotter Koordinat Sistemi

Bu koordinat sistemi plotterin hərəkətinə əsaslanan çertyojları çəkmək üçün istifadə olunur. Minimum plotter hərəkətinin tipik XY vahidi 0,025 mm-dir. Rəsmin mümkün diapazonu plotter növləri ilə dəyişir.

#### İstifadəçi koordinat sistemi

İstifadəçi tərəfindən müəyyən edilmiş koordinat sistemi miqyasdan və mənşədən istifadə etməklə qurula bilər. Bunlar IP əmri və SC əmrindən istifadə edərək plotter koordinatlarına çevrilir. Bu çevrilmə həyata keçirilmədikdə plotter sisteminin koordinatları standart olaraq istifadə olunur.

## HPGL fayl formatı
HPGL faylları ASCII (mətn faylı) formatındadır və bir neçə quraşdırma əmri ilə başlayır. Bu, plan qurmaq üçün plotter üçün müəyyən parametrləri təyin edir. Tipik bir HPGL faylı aşağıdakı kimi görünür.

|Əmr|Mənası
---|---|
|IN;|insiallaşdırın, plan qurmağa başlayın|
|IP;|miqyaslama nöqtələrini (P1 və P2) standart mövqelərinə təyin edin|
|SP1;|qələm 1-i seçin|
|PU0,0;|Qələmi yuxarı qaldırın və növbəti hərəkət üçün başlanğıc nöqtəsinə keçin|
|PD100,0,100,100,0,100,0,0;|Qələmi Aşağı qoyun və aşağıdakı yerlərə keçin (səhifənin ətrafında bir qutu çəkin)|
|PU50,50;|Pen Up və X,Y koordinatlarına keçin 50,50|
|CI25;|radiusu 25| olan çevrə çəkin
|SS;|standart simvol dəstini seçin|
|DT*,1;|mətn ayırıcısını ulduz işarəsinə qoyun və onları çap etməyin (doğru mənasını verən 1)|
|PU20,80;|qələmi qaldırın və 20,80|-ə keçin
|LBHello World*;|etiket çəkin|

## İstinadlar
 * [Wikipedia tərəfindən HPGL](https://en.wikipedia.org/wiki/HP-GL)
 * [HPGL İstinad Bələdçisi](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

