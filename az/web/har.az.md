{
  "date": "2021-07-08",
  "keywords": [
"HAR",
"Fayl",
"Uzatma",
"Fayl Format",
"Fayl uzadılması",
"JSON",
"Arxiv faylı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAR - HTTP Arxiv Fayl Formatı",
  "description": "HAR faylı və HAR faylını yarada və aça bilən API-lərin nə olduğunu öyrənmək üçün fayl formatı bələdçisi.",
  "linktitle": "HAR",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ha-azr"
}
},
  "lastmod": "2021-07-08"
}

## HAR faylı nədir?

.har (HTTP Arxivi) faylı olan fayl [JSON](/web/json/) fayl formatında bir çox brauzerlər (məsələn, Chrome, Safari, IE, Firefox və s.) üzərindən ötürülən sessiya məlumatlarını saxlayan HTTP arxiv faylıdır. Server və müştəri (bu halda istifadəçinin brauzeri) arasında internet üzərindən ötürülən məlumatlar HAR faylında saxlanılan HTTP sorğusu və cavab başlıqlarını ehtiva edir. Bundan əlavə, brauzerdə yüklənmiş veb səhifələr haqqında performans məlumatları haqqında ətraflı məlumat ehtiva edir. HAR faylları Microsoft Windows OS-də Notepad və Apple MacOS-da TextEdit kimi istənilən mətn redaktorunda açıla bilər.

## HAR Fayl Format - Ətraflı Məlumat

HAR faylları populyar JSON formatından istifadə edərək sessiya məlumatlarını düz mətn faylında saxlayır. HAR fayl formatı üçün spesifikasiyalar Dünya Veb Konsorsiumunun (W3C) Veb Performans Qrupu tərəfindən hazırlanmışdır, lakin dərc edilə bilməz. Bununla belə, HTTP əməliyyatları üçün arxiv formatını uğurla müəyyən etdi.

Sorğu və cavab məlumatlarının ötürülməsinə nəzarət etməklə yanaşı, HAR faylları tərtibatçılar tərəfindən veb-brauzerin səhifə yükləmə sürəti, məzmunun yüklənmə müddəti, yüklənmiş məzmun, brauzerdən cavab almaq üçün yerinə yetirilən sorğular və bir çox digər parametrlər baxımından veb brauzerin performansını qeyd etmək üçün istifadə olunur. .

## HAR fayllarından niyə istifadə edilməlidir?

HAR faylları uzun yükləmə müddətlərini, səhifənin göstərilmə vaxtlarını və cavab vaxtlarını qiymətləndirərək veb saytın performansını yaxşılaşdırmaqda faydalı ola bilər. HAR faylları bu cür problemləri tapmaq və performansı yaxşılaşdırmaq üçün veb saytla bağlı hər hansı bir problemi həll etmək üçün təhlil edilə bilər.

## HAR faylını necə yaratmaq olar?

Beləliklə, HAR faylını necə yaratmaq olar? Bu, HAR faylı yaratmaq üçün hansı brauzerdən istifadə etdiyinizdən asılıdır. Bu təlimatda biz Google Chrome brauzeri üçün addımları sadalayırıq. Safari, Firefox və s. istifadə edərək HAR fayllarının yaradılması üsullarını internetdə asanlıqla axtarmaq və izləmək olar.

### Google Chrome istifadə edərək HAR faylı yaratmaq üçün addımlar

Problemlərlə üzləşən veb səhifəsində aşağıdakı addımlar yerinə yetirilə bilər.

 1. Problemin baş verdiyi Google Chrome-da veb səhifəni açın.
 1. Geliştirici alətini açın (elementi yoxlayın).
 1. Fayl qeydinə başlamaq üçün panelin soluna keçin. Bu bölmədə kiçik yuvarlaq qırmızı düymə var.
 1. Brauzerdə saxlanılan hər hansı jurnal qeydlərini silmək üçün Təmizləmə nişanı” üzərinə klikləyin.
 1. İstədiyiniz məzmunu yuxarıda göstərildiyi kimi saxlamaq üçün sağ klikləyin və HAR Faylı kimi Saxla düyməsini basın.

## İstinadlar

* [HAR Fayl Format - Vikipediya](https://en.wikipedia.org/wiki/HAR_(fayl_formatı))


