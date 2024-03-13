{
  "date": "2020-03-16",
  "keywords": [
"DWG",
"Fayl Format",
"CAD",
"Açıq",
"Yaradın"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "DWG fayl formatı və DWG fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "DWG fayl formatı",
  "linktitle": "DWG",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dw-azg"
}
},
  "lastmod": "2019-09-10"
}

## DWG faylı nədir?

DWG uzantısı olan fayllar 2D və 3D dizayn məlumatlarını ehtiva etmək üçün istifadə edilən xüsusi ikili faylları təmsil edir. ASCII faylları olan DXF kimi, DWG də CAD (Kompüter Dəstəkli Dizayn) çertyojları üçün ikili fayl formatını təmsil edir. O, CAD fayllarının məzmununu təmsil etmək üçün vektor şəkli və metadata ehtiva edir. Autodesk-in pulsuz DWG TrueView kimi Windows Əməliyyat Sistemində DWG fayllarına baxmaq üçün pulsuz izləyicilər mövcuddur. DWG fayllarına çatmağı dəstəkləyən digər üçüncü tərəf proqramları da var. DWG faylları istifadəçi tərəfindən yaradılmış məlumatları ehtiva edir və bunlara daxildir:

* Dizaynlar

* Həndəsi məlumatlar

* Xəritələr və fotoşəkillər


Bu format memarlar, mühəndislər və dizaynerlər tərəfindən müxtəlif dizayn məqsədləri üçün geniş istifadə olunur.

## Qısa tarix ##

DWG file format has evolved with the time since its formal introduction in 1982. Tarix nöqteyi-nəzərindən keçmiş hadisələrin qısa icmalı aşağıdakı kimidir.

**1982:** Autodesk 1970-ci ildə Mike Riddle tərəfindən AutoCAD üçün əsas kimi hazırlanmış DWG fayl formatını lisenziyalaşdırmışdır.

**1998:** AutoCAD R14.01-in buraxılması ilə Autodesk proqram tərəfindən yaradılmış DWG fayllarına Autodesk tərəfindən WaterMark adlanan şifrələnmiş yoxlama məbləğini və məhsul kodunu daxil edən DWGCHECK adlı funksiya vasitəsilə fayl yoxlamasını əlavə etdi.

**2006:** Autodesk, DWG fayllarına Autodesk DWG. Bu fayl Autodesk tətbiqi və ya Autodesk lisenziyalı tətbiqi tərəfindən sonuncu dəfə saxlanılan Etibarlı DWG-dir mətn sətirini daxil etmək üçün TrustedDWG texnologiyasını daxil etmək üçün AutoCAD 2007-ni dəyişdirdi. Bunun məqsədi Autodesk proqram istifadəçilərinə bu faylların Autodesk və ya RealDWG tətbiqi tərəfindən yaradılmasını təmin etməkdə kömək etmək idi ki, bu da mütləq uyğunsuzluq riskini azaltmağa kömək etməlidir.

## Fayl strukturu ##

DWG bir sıra proqramlar tərəfindən geniş istifadə olunan fayl formatlarından biri olmuşdur və möhkəm fayl strukturuna malikdir. DWG ikili fayl formatı olduğundan, sadə ASCII [DXF](/cad/dxf/) fayl formatı kimi insanlar tərəfindən oxuna bilməz. DWG faylları adətən şəkil koordinatları və onunla əlaqəli hər hansı metadata haqqında məlumatları ehtiva edir. Tam [specifications](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) DWG fayl formatı OpenDesign tərəfindən endirilə bilər. DWG fayl formatının fayl strukturu aşağıdakı kimi ümumiləşdirilir.

**Başlıq**: Fayl başlığı DWG Başlıq dəyişənlərindən və xətanın aşkarlanması üçün istifadə edilən Cyclic Redundancy Check (CRC) haqqında məlumatdan ibarətdir. Hər bir alt bölmə müxtəlif etiketləri təmsil etmək üçün müxtəlif uzunluqlu bitlərin istifadə edildiyi xüsusi vektordur. Məsələn, DWG Header dəyişəninin ilk 6 biti versiya sətrini ifadə edir.

**Sinif tərifləri:** DWG faylı xüsusi .dwg faylının məqsədindən asılı olaraq çoxsaylı siniflərdən ibarət ola bilər. Başqalarına əlavə olaraq sinif məlumat sahəsinin sinif metadata ölçüsü, sinif nömrəsi və yoxlama məbləği kimi məlumatlar.

**Şablon**: Bu isteğe bağlıdır və R15 və R15 versiyaları üçün bu bölmə Obyekt Boş Məkan bölməsinin altındadır.

** Doldurma**: Metadata müəyyən sayda baytla əlavə olunur və sonradan əlavə olunur ki, bu da köhnə AutoCAD proqram təminatı versiyalarının yeni DWG fayl formatına uyğun olmasını təmin edir.

**Şəkil Məlumatı**: Bu bölmə üçün metadata xüsusi .dwg növündən asılıdır. R14 və R15 istifadəçiləri üçün bu bölmə isteğe bağlıdır.

**Obyekt Məlumatı**: Obyekt məlumatları mövcud obyektlər siyahısına uyğun gələn cədvəl obyektlərinin tam siyahısından, lüğət yazılarından və s. ibarətdir.

**Obyekt Xəritəsi**: Fayldakı hər bir obyektin yeri faylın bu bölməsində göstərilmişdir. Bu bölmədəki metadataların əksəriyyəti obyektin identifikasiyası və yenidən göstərilməsində rol oynayan fayl tutacaqlarıdır.

**Obyekt Boş Yer**: Bu bölmə bütün istifadəçilər üçün isteğe bağlıdır

**İkinci Başlıq**: DWG faylının sonuna doğru fayl başlığı bölməsinin dublikatı

## İstinadlar ##

* [DWG Fayl Formatının Xüsusiyyətləri](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)

* [DWG Fayl Spesifikasiyası](https://www.scan2cad.com/blog/dwg/file-spec/)

* [DWG - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/.dwg)


