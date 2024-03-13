{
  "date": "2019-10-11",
  "keywords": [
"gbr faylı",
"gbr fayl formatı",
"gbr faylı nədir",
"fayl",
"gbr misal",
"gbr fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GBR Fayl Format - PCB üçün Gerber Fayl Format",
  "description": "GBR faylları yarada və aça bilən GBR fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "GBR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gb-azr"
}
},
  "lastmod": "2019-09-10"
}

## GBR faylı nədir?

.gbr uzantılı fayl çap dövrə lövhəsi (PCB) dizayn məlumatlarının ötürülməsi üçün Gerber təsvir faylı formatıdır. Ucamco tərəfindən hazırlanmışdır. PCB dizayn məlumatları emal üçün istehsal sənayesi tərəfindən tələb olunan əsas komponentdir. GRB faylı mis təbəqələr, lehim maskası, əfsanə və qazma və marşrut məlumatları kimi PCB məlumatlarını ehtiva edir. Standart formatda qalınlıq və ya bitirmə daxil olmaqla, PCB istehsal xüsusiyyətləri kimi məlumatları ötürmək üçün istifadə edilə bilər. Bütün PCB dizayn sistemləri PCB istehsal sistemləri tərəfindən idarə oluna bilən Gerber fayllarını çıxarır. GBR faylları indi çap dövrə lövhəsi (PCB) dizayn məlumatlarının ötürülməsi üçün faktiki standart halına gəldi. Ucamco GBR fayl formatlarını açmaq və baxmaq üçün [free online viewer](https://gerber-viewer.ucamco.com/) təmin etmişdir.

## GBR fayl formatı

GBR yalnız 27 əmrdən ibarət olan UTF-8 insan tərəfindən oxuna bilən formatdır. Əmrlərin bu qısa siyahısına və onun yığcamlığına görə GBR-də debug etmək asandır. Gerber 2D ikili şəkillər üçün açıq vektor formatıdır. Meta-məlumatlar Atributlar vasitəsilə şəkillərlə ötürülür. Tək GRB faylı tək təsviri təyin edir və hər hansı müşayiət olunan faylların və ya xarici parametrlərin şərh edilməsini tələb etmir. Bir şəkilə yalnız bir fayl lazımdır. O, çap edilə bilən spesifikasiyada müəyyən edilmiş bütün əmrlər və adlar üçün 7 bitlik ASCII simvollarından istifadə edir. Bu, tam təsvirin yaradılmasını tam əhatə edir.

### Nümunə GBR Faylı

Aşağıda mənşəyə mərkəzləşdirilmiş 1,5 mm diametrli bir dairə yaradan nümunə Gerber faylı verilmişdir. Hər sətirdə bir əmr var.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## İstinadlar

 * [Gerber Format](https://www.ucamco.com/en/gerber)

