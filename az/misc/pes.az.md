{
  "date": "2021-07-29",
  "keywords": [
"pes faylı",
"pes fayl formatı",
"pes faylı nədir",
"fayl",
"pes misal",
"pes fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PES Fayl Format - Brother PE Embroidery Format",
  "description": "PES faylları yarada və aça bilən PES fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "PES",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-pe-azs"
}
},
  "lastmod": "2021-07-29"
}

## PES Embroidery faylı nədir?

PES tikmə faylı tikmə/tikiş maşınları üçün təlimatları ehtiva edən dizayn faylıdır. O, Brother Industries tərəfindən tikmə maşınları üçün hazırlanmış, lakin sonradan ümumi fayl formatı kimi rəsmiləşdirilmişdir. PES faylları tikiş maşınları tərəfindən parça üzərində naxış tikmək üçün təlimatları oxumaq üçün istifadə olunur. Bu fayllar iki məqsədə xidmət edir; ilk olaraq Brother Industries tərəfindən hazırlanmış PE-Dizayn tətbiqi üçün dizayn məlumatı, ikincisi, dizayn adı, rəngləri və dayan, atlama və trim kimi tikmə maşını kodları təmin edir.

## PES Fayl Format - Ətraflı Məlumat

PES faylı ikili fayl formatında diskdə saxlanılır. Bu, əvvəlcədən təyin edilmiş metoddan istifadə edərək saxlanılan tikiş məlumatı olan bir neçə bölmədən ibarətdir. PES fayl formatı aşağıdakı kimidir.

 * Versiya Məlumatı - Versiya məlumatı verir və istənilən qiymət `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060` ola bilər.
 * PEC Axtarış Dəyəri - Versiya məlumatından dərhal sonra gələn 4 baytlıq kiçik endian tam ədəddir və dizayn təfərrüatlarını ehtiva edən PEC bölməsi üçün axtarış dəyərini təmsil edir.
 * PSE Bölməsi - Brother PE-Design ilə əlaqəli dizayn məlumatlarını ehtiva edir və digər tikiş proqramları ola bilər
 * PCE Bölməsi - PSE faylının istənilən yerində ola bilər, lakin PEC Axtarış Dəyəri tərəfindən istinad edilir.

## PES faylından istifadə edən tikiş maşınlarının növü

PES faylları ilk növbədə Brother tikiş maşınları ilə istifadə olunan PE-Dizayn Proqramı tərəfindən yaradılır. PES fayllarını dəstəkləyə biləcək bəzi digər maşınlara Babylock və Bernina ev tikmə maşınları daxildir.

## PSE fayllarını necə çevirmək olar?

PE-Design proqram proqramı .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd və ya .xxx kimi digər formatlara [convert PSE file](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl=pes+file) edə bilər . Bu, faylı açmaq və Dönüşüm formatını seçməklə PE-Design proqramından istifadə etməklə edilə bilər.

## İstinadlar

* [PE Dizayn - Təlimat Təlimatı](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)


