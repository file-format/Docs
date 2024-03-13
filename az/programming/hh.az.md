{
  "date": "2019-10-11",
  "keywords": [
"h",
".H h",
".hh faylı nədir",
".hh faylını necə açmaq olar",
"uzadılması",
"fayl",
".hh faylı",
".hh fayl formatı",
".hh fayl uzantısı",
".HH Fayl nümunəsi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HH - C++ Başlıq Fayl Formatı",
  "description": "HH faylı yarada və aça bilən HH fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "HH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-azh"
}
},
  "lastmod": "2021-06-20"
}

## HH faylı nədir?

.hh uzantılı fayl dəyişənlərin, sabitlərin və funksiyaların elanını ehtiva edən C++ başlıq faylıdır. Bu bəyannamələr, adətən istifadəçi məntiqinin faktiki icrasını ehtiva edən [.cpp](/programming/cpp/) faylları kimi saxlanılan müvafiq C++ icra faylları tərəfindən istifadə olunur. .hh başlıq fayllarına `#include` direktivindən istifadə edərək həyata keçirmə CPP fayllarında istinad edilir. Layihə səviyyəli bəyannamələri daxil etmək üçün C++ layihənizə mümkün qədər çox başlıq faylı əlavə edə bilərsiniz.

## .HH Fayl Formatı

.hh faylı başlıq faylının tərifi qaydalarını nəzərə alaraq yaradılmış düz mətn faylıdır. .hh faylında elan edilən ən ümumi məlumatlara aşağıdakılar daxildir.

**`Dəyişənlər`** - Obyekt yönümlü proqramlaşdırma (OOP) vəziyyətində, sinif başlıq faylı həyata keçirmə mənbə kodu faylları vasitəsilə əldə edilə bilən bütün sinif səviyyəli dəyişənlərin təriflərini ehtiva edir.
**`Metod Bəyannaməsi`** - Bütün metodlar bəyannamələri çoxsaylı icra faylları arasında əlçatan olmaq üçün .h başlıq fayllarına daxil edilmişdir.
**`Qeyri-sətirli Funksiya Tərifləri`** - Başlıq fayllarında qeyri-sətirli metodların tərifləri də ola bilər.
**`Mesaj Xəritələri`** - MFC mənbə kodunun tətbiqi zamanı başlıq faylında mesaj xəritələri də ola bilər. Bu halda, mesaj xəritələri düymə, onay qutusu, radio düymələri və s. kimi UI elementləri ilə əlaqəli funksionallıq tətbiqi ilə əlaqələndirilir.

## .H və .HH Faylları Arasındakı Fərq

Göründüyü kimi, .h və .hh başlıq faylları arasında müvafiq dillər, yəni [C](/programming/c/) və ya C++ üçün tövsiyə olunan istifadə üsulundan başqa heç bir fərq yoxdur. Başlıq fayllarınızı bu dillərə uyğun adlandırmaq, C və C++ tətbiqlərinin qarışığı ola biləcək böyük bir layihədə bunları ayırd etməyə kömək edir.

Bundan əlavə, başlıqlar genişləndirmə ilə ayrılırsa, redaktorunuz müvafiq olaraq avtomatik olaraq müvafiq formatlaşdırmanı tətbiq edə bilər.

Ümumilikdə, bu iki fayl formatının fərqləndirilməsi heç bir zərər verməyəcək, lakin faydalı olacaq və C və C++ fərqinə riayət etmək tövsiyə olunur.

### Başlıq Mühafizəçiləri

Başlıq faylları digər başlıq fayllarının əlavə edilməsi nəticəsində eyni fayla çoxsaylı bəyannamələrin daxil edildiyi mürəkkəb xətalara səbəb ola bilər. Bu dublikat təriflər kompilyator xətalarını artırır. Bu problemli vəziyyətin qarşısını aşağıda göstərildiyi kimi şərti tərtib direktivləri olan başlıq mühafizəsi adlı mexanizm vasitəsilə almaq olar.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Bu başlıqla preprosessor `ANY_UNIQUE_NAME_HERE_HPP`-nin artıq müəyyən edilib-edilmədiyini yoxlayır. Başlıq təkrar-təkrar eyni fayla daxil edilərsə, başlığın məzmunu nəzərə alınmayacaq.

## İstinadlar

* [Başlıq Filers - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

* [.h və .hh fayl formatları arasındakı fərq](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)


