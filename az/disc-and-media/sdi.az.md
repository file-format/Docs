{
  "date": "2021-08-13",
  "keywords": [
"sdi faylı",
"sdi fayl formatı",
"sdi faylı nədir",
"fayl",
"sdi nümunəsi",
"sdi fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "SDI fayl formatı və SDI faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "SDI - Windows Sistemi Yerləşdirmə Şəkil Faylı",
  "linktitle": "SDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-sd-azi"
}
},
  "lastmod": "2021-08-13"
}

## SDI faylı nədir?
.sdi uzantısı olan faylda yükləmə blob, açılış blob və hissə blob var; Windows Embedded Studio tərəfindən Windows-u yükləmək və quraşdırmaq üçün RAM diskləri və ya yükləmə diskləri yaratmaq üçün adətən istifadə olunur. SDI, System Deployment Image üçün qısaldılmışdır. Windows Embedded Studio Windows üçün disk şəkilləri yaratmaq üçün istifadə olunan proqramdır. Əslində bu proqram SDI Fayl Meneceri proqramı və **sdimgr.exe** adlı əmr xətti alətini ehtiva edir, hər ikisi SDI şəkillərini yerləşdirmək, yaratmaq və redaktə etmək üçün istifadə edilə bilər.

## SDI fayl formatı
SDI fayl formatı sistemin yüklənməsi üçün virtual diskdən istifadə etmək üçün geniş istifadə olunur. Microsoft Windows-un bəzi versiyaları SDI faylını yaddaşa yükləmək və sonra ondan yükləmək üçün vacib olan **RAM yüklənməsini** aktivləşdirir. SDI fayl formatı həmçinin PXE (Preboot Execution Environment) istifadə edərək şəbəkə yüklənməsini təmin edir. O, həmçinin sabit disk təsviri üçün istifadə olunur.
### SDI fayl bölmələri
SDI faylının özü aşağıdakı bölmələrə bölünə bilər:
- **Boot BLOB**: Bu, əsl yükləmə proqramı olan STARTROM.COM-u ehtiva edir. Bu, sabit diskin açılış sektorunun analoqudur.
- **Load BLOB**: Bu adətən NTLDR ehtiva edir və açılış BLOB tərəfindən işə salınır.
- **BLOB Hissəsi**: Bu, faktiki yükləmə müddətini ehtiva edir; boot.ini və ntdetect.com faylları da daxildir ki, bunlar icra müddətinin kök qovluğunda yerləşməlidir.
- **Disk BLOB**: Bu, MBR ilə başlayan düz HDD şəklidir. Yükləmə əvəzinə sabit diskin təsviri üçün istifadə olunur. Həmçinin yalnız Disk BLOB-ları Microsoft-un utilitləri ilə quraşdırmaq olar.


## İstinadlar 

* [Sistem Yerləşdirmə Şəkli - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/System_Deployment_Image)



