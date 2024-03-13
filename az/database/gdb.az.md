{
  "date": "2022-05-08",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDB Fayl Format - ESRI Fayl Geoməlumatlar Baza Faylı",
  "description": "GDB fayl formatı və GDB fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "GDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-gd-azb"
}
},
  "lastmod": "2022-05-08"
}

## GDB faylı nədir?

ESRI faylı Geoməlumatlar bazası (FileGDB) diskdəki qovluqda xüsusiyyət verilənlər dəsti, xüsusiyyət sinifləri və əlaqəli cədvəllər kimi əlaqəli coğrafi məlumatları saxlayan fayllar toplusudur. Onun işləməsi üçün .gdb faylı ilə yanaşı, eyni qovluqda saxlanması üçün müəyyən digər faylları tələb edir. Məkan, eləcə də qeyri-məkan məlumatları idarə etmək üçün sorğular .gdb faylında icra edilə bilər.

## GDB Fayl Format - Ətraflı Məlumat

Fayl geoməlumat bazaları yeddi sistem cədvəlindən və istifadəçi məlumatlarından ibarətdir. İstifadəçi məlumatları aşağıdakı məlumat dəstlərində saxlanıla bilər:

* Xüsusiyyət sinfi

* Xüsusiyyət verilənlər toplusu

* Mozaika məlumat dəsti

* Raster kataloqu

* Raster verilənlər toplusu

* Sxematik verilənlər toplusu

* Cədvəl (məkansız)

* Alət qutuları


Xüsusiyyət verilənlər dəstləri xüsusiyyət sinifləri ilə yanaşı, aşağıdakı məlumat dəstlərini ehtiva edə bilər:

* Qoşmalar

* Xüsusiyyətlə əlaqəli annotasiya

* Həndəsi şəbəkələr

* Şəbəkə verilənlər bazası

* Parsel parçaları

* Münasibət dərsləri

* Ərazilər

* Topologiyalar


Fayl geoməlumat bazalarında verilənlər dəstlərinin standart maksimum ölçüsü 1 TB-dir. Böyük verilənlər dəstləri (adətən raster) üçün maksimum ölçü 256 TB-ə qədər artırıla bilər. Bu, konfiqurasiya açar sözü ilə idarə olunur. Əlavə məlumat üçün fayl geoməlumat bazaları üçün Konfiqurasiya açar sözlərinə baxın.

Fayl geoməlumat bazaları həmçinin alt tipləri və domenləri ehtiva edə bilər və checkout/check-in replikasiyasında və birtərəfli replikalarda iştirak edə bilər.

Fayl geoməlumat bazasına eyni vaxtda bir neçə istifadəçi daxil ola bilər. İstifadəçilər redaktə edirsə, müxtəlif verilənlər bazalarını redaktə etməlidirlər.

## GDB Fayl Formatının Xüsusiyyətləri ##

Fayl GDB ESRI mülkiyyət formatıdır və onun spesifikasiyası ictimaiyyətə açıq deyil. Bu səbəbdən, FIle GDB üçün fayl formatı təfərrüatları bunu tərs mühəndisliklə [partially](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) etmiş bəzi mənbələrdən başqa heç bir yerdə sənədləşdirilə bilmədi.

## İstinadlar ##

* [FGDB Spesifikasiyaları](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)


