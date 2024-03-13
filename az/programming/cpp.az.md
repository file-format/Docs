{
  "date": "2019-10-11",
  "keywords": [
"c++",
"fayl",
"uzadılması",
"fayl formatı",
"C++",
"Proqramlaşdırma dili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CPP - C++ Mənbə Kodu Faylı",
  "description": "CPP faylları yarada və aça bilən CPP fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CPP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cp-azp"
}
},
  "lastmod": "2019-09-10"
}

## C++ faylı nədir?

CPP fayl uzantısı olan fayllar C++ proqramlaşdırma dilində yazılmış proqramlar üçün mənbə kodu fayllarıdır. Tək C++ layihəsində proqram mənbə kodu kimi birdən çox CPP faylı ola bilər. Belə bir layihə müxtəlif fayl növlərindən ibarətdir ki, bunlardan CPP faylları başlıq (.h) faylında elan edilmiş metodların bütün təriflərini ehtiva etdiyi üçün icra faylları kimi tanınır. C++ layihəsi bütövlükdə tərtib edildikdə icra edilə bilən proqramla nəticələnir.

## CPP Fayl Strukturu

CPP fayl strukturu başlıq faylları ilə müqayisədə sadədir. Belə bir icra faylının əsas məqsədi interfeysi tətbiqdən ayırmaqdır. Bu, başlıq faylındakı bütün üzv funksiyaların bəyannaməsi və onların CPP faylı daxilində təfərrüatları ilə nəticələnir. CPP tətbiq faylı ərizə yazmaq üçün sadə fayl və ya sinif tətbiqi kimi istifadə edilə bilər.

### Müstəqil icra

Müstəqil proqram kimi istifadə edildikdə CPP faylı başlıq faylında metod bəyannaməsi tələb edilmədən daxilindəki bütün tətbiqləri ehtiva edə bilər. Belə bir icra, tətbiqin girişinin arqument kimi isteğe bağlı istifadəçi daxiletməsini qəbul edən əsas metodla idarə olunduğu icra faylında müəyyən edilmiş bütün üsullardan ibarətdir. O, həmçinin C++ Standart Kitabxanasından faylda elan edilmiş hər hansı metodlar tərəfindən istifadə ediləcək hər hansı kitabxanaları daxil edə bilər.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Sinif Tətbiqi

Obyekt yönümlü proqramlaşdırmada (OOP) CPP faylı sinif tərifi kimi istifadə olunur. Bu halda, bütün sinif verilənləri üzvləri və üzv funksiyaları başlıq faylında elan edilir. Hər bir başlıq faylı öz növbəsində standart kitabxana metodlarına istinad edə bilər. Sinif tərifi CPP faylı faylın əvvəlində daxil olan ifadədəki başlıq faylına istinad edir. Əsasən, proqram tərtibatçıları faylın faktiki məzmunu, müəllif təfərrüatları və icra tarixi haqqında məlumat verən belə bir sinif tətbiqi faylının başlanğıcına şərhlər daxil edirlər. Belə hallarda başlıq icra faylları eyni adlara malik olmalıdır. Belə bir başlıq və icra faylının nümunəsi aşağıdakı kimidir.

### Başlıq Faylı

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### CPP İcra Faylı

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## İstinadlar

* [Sinif Tətbiqi - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Class_implementation_file)


