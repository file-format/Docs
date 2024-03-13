{
  "date": "2019-10-11",
  "keywords": [
"sln faylı",
"sln faylını necə işə salmaq olar",
"sln",
"uzadılması",
"format",
"sln faylı nədir",
"sln fayl formatı",
"Visual Studio Həlli",
"Visual Studio həlli VS layihəsi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SLN",
  "description": "SLN fayl formatı və SLN fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "SLN",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-sl-azn"
}
},
  "lastmod": "2019-09-10"
}

## SLN faylı nədir?
.SLN uzantılı fayl layihələrin təşkili haqqında məlumatı həll faylında saxlayan **Visual Studio həlli** faylını təmsil edir. Belə bir həll faylının məzmunu faylın içərisində düz mətnlə yazılır və faylı istənilən mətn redaktorunda açmaqla müşahidə etmək/redaktə etmək olar. Həll faylında olan məlumat qalıcı olaraq qalır və [projects ](/programming/csproj/)və istənilən digər tələb olunan məlumat kimi həll ilə əlaqəli məlumatları yükləmək üçün istifadə olunur. Həll faylı tərəfindən istinad edilən layihə faylları iyerarxiyanı həmin layihənin elementləri ilə doldurmaq üçün mühiti təmin etmək üçün əlavə məlumatları ehtiva edir. .sln faylında heç bir məlumat saxlanılmır, baxmayaraq ki, layihə məlumatı tələb olunarsa .sln faylına yazıla bilər.

## **SLN Versiya Tarixçəsi** ##

Həll formatı versiyası hər bir Microsoft Visual Studio həlli ilə zaman keçdikcə təkamül etdi. Bunlarla bağlı təfərrüatlar aşağıdakı kimidir.


|Visual Studio Version|Hol Format Versiyası
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Həll faylının məzmunu** ###

Həll faylı layihəni yükləmək üçün mühit tərəfindən oxunan bir neçə bölmədən ibarətdir. Nümunə .sln faylının məzmunu aşağıda göstərildiyi kimidir.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Layihə Bəyannaməsi** ###

Həll faylı birdən çox layihə bəyannaməsini və fərqli layihə növlərini ehtiva edə bilər. Məsələn, tək bir həll faylı CSharp və VB.NET layihəsini ehtiva edə bilər. Bu növlər [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs) istifadə edərək həlldə fərqləndirilir. Yuxarıdakı layihə bəyannaməsi aydın başa düşülməsi üçün aşağıdakı kimi ümumiləşdirilə bilər.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID müxtəlif layihə növləri üçün unikaldır və layihənin növünü müəyyən etmək üçün həll oxucusu tərəfindən istifadə olunur. Bu halda F184B08F-C81C-45F6-A57F-5ABD9991F28F onun VB.NET layihəsi olduğunu göstərir.

`Layihə GUID:` Həlldəki digər layihələrdən fərqləndirən layihənin unikal GUID-i. Həlldəki layihənin unikal ID-si həlldəki digər layihələrin ona daxil olmasını mümkün edir.

.sln faylının layihə bölməsində olan məlumatlara əsasən, mühit hər bir layihə faylını yükləyir. Layihənin özü daha sonra layihə iyerarxiyasını doldurmaq və hər hansı daxili layihələri yükləmək üçün cavabdehdir. Həlldə edilən hər hansı dəyişiklik layihəni saxladıqdan və ya bağladıqdan sonra yenidən həll faylında saxlanılır.

## Visual Studio həlli VS layihəsi

**Layihə:** Məntiqi olaraq, Visual Studio-dan istifadə edərək proqram və ya proqram yaratmağa başlayanda yeni layihəyə başlayırsınız. Layihə icra edilə bilən proqrama, vebsayta və ya kitabxanaya yığılacaq mənbə kodu, nişanlar, şəkillər, məlumat faylları və s. kimi bütün zəruri faylları ehtiva edir.

**Həll:** Həll bir və ya bir neçə layihədən ibarətdir. Beləliklə, həll Visual Studio layihələri üçün konteyner kimidir. Məntiqlə deyə bilərik ki, kimsə öz biznesi üçün vebsayt, masaüstü proqramı, rahat xidmət və mobil proqram daxil olmaqla tam həll yolu əldə etmək istəyir.

### **İstinadlar** ###

* [Həll Faylı - MSDN tərəfindən](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)

* [Layihə Tipi GUID-lər](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)


