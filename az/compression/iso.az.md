{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ISO - Disk Şəkil Fayl Formatı",
  "description":"ISO faylları yarada və aça bilən ISO faylı və API nədir.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso-az",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## ISO faylı nədir?

.iso uzantısı olan fayl CD və ya DVD kimi optik diskdəki bütün məlumatların məzmununu təmsil edən sıxılmamış arxiv disk təsvir faylıdır. [ISO-9660](https://www.iso.org/standard/17505.html) standartına əsaslanaraq, ISO təsvir faylı formatı disk məlumatlarını və orada saxlanılan fayl sistemi məlumatlarını ehtiva edir. ISO fayllarının məzmunun dəqiq surətini ehtiva etmə qabiliyyəti onu CD/DVD nüsxələrini yaratmaq üçün mükəmməl fayl növü edir və əsasən quraşdırma üçün yüklənə bilən məlumatları saxlamaq üçün istifadə olunur. Çox vaxt ISO faylları quraşdırma üçün maşını yükləmək üçün yüklənə bilən məzmun kimi USB/CD/DVD-yə yandırılır. ISO fayllarında MIME tipli proqram/x-iso9660-image var.

## ISO fayl formatı

ISO fayl formatı digər konteyner fayl formatlarına bənzəmir, baxmayaraq ki, məlumatların müəyyən edilmiş məzmununu arxivləşdirir. Arxiv məzmunun və fayl sistemi məlumatının dəqiq strukturu ilə ikili fayl kimi yaradılır. ISO fayl formatı [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) tərəfindən aşağıdakı kimi təsvir edilmişdir.

### ISO Faylının Yüksək Səviyyəli Strukturu

Faylın ümumi strukturu aşağıdakılardan ibarətdir:

 * `Sistem Sahəsi` - 32,768 bayt və ISO_9660 tərəfindən istifadə edilmir
 * `Məlumat Sahəsi` - Həcm deskriptorları dəsti və Yol cədvəlləri, kataloqlar və fayllardan ibarətdir

### Həcmi Deskriptor Dəsti

Məlumat sahəsi həcm deskriptor dəsti ilə başlayır, bir və ya daha çox həcm deskriptorları toplusu həcm təsviri dəsti terminatoru ilə başa çatır. Bunlar birlikdə məlumat sahəsi üçün başlıq rolunu oynayır və onun məzmununu təsvir edir (FAT, HPFS və NTFS formatlı disklər tərəfindən istifadə edilən BIOS parametr blokuna bənzər).

Həcm deskriptoru dəsti aşağıda göstərildiyi kimidir.

|Həcmi Deskriptor Dəsti|
---|
|Həcm deskriptoru #1|
|...|
|Həcmin təsviri #N|
|Həcm təsviri dəsti terminatoru|

#### Həcm Deskriptoru

Hər bir həcm deskriptorunun ölçüsü 2048 baytdır və aşağıdakı struktura malikdir:

|Hissə |Növ |İdentifikator |Versiya |Məlumatlar|
---|---|---|---|---|
|Ölçü |1 bayt |5 bayt (həmişə 'CD001') |1 bayt (həmişə 0x01) |2,041 bayt|

## İstinadlar

* [Optik Disk Şəkli - Vikipediya](https://en.wikipedia.org/wiki/Optical_disc_image)

* [Fayl İmzaları](https://www.garykessler.net/library/file_sigs.html)

* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)


