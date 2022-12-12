{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "файл", "разширение", "файлов формат", "Проект на Visual C++", "Ръководство за програмиране" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Научете за файловия формат VCXPROJ и API, които могат да създават и отварят VCXPROJ файлове.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Какво е VCXPROJ файл?

Файл с разширение .vcxproj е проектен файл на Microsoft Visual C++, който съхранява информацията за проекта [C++](/bg/programming/cpp/). Той съдържа информация, която се използва от проектната система MSBuild за компилиране и изграждане на крайния резултат. VCXPROJ на проекти на Visual C++ е същият като този на [CSPROJ](/bg/programming/csproj/) за .NET проекти. VCXPROJ файловете не съдържат никакъв код, но се отнасят до всички класове, цели и свойства, дефинирани за проекта за изграждане на проекта. Те могат да бъдат отворени в редактори с обикновен текст или за предпочитане в Microsoft Visual Studio IDE.


## VCXPROJ файлов формат - повече информация

VCXPROJ файловете са текстови файлове, които са създадени във файлов формат [XML](/bg/web/xml/). Те могат да бъдат отворени във всеки текстов редактор, но е силно препоръчително да използвате Microsoft Visual Studio IDE за отваряне и редактиране на тези файлове. Те не са предназначени за ръчно редактиране. Грешките могат да доведат до срив на IDE или да се държат по неочакван начин.

Съдържанието на примерен VCXPROJ файл е както следва.

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
### VCXPROJ файлови елементи

Типичният VCXPROJ файл съдържа редица елементи, както може да се види в примерния XML по-горе. [VCXPROJ структура](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) от Microsoft обяснява подробно всеки файлов елемент и може да бъде препратен от гледна точка на разработчика.

#### Проектен елемент

Това е основният възел на файла VCXPROJ. MSBuild използва този елемент, за да прочете версията на компилацията и целта по подразбиране за компилация.

#### Project Configurations ItemGroup Елемент

Той съдържа информация за конфигурацията на проекта, която може да включва метода на изграждане (Debug или Release), 32 или 64-битова компилация, опции за оптимизация и други. Информацията в тази група се използва от IDE за зареждане на проекта.

#### Елементи за конфигурация на проекта

Елементите на ProjectConfiguration във файл VCXPROJ съдържат информация за компилацията и платформата, за които е зареден проектът. Името му трябва да следва формата `$(Конфигурация)|$(Платформа)`.

#### Globals PropertyGroup елемент

Този раздел съдържа настройки, които предоставят информация за ниво проект, като например:

* ProjectGuid
* Основно пространство от имена
* ApplicationType или ApplicationTypeRevision


## Препратки

* [VCXPROJ структура - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++ проектни файлове](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

