{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "fișier", "extensie", "format fișier", "Visual C++ Project", "Ghid de programare"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Aflați despre formatul de fișier VCXPROJ și despre API-urile care pot crea și deschide fișiere VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Ce este un fișier VCXPROJ?

Un fișier cu extensia .vcxproj este un fișier de proiect Microsoft Visual C++ care stochează informațiile proiectului [C++](/ro/programming/cpp/). Conține informații care sunt utilizate de sistemul de proiect MSBuild pentru a compila și construi rezultatul final. VCXPROJ al proiectelor Visual C++ este același cu cel al [CSPROJ](/ro/programming/csproj/) pentru proiectele .NET. Fișierele VCXPROJ nu conțin niciun cod, ci se referă la toate clasele, țintele și proprietățile definite pentru proiect pentru a construi proiectul. Acestea pot fi deschise în editori de text simplu sau, de preferință, în Microsoft Visual Studio IDE.


## Format de fișier VCXPROJ - Mai multe informații

Fișierele VCXPROJ sunt fișiere text care sunt create în format de fișier [XML](/ro/web/xml/). Acestea pot fi deschise în orice editor de text, dar este foarte recomandat să utilizați Microsoft Visual Studio IDE pentru deschiderea și editarea acestor fișiere. Acestea nu au fost concepute pentru editare manuală. Greșelile pot face ca IDE-ul să se prăbușească sau să se comporte în moduri neașteptate.

Conținutul unui exemplu de fișier VCXPROJ este după cum urmează.

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
### Elementele fișierului VCXPROJ

Un fișier VCXPROJ tipic conține un număr de elemente, așa cum se poate vedea în exemplul XML de mai sus. [Structura VCXPROJ](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) de la Microsoft explică fiecare element de fișier în detaliu și poate fi referit din perspectiva dezvoltatorului.

#### Element de proiect

Acesta este nodul rădăcină al fișierului VCXPROJ. MSBuild folosește acest element pentru a citi versiunea de compilare și ținta implicită pentru compilare.

#### ProjectConfigurations Element GroupGroup

Conține informațiile de configurare a proiectului care pot include metoda de construire (Debug sau Release), compilare pe 32 sau 64 de biți, opțiuni de optimizare și altele. Informațiile din acest grup sunt folosite de IDE pentru a încărca proiectul.

#### Elemente de configurare a proiectului

Elementele ProjectConfiguration dintr-un fișier VCXPROJ conțin informații despre construcția și platforma pentru care este încărcat proiectul. Numele său ar trebui să urmeze formatul `$(Configuration)|$(Platform)`.

#### Elementul Globals PropertyGroup

Această secțiune conține setări care oferă informații la nivel de proiect, cum ar fi:

* ProjectGuid
* RootNamspace
* ApplicationType sau ApplicationTypeRevision


## Referințe

* [VCXPROJ Structure - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [Fișiere de proiect C++](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

