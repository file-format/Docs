{
   "date":"2023-10-18",
   "keywords":[
"replika",
"cue faylı",
"cue cdrwin replika vərəq faylı",
"cue faylını necə açmaq olar",
"fayl",
"cue fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CUE Fayl Format - CDRWIN Cue Sheet",
   "description":"CUE CDRWIN Cue Sheet fayl formatı və CUE faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
   "linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin-az",
         "parent":"disc-and-media"
}
},
   "lastmod":"2023-10-18"
}

## CUE faylı nədir?

**CDRWIN Cue Sheet** kimi də tanınan **.CUE** faylı adətən BIN və ya ISO formatında audio CD və ya disk şəklinin trekləri və tərtibatı haqqında məlumatları ehtiva edən sadə mətn faylıdır. Bu fayllar tez-tez diskin strukturunu və məzmununu təsvir etmək üçün istifadə olunur, CD yazan proqram təminatı və ya virtual sürücü proqramı orijinal diski dəqiq surətdə çıxarmağa imkan verir.

## CUE faylının nümunəsi

.cue faylının necə görünə biləcəyinə dair bir nümunə:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN Cue Vərəqi

CDRWIN Cue Sheet CDRWIN proqramı tərəfindən istifadə edilən .cue fayl formatının xüsusi variasiyasıdır. CDRWIN CD/DVD yazan və müəllif proqramıdır və onun .cue vərəqləri bu proqram təminatı ilə istifadə üçün nəzərdə tutulmuşdur. Bu .cue vərəqləri CD və ya DVD-ni dəqiq şəkildə yaratmaq və ya yazmaq üçün CDRWIN üçün lazım olan məlumatları ehtiva edir.

CDRWIN Cue Vərəqlərinə xas olan bəzi əsas detallar bunlardır:

1.  **CDRWIN-ə unikal**: CDRWIN-in .cue vərəqləri CDRWIN proqram təminatına xas olan mülkiyyət formatıdır. Onlar standart .cue faylları ilə oxşarlıqları paylaşsa da, onlar CDRWIN-in xüsusiyyətləri və parametrləri ilə işləmək üçün hazırlanmışdır.
    
2.  **İstifadəçi Dostu İnterfeys**: CDRWIN .cue vərəqlərini yaratmaq və redaktə etmək üçün istifadəsi asan interfeys təqdim edir. İstifadəçilər treklər, indekslər, boşluqlar və digər parametrlər haqqında məlumatları istifadəçi dostu şəkildə əlavə edə və ya dəyişdirə bilərlər.
    
3.  **Uyğun Disk Tipləri**: CDRWIN Cue Vərəqləri əsasən məlumat diskləri, audio CD-lər, qarışıq rejimli disklər və sair daxil olmaqla müxtəlif növ CD və DVD-lərin yaradılması üçün istifadə olunur. Bu format istifadəçilərə yaratmaq istədikləri diskin növünü və məzmununu təyin etməyə imkan verir.
    
4.  **Disk Planına Nəzarət**: CDRWIN Cue Vərəqləri diskin tərtibatı və strukturu, o cümlədən trek sırası, fasilə/boşluq parametrləri və istifadəçinin malik ola biləcəyi hər hansı digər xüsusi üstünlüklər üzərində ətraflı nəzarəti təmin edir.
    
5.  **ISO və BIN dəstəyi**: CDRWIN həm ISO, həm də BIN disk təsvir formatları ilə işləyə bilər. .cue vərəqi disk üçün hansı şəkil faylının istifadə olunduğunu, işarələr və təsvir arasında düzgün sinxronizasiyanı təmin edir.
    
6.  **Yandırma və Yırtma**: Bu .cue vərəqləri CDRWIN-dən istifadə edərək diskləri yandırarkən və ya disklərdən trekləri çıxararkən çox vacibdir. Onlar son məhsulun nəzərdə tutulan tərtibat və məzmuna uyğun olmasını təmin etməyə kömək edir.
    
7.  **Yedəkləmə və Bərpa**: CDRWIN istifadəçiləri CD və ya DVD-lərinin ehtiyat nüsxəsini çıxararkən tez-tez .cue vərəqləri yaradırlar. Bu vərəqlər daha sonra diskin məzmununu, o cümlədən trekin tərtibatı və vaxtı bərpa etmək üçün istifadə edilə bilər.

## CUE faylını necə açmaq olar?

CDRWIN Cue Vərəqləri xüsusi olaraq CDRWIN proqramı üçün nəzərdə tutulmuşdur, ona görə də onlar adətən CDRWIN daxilində açılıb istifadə edilmək üçün nəzərdə tutulub.

CUE fayllarını açan və ya istinad edən proqramlar

- CDRWIN
- Smart Projects IsoBuster
- EZB Systems UltraISO

## Digər CUE faylları

Burada **.cue** fayl uzantısından istifadə edən digər fayl növləri var.

**Disk və Media**
- [CUE - Cue Sheet File](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## İstinadlar
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)


