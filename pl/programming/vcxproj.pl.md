{
  "date" : "2019-10-11",
  "keywords" :["vcxproj", "plik", "rozszerzenie", "format pliku", "Projekt Visual C++", "Przewodnik po programowaniu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Dowiedz się o formacie pliku VCXPROJ i interfejsach API, które mogą tworzyć i otwierać pliki VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Czym jest plik VCXPROJ?

Plik z rozszerzeniem .vcxproj to plik projektu Microsoft Visual C++, który przechowuje informacje o projekcie [C++](/pl/programming/cpp/). Zawiera informacje, które są używane przez system projektu MSBuild do kompilowania i kompilowania ostatecznego wyniku. VCXPROJ projektów Visual C++ jest taki sam jak w przypadku [CSPROJ](/pl/programming/csproj/) dla projektów .NET. Pliki VCXPROJ nie zawierają żadnego kodu, ale odnoszą się do wszystkich klas, celów i właściwości zdefiniowanych dla projektu w celu zbudowania projektu. Można je otworzyć w edytorach zwykłego tekstu lub najlepiej w Microsoft Visual Studio IDE.


## Format pliku VCXPROJ — więcej informacji

Pliki VCXPROJ to pliki tekstowe utworzone w formacie pliku [XML](/pl/web/xml/). Można je otworzyć w dowolnym edytorze tekstu, ale do otwierania i edytowania tych plików zdecydowanie zaleca się korzystanie ze środowiska Microsoft Visual Studio IDE. Nie zostały one zaprojektowane do ręcznej edycji. Błędy mogą spowodować awarię środowiska IDE lub zachowanie w nieoczekiwany sposób.

Zawartość przykładowego pliku VCXPROJ jest następująca.

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
### Elementy pliku VCXPROJ

Typowy plik VCXPROJ zawiera wiele elementów, jak widać w powyższym przykładzie XML. [Struktura VCXPROJ](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) firmy Microsoft szczegółowo wyjaśnia każdy element pliku i można się do niego odnieść z perspektywy dewelopera.

#### Element projektu

To jest węzeł główny pliku VCXPROJ. MSBuild używa tego elementu do odczytywania wersji kompilacji i domyślnego celu kompilacji.

#### Element grupy pozycji konfiguracji projektu

Zawiera informacje o konfiguracji projektu, które mogą obejmować metodę kompilacji (debugowanie lub wydanie), kompilację 32- lub 64-bitową, opcje optymalizacji i inne. Informacje w tej grupie są używane przez IDE do ładowania projektu.

#### Elementy konfiguracji projektu

Elementy ProjectConfiguration w pliku VCXPROJ zawierają informacje o kompilacji i platformie, dla której ładowany jest projekt. Jego nazwa powinna być zgodna z formatem `$(Konfiguracja)|$(Platforma)`.

#### Globalny element PropertyGroup

Ta sekcja zawiera ustawienia, które dostarczają informacji na poziomie projektu, takie jak:

* Przewodnik projektu
* Główna przestrzeń nazw
* ApplicationType lub ApplicationTypeRevision


## Bibliografia

* [Struktura VCXPROJ — MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [Pliki projektu C++](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

