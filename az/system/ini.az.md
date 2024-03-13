{
  "date": "2021-07-07",
  "keywords": [
"INI",
"uzadılması",
"fayl",
"format",
"sistemi",
"Təşəbbüs",
"kataloq uzantısı",
"proqramlar",
"kompüter",
"tətbiq"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "INI - Başlanğıc Fayl Format",
  "description": "INI faylları yarada və aça bilən INI fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "INI",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-in-azi"
}
},
  "lastmod": "2021-07-07"
}

## INI faylı nədir? ##

INI faylı, çərçivə və qrammatikada atributları təşkil edən xüsusiyyətlər və bölmələr üçün açıq açarları ehtiva edən kompüter proqramları üçün mesaj konfiqurasiya sənədidir. Bu sistem fayl formatı konfiqurasiya sənədləri öz adlarını MS-DOS əməliyyat sisteminin başlanğıc mənasını verən INI kataloq genişlənməsindən alır. Proqram təminatının qurulmasının bu formasını populyarlaşdırdı. Digər proqram proqramlarında olan bir çox proqramlar CONF və [CFG](/system/cfg/) kimi müxtəlif fayl adı əlavələrindən istifadə edir, baxmayaraq ki, format bir çox konfiqurasiya vəziyyətlərində qeyri-rəsmi standart yaratmışdır.

## INI Fayllarının Qısa Tarixi##

Başlanğıcda, Windows-un əsas proqram konfiqurasiya texnikası bölmələrə bölünmüş hər sətirdə bir mühüm cütü olan mətn sətirlərindən ibarət mətn faylı formatı idi. Cihaz drayverləri, şriftlər və işə salma qurğuları hamısı bu formatda saxlanılırdı. Fərdi parametrlər də adətən proqramlar tərəfindən INI fayllarında saxlanılırdı.
Windows 3.1x-ə qədər format 16 bitlik Microsoft Windows platformalarında dəstəklənirdi. Windows 95-dən başlayaraq Microsoft, tərtibatçıları konfiqurasiya üçün INI faylları əvəzinə Windows Reyestrindən istifadə etməyə təşviq etməyə başladı.

## INI Faylı - Fayl Formatının Xüsusiyyətləri

### Açarlar/Xüsusiyyətlər ###

Açar/mülk INI faylının ən əsas elementidir. Bərabər simvol (=) hər bir açarın adını və dəyərini ayırır. Bərabər işarəsinin solunda adın göründüyü yerdir. Bərabər simvol və nöqtəli vergül Windows sistemində təmkinli hərflərdir, ona görə də açarda istifadə edilə bilməz. Dəyərdə istənilən simvol istifadə edilə bilər.

```
name=value
```

### Bölmələr ###

Bölmə şərhi öz sətrində kvadrat mötərizədə ([]) görünür. Bölmə tərifindən sonra bütün düymələr həmin bölmə ilə əlaqələndirilir. Bölmələr ən sonrakı bölmə təyinatında və ya sənədin sonunda bitir; xüsusi bölmənin sonu ayırıcı yoxdur. Bölmələr yığıla bilməz; onlar yalnız bir dəfə adlandırıla bilər və əlaqələndirilməsi tələb olunmur.

```
[section]
a=a
b=b
```

### Dəyişən funksiyalar ###

INI fayl formatının qlobal səviyyədə qəbul edilmiş tərifi yoxdur. Bir çox kompüter proqramları yuxarıda qeyd olunanlara əlavə olaraq funksiyaları ehtiva edir. Aşağıdakı siyahıya hər hansı fərdi proqrama daxil edilə bilən və ya daxil edilməyən bəzi ümumi xüsusiyyətlər daxildir.

* Şərhlər

* Qaçış personajları 

* Dublikat adlar 



## INI Nümunəsi ##

Nümunə INI faylı aşağıdakı kimi görünür:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## İstinad ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


