{
  "date": "2023-07-12",
  "keywords": [
"exp",
"exp faylı",
"exp mpeg faylı nədir",
"exp faylını necə açmaq olar",
"fayl",
"exp fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "EXP Fayl Format - Simvollar İxrac Faylı",
  "description": "EXP faylları yarada və aça bilən EXP formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "EXP",
  "menu": {
    "docs": {
      "identifier": "programming-exp-az",
      "parent": "programming"
}
},
  "lastmod": "2023-07-12"
}

## EXP faylı nədir?

Simvolların ixrac faylı mənasını verən EXP faylı inteqrasiya olunmuş inkişaf mühiti (IDE) və ya kompilyator tərəfindən yaradılır. Bu fayl ixrac edilmiş məlumat və funksiyalara aid ikili detallardan ibarətdir. Onun məqsədi ikisini bir-birinə bağlamağa kömək etməklə mənşəli proqram ilə başqa bir proqram arasında əlaqə yaratmaqdır. EXP faylları müxtəlif proqram proqramları arasında qüsursuz inteqrasiya və əməkdaşlığın asanlaşdırılmasında mühüm rol oynayır.

## EXP Fayl Format - Ətraflı Məlumat

Proqram həm məlumatların idxalı, həm də ixracı ilə başqa proqramla qarşılıqlı əlaqə yaratmalı olduqda, idxal kitabxanasından və ixrac faylından istifadə edərək əlaqə yaratmaq lazımdır. Bu əlaqə proqramlar arasında yarana biləcək dövri idxal asılılıqlarını həll etmək üçün çox vacibdir.

Dairəvi idxal A Proqramı B Proqramından müəyyən məlumat və ya funksiyalardan, B Proqramı da A Proqramından verilənlər və ya funksiyalardan asılı olduqda baş verir. Bu qarşılıqlı asılılıq proqram təminatının işlənməsi prosesinin əlaqələndirilməsi mərhələsində problem yarada bilər.

Dairəvi idxalı həll etmək üçün tipik yanaşma proqramları birləşdirərkən .LIB faylından (import kitabxanası) və EXP faylından (ixrac faylı) istifadə etməyi nəzərdə tutur. LIB faylı A Proqramının B Proqramından tələb olunan məlumat və ya funksiyalara daxil olması üçün lazımi məlumatı təmin edən idxal kitabxanası kimi xidmət edir. Digər tərəfdən, EXP faylı B Proqramının ixrac etdiyi müvafiq simvol məlumatını ehtiva edən ixrac faylı kimi çıxış edir. A proqramı ilə istehlak üçün.

Əlaqələndirmə prosesi zamanı LIB faylı və EXP faylından istifadə etməklə dairəvi idxal asılılıqları həll edilə bilər. A proqramı idxal kitabxanası vasitəsilə Proqram B-dən tələb olunan elementləri uğurla idxal edə bilər və B Proqramı ixrac faylı vasitəsilə A Proqramı tərəfindən əldə ediləcək zəruri simvolları ixrac edə bilər.

## Proqram təminatının hazırlanmasında EXP fayllarının məqsədi və istifadəsi

EXP faylları ilk növbədə proqram təminatının inkişafı ilə bağlıdır və müxtəlif proqramlaşdırma dilləri və inkişaf alətləri ilə birlikdə istifadə olunur. EXP faylları ilə əlaqəli ümumi proqram və alətlərdən bəziləri bunlardır:

- **Tərtibçilər:** GCC (GNU Compiler Collection) və ya Microsoft Visual C++ kimi kompilyator proqramı tərtib prosesinin bir hissəsi kimi EXP faylları yarada bilər. EXP fayllarında əlaqə və sazlamaya kömək edən simvol məlumatı var.
- **Bağlayıcılar:** GNU ld (Linker) və ya Microsoft Linker kimi bağlayıcılar simvol istinadlarını həll etmək və əlaqələndirmə prosesi zamanı müxtəlif kod modulları arasında əlaqə yaratmaq üçün EXP fayllarından istifadə edir.
- **İnteqrasiya edilmiş İnkişaf Mühitləri (İDE-lər):** Visual Studio, Eclipse və ya Xcode kimi IDE-lər çox vaxt EXP faylları ilə işləmək üçün daxili dəstəyə malikdir. Onlar simvol məlumatlarını idarə etmək, sazlamaq və əlaqələndirmək, pərdə arxasında EXP fayllarından istifadə etmək üçün funksiyalar təmin edir.
- **Debuggers:** GDB (GNU Debugger) və ya WinDbg kimi sazlama alətləri yaddaş ünvanlarını mənbə kodu simvolları ilə əlaqələndirmək üçün EXP fayllarından istifadə edərək tərtibatçılara öz proqramlarını effektiv şəkildə sazlamağa imkan verir.
- **Profillər:** Intel VTune və ya Visual Studio Profiler kimi profilləşdirmə alətləri profilləmə prosesi zamanı performans məlumatlarını xüsusi funksiyalara və ya kod regionlarına uyğunlaşdırmaq üçün EXP fayllarından istifadə edə bilər.

## EXP faylını necə açmaq olar?

Simvol ixrac faylları olan EXP faylları adətən son istifadəçilər tərəfindən birbaşa açılması və ya baxılması üçün nəzərdə tutulmur. Onlar ilk növbədə tərtibatçılar tərəfindən istifadə olunur və tərtib, əlaqələndirmə və sazlama prosesləri zamanı alətlər qurur.

EXP faylları adətən inkişaf alətləri tərəfindən avtomatik işlənir və ya qurma sisteminə inteqrasiya olunur. Onlar simvol istinadlarını həll etmək, yaddaş ünvanlarını mənbə kodu elementləri ilə əlaqələndirmək və kod modullarının əlaqələndirilməsini asanlaşdırmaq üçün tərtibçi, əlaqələndirici, sazlayıcı və ya profilçi üçün istinad kimi xidmət edir.

Əgər siz EXP faylı ilə işləyən tərtibatçısınızsa, adətən faylı əl ilə açmağa və ya onunla əlaqə saxlamağa ehtiyac yoxdur. Bunun əvəzinə, EXP faylını əlaqələndirmə, sazlama və ya profil yaratmaq kimi müvafiq məqsədləri üçün daxildən istifadə edən inkişaf alətlərinə və ya proqramlaşdırma mühitlərinə etibar edərdiniz.

## İstinadlar
* [.Exp Faylları Bağlayıcı Girişi kimi](https://learn.microsoft.com/en-us/cpp/build/reference/dot-exp-files-as-linker-input?view=msvc-170)


