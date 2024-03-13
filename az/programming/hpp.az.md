{
  "date": "2023-06-08",
  "keywords": [
"hpp faylı",
"hpp faylı nədir",
"hpp faylında nə var",
"hpp fayl nümunəsi",
"hpp faylının formatı nədir",
"fayl",
"hpp fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "HPP Fayl Format - C++ Başlıq Faylı",
  "description": "HPP faylları yarada və aça bilən HPP formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp-az",
      "parent": "programming"
}
},
  "lastmod": "2023-06-08"
}

## HPP faylı nədir?

.hpp fayl formatı adətən C++ proqramlaşdırma dilində başlıq faylları üçün istifadə olunur. Başlıq faylları adətən C++ layihəsində digər mənbə kodu faylları tərəfindən istifadə olunan funksiyaların, siniflərin, dəyişənlərin və sabitlərin bəyannamələrini və təriflərini ehtiva edir.

Başlıq fayllarından istifadənin məqsədi kodun özünü təkrarlamadan çoxlu mənbə kodu faylları arasında ümumi kodu paylaşmaq üçün bir yol təmin etməkdir. C++ mənbə faylının başlıq faylından bəyannamələrə və ya təriflərə daxil olması lazım olduqda, o, `#include` preprosessor direktivindən istifadə edərək başlıq faylını ehtiva edir.

.hpp fayl uzantısı tez-tez faylın C++ başlıq faylı olduğunu göstərmək üçün istifadə olunur. Başlıq faylları üçün bu xüsusi uzantıdan istifadə etmək tələb olunmur və siz .h və ya digər uzantıları olan başlıq fayllarına da rast gələ bilərsiniz. Uzatma seçimi əsasən konvensiya və şəxsi üstünlük məsələsidir.

C++ mənbə faylına `#include` istifadə edərək başlıq faylı daxil olduqda, kompilyator onu vahid kimi tərtib etməzdən əvvəl başlıq faylının məzmununu mənbə faylı ilə effektiv şəkildə birləşdirir. Bu, mənbə fayla başlıq faylındakı bəyannamələrə və təriflərə daxil olmaq imkanı verir, tərtibçiyə növ yoxlaması və kod yaratmaq üçün lazımi məlumatları təmin edir.

## HPP faylında nə var?

.hpp faylında tapa biləcəyiniz bəzi ümumi məzmunlar bunlardır:

- **Funksiya bəyannamələri:** Başlıq faylları çox vaxt onların faktiki icrası olmadan funksiya bəyannamələrini ehtiva edir. Bu bəyannamələr funksiyanın adı, qaytarma növü və parametrləri haqqında məlumat verir, digər mənbə kodu fayllarına icra detallarını bilmədən funksiyadan istifadə etməyə imkan verir.
- **Sinif bəyannamələri:** Başlıq faylları sinif adı, üzv dəyişənləri, üzv funksiyaları və giriş spesifikatorları daxil olmaqla, sinif bəyannamələrini ehtiva edə bilər. Sinif bəyannaməsini başlıq faylına daxil etməklə, digər mənbə kodu faylları həmin sinfin obyektlərini yarada və onun üzvlərinə daxil ola bilər.
- **Daimi bəyannamələr:** Başlıq faylları birdən çox mənbə kodu faylları arasında paylaşılması nəzərdə tutulan qlobal dəyişənlər və ya enum dəyərləri kimi sabitləri müəyyən edə bilər. Bu sabitlərə başlıq faylını digər mənbə fayllarına daxil etməklə əldə etmək olar ki, bu da onlara müəyyən edilmiş sabitlərdən istifadə etməyə imkan verir.
- **Növ tərifləri:** Başlıq fayllarında typedef açar sözündən istifadə edən tip tərifləri və ya istifadə açar sözündən istifadə edərək tip ləqəbləri ola bilər. Bu təriflər mövcud növlər üçün yeni adlar yaradır, kodu daha oxunaqlı və davamlı edir.
- **Daxili funksiya tərifləri:** Bəzi hallarda başlıq fayllarında daxili funksiya tərifləri ola bilər. Daxili funksiyalar, ayrıca funksiya kimi çağırılmaq əvəzinə, çağırış yerində genişləndirilən kiçik funksiyalardır. Başlıq faylına daxili funksiya tərifinin daxil edilməsi kompilyatora funksiya çağırışını birbaşa funksiya gövdəsi ilə əvəz etməyə imkan verir, potensial olaraq performansı artırır.

## HPP fayl nümunəsi

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## HPP faylının formatı nədir?

HPP sadə mətn faylıdır, lakin C++ proqramlaşdırma dilinin ümumi qaydalarına və sintaksisinə əməl edir. Budur .hpp faylının ümumi formatı və strukturu:

- **Başlıq qoruyucuları:** Tipik olaraq, .hpp faylı eyni faylın çoxsaylı daxil edilməsinin qarşısını almaq üçün başlıq qoruyucuları ilə başlayır. Buna `#ifndef`, `#define` və `#endif` kimi preprosessor direktivlərindən istifadə etməklə nail olunur. Başlıq qoruyucusu kompilyasiya prosesində faylın məzmununun yalnız bir dəfə daxil olmasını təmin edir.
- **İfadələri daxil edin:** Başlıq qoruyucularından sonra `#include` direktivindən istifadə edərək digər zəruri başlıq fayllarını daxil edə bilərsiniz. Bunlara standart kitabxana başlıqları və ya kodunuz tərəfindən tələb olunan digər fərdi başlıqlar daxil ola bilər.
- **Bəyannamələr və Təriflər:** .hpp faylının əsas məzmunu bəyannamələr və bəzi hallarda siniflərin, funksiyaların, sabitlərin, tip ləqəblərinin və digər elementlərin tərifləridir. Məsələn, siz `class` açar sözündən istifadə edərək sinifləri, onların qaytarılma növündən, adından və parametrlər siyahısından istifadə edən funksiyalardan və `const` açar sözünün ardınca onların növü və adından istifadə edərək sabitləri elan edə bilərsiniz.
- **Inline Funksiya Tərifləri:** Müəyyən hallarda, siz birbaşa .hpp faylına daxili funksiya təriflərini daxil edə bilərsiniz. Daxili funksiyalar adətən sinif gövdəsi daxilində müəyyən edilir, yəni funksiya tərifi onun bəyannaməsi ilə yanaşı daxil edilir. Bu, funksiya tərifini `inline` açar sözü ilə prefiks etməklə edilə bilər.
- **Ad məkanı bəyannamələri:** Əgər kodunuzda ad boşluqlarından istifadə edirsinizsə, onları .hpp faylı daxilində elan edə bilərsiniz. Bu, `namespace` açar sözünün ardınca ad sahəsinin adı və müvafiq kodu ad sahəsi blokuna daxil etməklə həyata keçirilir.

## İstinadlar
* [Başlıq faylları (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


