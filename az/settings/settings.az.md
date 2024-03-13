{
  "date": "2023-03-29",
  "keywords": [
"parametrlər faylı",
"parametrlər faylı nədir",
"fayl",
"parametrlər fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SETTINGS Fayl Format - Visual Studio Parametrlər Faylı",
  "description": "SETTINGS faylları yarada və aça bilən SETTINGS formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "SETTINGS",
  "menu": {
    "docs": {
      "identifier": "settings-settings-az",
      "parent": "settings"
}
},
  "lastmod": "2023-03-29"
}

## SETTINGS faylı nədir?

Visual Studio-da .settings faylı proqram parametrlərini ehtiva edən fayldır və müəyyən bir layihə və ya həll üçün istifadəçi seçimlərini və konfiqurasiya məlumatlarını saxlamaq üçün istifadə edilə bilər. Bu parametrlərə şrift ölçüləri, pəncərə düzeni, standart layihə parametrləri və digər konfiqurasiya seçimləri kimi şeylər daxil ola bilər. .settings faylı adətən layihə yaradıldıqda və layihə qovluğunda Properties adlı qovluqda saxlandıqda avtomatik olaraq Visual Studio tərəfindən yaradılır. Faylın özü layihə üçün müxtəlif parametrləri və dəyərləri müəyyən edən elementlər və atributlar dəstindən ibarət XML faylıdır.

Tərtibatçılar həmçinin layihələr və onlara aid həllər üçün xüsusi .settings faylları yarada bilərlər ki, bu da onların tətbiqinə xas olan əlavə konfiqurasiya məlumatlarını saxlamaq üçün istifadə edilə bilər. Bu xüsusi .settings faylları Visual Studio IDE istifadə edərək və ya .NET-də ConfigurationManager sinifindən istifadə edərək kod vasitəsilə əldə edilə və dəyişdirilə bilər. Visual Studio-dakı .settings faylı IDE-nin konfiqurasiya sisteminin mühüm hissəsidir və tərtibatçılara öz layihələri daxilində proqram parametrlərini və üstünlüklərini saxlamaq və idarə etmək üçün bir yol təqdim edir.

## SETTINGS Fayl Format - Ətraflı Məlumat

The .settings file consists of several sections each containing one or more settings. Each setting is defined by a name and a value, including other attributes e.g. description or default value.

.settings faylının əsas xüsusiyyətlərindən biri odur ki, o, tərtibatçılara güclü şəkildə yazılmış parametrlər yaratmağa imkan verir, bu o deməkdir ki, hər bir parametrin xüsusi məlumat növü var və koddan istifadə etməklə daxil olmaq və manipulyasiya etmək olar. Bu, tərtibatçılara mürəkkəb kod yazmadan və ya konfiqurasiya fayllarını əl ilə idarə etmədən proqram parametrlərini asanlıqla saxlamağa və əldə etməyə imkan verir.

Visual Studio, tərtibatçılara qrafik interfeysdən istifadə edərək layihələri üçün parametrlər yaratmağa və idarə etməyə imkan verən Parametrlər Dizayner alətini təqdim edir. Alət parametrlərə daxil olmaq və onları dəyişdirmək üçün lazımi kodu yaradır və tərtibatçıların onlardan öz kodlarında istifadə etmələrini asanlaşdırır.

Defolt .settings faylına əlavə olaraq, tərtibatçılar öz layihələri üçün fərdi parametrlər faylları da yarada bilərlər. Bu fayllar qoşulma sətirləri, API açarları və ya digər həssas məlumatlar kimi tətbiqlərinə xas olan əlavə konfiqurasiya məlumatlarını saxlamaq üçün istifadə edilə bilər. Bu məlumatı qorumaq üçün tərtibatçılar Data Protection API (DPAPI) istifadə edərək fərdi parametrlər fayllarını şifrələyə bilər, bu, hətta fayla təhlükə yaransa belə, məlumatların təhlükəsizliyini təmin edir.

## İstinadlar
* [Visual Studio](https://en.wikipedia.org/wiki/Visual_Studio)


