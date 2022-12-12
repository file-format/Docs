{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Dowiedz się o formacie pliku SLN i interfejsach API, które mogą tworzyć i otwierać pliki SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik SLN?
Plik z rozszerzeniem .SLN reprezentuje plik **rozwiązania programu Visual Studio**, który przechowuje informacje o organizacji projektów w pliku rozwiązania. Zawartość takiego pliku rozwiązania jest zapisywana w postaci zwykłego tekstu w pliku i można ją obserwować/edytować, otwierając plik w dowolnym edytorze tekstu. Informacje zawarte w pliku rozwiązania pozostają trwałe i służą do ładowania informacji związanych z rozwiązaniem, takich jak [projekty](/pl/programming/csproj/)i wszelkie inne wymagane informacje. Pliki projektu, do których odwołuje się plik rozwiązania, zawierają dodatkowe informacje umożliwiające środowisku wypełnianie hierarchii elementami tego projektu. Żadne dane nie są przechowywane w pliku .sln, chociaż w razie potrzeby można zapisać informacje o projekcie w pliku .sln.

## **Historia wersji SLN** ##

Wersja formatu rozwiązania ewoluowała z każdym rozwiązaniem Microsoft Visual Studio wraz z upływem czasu. Szczegóły na ich temat są następujące.


|Wersja programu Visual Studio|Wersja formatu rozwiązania
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Zawartość pliku rozwiązania** ###

Plik rozwiązania składa się z kilku sekcji, które są odczytywane przez środowisko w celu załadowania projektu. Poniżej przedstawiono przykładową zawartość pliku .sln.

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

### **Deklaracja projektu** ###

Plik rozwiązania może zawierać więcej niż jedną deklarację projektów, a także różne typy projektów. Na przykład pojedynczy plik rozwiązania może zawierać zarówno projekt CSharp, jak i VB.NET. Te typy są rozróżniane w rozwiązaniu przy użyciu [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Powyższą deklarację projektową można uogólnić w następujący sposób dla jasnego zrozumienia.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID jest unikatowy dla różnych typów projektów i jest używany przez czytelnika rozwiązania do identyfikowania typu projektu. W tym przypadku F184B08F-C81C-45F6-A57F-5ABD9991F28F pokazuje, że jest to projekt VB.NET.

`identyfikator GUID projektu:` unikalny identyfikator GUID projektu, który odróżnia go od innych projektów w rozwiązaniu. Unikalny identyfikator projektu w rozwiązaniu umożliwia innym projektom w rozwiązaniu dostęp do niego.

Na podstawie informacji zawartych w sekcji projektu pliku .sln środowisko ładuje każdy plik projektu. Sam projekt jest wówczas odpowiedzialny za wypełnienie hierarchii projektu i załadowanie wszelkich zagnieżdżonych projektów. Wszelkie zmiany wprowadzone w rozwiązaniu są zapisywane z powrotem w pliku rozwiązania po zapisaniu lub zamknięciu projektu.

## Rozwiązanie Visual Studio VS projekt

**Projekt:** Rozpoczynając tworzenie aplikacji lub oprogramowania przy użyciu programu Visual Studio, rozpoczynasz nowy projekt. Projekt zawiera wszystkie niezbędne pliki, takie jak kod źródłowy, ikony, obrazy, pliki danych i inne, które zostaną skompilowane w wykonywalną aplikację, stronę internetową lub bibliotekę.

**Rozwiązanie:** rozwiązanie zawiera co najmniej jeden projekt. Rozwiązanie jest więc jak kontener dla projektów Visual Studio. Logicznie rzecz biorąc, możemy powiedzieć, że ktoś chce uzyskać kompletne rozwiązanie dla swojej firmy, w tym stronę internetową, aplikację komputerową, usługę zapewniającą spokój i aplikację mobilną.

### **Bibliografia** ###

* [Plik rozwiązania — według MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [identyfikatory GUID typu projektu](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

