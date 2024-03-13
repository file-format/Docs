{
  "date": "2019-10-11",
  "keywords": [
"vcxproj",
"fayl",
"uzadılması",
"fayl formatı",
"Visual C++ Layihəsi",
"Proqramlaşdırma bələdçisi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCXPROJ",
  "description": "VCXPROJ faylları yarada və aça bilən VCXPROJ fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "VCXPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vcxpro-azj"
}
},
  "lastmod": "2020-09-10"
}

## VCXPROJ faylı nədir?

.vcxproj genişləndirilməsi olan fayl [C++](/programming/cpp/) layihə məlumatını saxlayan Microsoft Visual C++ layihə faylıdır. O, MSBuild layihə sistemi tərəfindən yekun nəticəni tərtib etmək və qurmaq üçün istifadə olunan məlumatları ehtiva edir. Visual C++ layihələrinin VCXPROJ .NET layihələri üçün [CSPROJ](/programming/csproj/) ilə eynidir. VCXPROJ fayllarında heç bir kod yoxdur, lakin layihənin qurulması üçün layihə üçün müəyyən edilmiş bütün siniflərə, hədəflərə və xassələrə istinad edir. Bunlar düz mətn redaktorlarında və ya tercihen Microsoft Visual Studio IDE-də açıla bilər.


## VCXPROJ Fayl Format - Ətraflı Məlumat

VCXPROJ faylları [XML](/web/xml/) fayl formatında yaradılmış mətn fayllarıdır. Bunlar istənilən mətn redaktorunda açıla bilər, lakin bu faylları açmaq və redaktə etmək üçün Microsoft Visual Studio IDE-dən istifadə etmək çox tövsiyə olunur. Bunlar əl ilə redaktə üçün nəzərdə tutulmamışdır. Səhvlər IDE-nin çökməsinə və ya gözlənilməz şəkildə davranmasına səbəb ola bilər.

Nümunə VCXPROJ faylının məzmunu aşağıdakı kimidir.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### VCXPROJ Fayl Elementləri

Tipik bir VCXPROJ faylı yuxarıdakı XML nümunəsində göründüyü kimi bir sıra elementləri ehtiva edir. Microsoft tərəfindən [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) hər bir fayl elementini təfərrüatı ilə izah edir və tərtibatçının nöqteyi-nəzərindən istinad edilə bilər.

#### Layihə Elementi

Bu VCXPROJ faylının kök nodeudur. MSBuild bu elementdən tərtib versiyasını və tərtib üçün standart hədəfi oxumaq üçün istifadə edir.

#### Layihə Konfiqurasiyaları Maddə Qrup Elementi

O, layihənin konfiqurasiya məlumatlarını ehtiva edir ki, bunlara tikinti metodu (Debug və ya Buraxılış), 32 və ya 64-bit kompilyasiya, optimallaşdırma seçimləri və digərləri daxil ola bilər. Bu qrupdakı məlumatlar layihəni yükləmək üçün IDE tərəfindən istifadə olunur.

#### Layihə Konfiqurasiya Elementləri

VCXPROJ faylındakı ProjectConfiguration elementləri layihənin yükləndiyi quruluş və platforma haqqında məlumatları ehtiva edir. Onun adı `$(Konfiqurasiya)|$(Platforma)` formatına uyğun olmalıdır.

#### Qlobal Mülk Qrupu Elementi

Bu bölmədə layihə səviyyəsi üçün məlumat verən parametrlər var, məsələn:

 * ProjectGuid
 * RootNamespace
 * ApplicationType və ya ApplicationTypeRevision


## İstinadlar

* [VCXPROJ Strukturu - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)

* [C++ Layihə Faylları](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)


