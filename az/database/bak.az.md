{
  "date": "2020-11-11",
  "keywords": [
"BAK",
"uzadılması",
"fayl",
"fayl formatı",
"BAK fayl növü",
"BAK fayl uzantısı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"Verilənlər Bazasının Faylları"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "BAK faylları yarada və aça bilən BAK fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "BAK Fayl Format - Verilənlər Bazasının Yedek Faylı",
  "linktitle": "BAK",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ba-azk"
}
},
  "lastmod": "2020-12-04"
}

## BAK faylı nədir?

.bak uzantısına malik fayl adətən məlumatların ehtiyat nüsxələrini saxlamaq üçün müxtəlif proqram alətləri tərəfindən istifadə edilən ehtiyat fayldır. Verilənlər bazası nöqteyi-nəzərindən, BAK faylı verilənlər bazasının məzmununu saxlamaq üçün Microsoft SQL Server tərəfindən istifadə olunur. Verilənlər bazası ilə əlaqəli bütün məlumatlar və fayllar bu fayl formatında saxlanılır ki, verilənlər bazası hər hansı səbəbdən korlana və ya etibarsızlaşa bilsin. Ehtiyat faylları təhlükəsizlik məqsədi ilə digər serverlərdə saxlanıla və indeksləşdirilə bilər. Bir neçə proqram SQL Server Management Studio, Transact-SQL və Windows PowerShell kimi BAK faylları yarada bilər.

## BAK fayl formatı

BAK faylının daxili təfərrüatları məlum deyil, lakin geniş şəkildə onun Microsoft Tape Formatına (MTF) əsaslandığı güman edilir. MTF spesifikasiyaları mövcuddur və faylın strukturunu başa düşmək üçün onlara istinad edilə bilər. Sənəd yaddaşın idarə edilməsi əməliyyatları, lent diskləri və fayl sistemləri haqqında ümumi biliyi olan hər kəs üçün MTF yaddaşı haqqında təfərrüatları təqdim edir.

### Məlumat dəstləri

Məlumat toplusu verilənlərin ehtiyat nüsxəsi və ya bərpası zamanı yaddaş daşıyıcısına (lent, optik disk və s.) yazılmış obyektlərin toplusudur. Məlumat dəstləri böyük həcmdə məlumat olduqda çoxlu mediadan ibarətdir.

### MTF-nin Əsas Elementləri

MTF faylı onun tikinti bloklarını təşkil edən bəzi fundamental elementlərdən ibarətdir. Bu elementlər bunlardır:

#### Deskriptor Blokları

Deskriptor blokları (DBLK) formata nəzarət üçün istifadə olunur və MTF faylının əsas əsaslarını təşkil edir. Tək bir MTF faylı hər bir unikal rol üçün çoxlu DBLK müəyyən edir. Hər bir DBLK aşağıdakı dörd hissəyə bölünən dəyişən uzunluqlu məlumat blokudur:

 * `Ümumi Blok Başlığı` - Bütün DBLK-lar üçün ümumi olan sabit uzunluqlu struktur. Bu tələb olunan yeganə Blok Başlığıdır.
 * `DBLK Tip Məlumatı` - Müəyyən edilən DBLK növünə xas olan Sabit Uzunluq bloku
 * `Əməliyyat Sistemi Məlumatları` - DBLK və Əməliyyat sistemlərinin növü əsasında müəyyən edilən xüsusi məlumatlar
 * `DBLK Məlumatı` - Sabit Uzunluqlu DBLK məlumatı ilə yadda saxlanıla bilməyən dəyişən uzunluqlu DBLK spesifik məlumat.

{{< figure src="../bak.png" alt="Microsoft SQL Backup File Format" >}}

#### Məlumat axını

MTF faylındakı məlumat axınları məlumatların inkapsulyasiyası və uyğunlaşdırılması üçün istifadə olunur. O, Axın Başlığından, ardınca Axın Məlumatından ibarətdir. Axın başlığı yalnız bir növ Yayım Məlumatını əhatə edə bilər.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL Yedəkləmə Fayl Format" >}}

#### Fayl İşarələri

Fayl nişanı media daxilində məntiqi ayırma və sürətli çıxış üçün istifadə olunur. Fayl nişanları cihaz sürücüsü tərəfindən və ya istifadə olunan cihaz fayl nişanlarını təmin etmədiyi halda Soft Filemark Deskriptor blokunun istifadəsi ilə təqlid edilir.

## Digər BAK faylları

**.bak** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Verilənlər bazası**
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

**Oyun**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Müxtəlif**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Parametrlər**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## İstinadlar ##

* [[MS-BCP]: Toplu Kopyalama Format](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)


