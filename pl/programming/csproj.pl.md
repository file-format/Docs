{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Poznaj format pliku CSPROJ i interfejsy API, które mogą tworzyć i otwierać pliki CSPROJ.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Co to jest plik CSProj?
Pliki z rozszerzeniem CSPROJ reprezentują plik projektu C#, który zawiera listę plików zawartych w projekcie wraz z odniesieniami do zestawów systemowych. Kiedy nowy projekt jest inicjowany w Microsoft VIiuual Studio, otrzymujesz jeden plik .csproj wraz z głównym plikiem rozwiązania ([.sln](/pl/programming/sln/)). Jeśli w projekcie jest więcej niż jeden zestaw, będzie również taka sama liczba plików projektu, gdzie plik .sln łączy je wszystkie razem jako część projektu. Zawartość tego pliku definiuje wszystkie wymagania, które są wymagane do zbudowania projektu, takie jak zawartość do uwzględnienia, wymagania dotyczące platformy, informacje o wersjach, ustawienia serwera WWW lub serwera bazy danych oraz zadania, które należy wykonać. Zawartość pliku projektu jest ułożona w formacie pliku XML i może być otwierana w dowolnym edytorze tekstu w celu edycji lub przeglądania. Zapewnia również logiczny widok plików projektu w celu prawidłowego ułożenia.

## CSPROJ Format pliku #

Deweloperzy mogą samodzielnie tworzyć pliki projektów, przestrzegając [schematu MSBuild XML](https://msdn.microsoft.com/library/5dy88c2e.aspx). Otwarta i przejrzysta struktura plików projektów pozwala twórcom aplikacji narzucić wyrafinowaną i precyzyjną kontrolę nad sposobem tworzenia i wdrażania projektów. Zawartość takiego pliku projektu ma bardzo wyraźny związek między sobą. Poniższy rysunek przedstawia kluczowe elementy i relacje między nimi dla takiego pliku projektu.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

W poniższych sekcjach omówiono elementy formatu pliku dla pliku projektu.

### Element projektu ###

Element [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) jest elementem głównym każdego pliku projektu. Identyfikuje schemat XML dla pliku projektu i może zawierać atrybuty określające punkty wejścia dla procesu kompilacji.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Właściwości i warunki

Właściwości reprezentują informacje niezbędne do zbudowania projektu. Takie właściwości są zdefiniowane w elemencie [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Te właściwości składają się z par klucz-wartość, w których nazwa elementu właściwości definiuje klucz właściwości, a zawartość elementu definiuje wartość właściwości. Można na przykład zdefiniować właściwości o nazwach ServerName i ConnectionString, aby przechowywać statyczną nazwę serwera i parametry połączenia.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Warunki można określić za pomocą elementów w celu określenia kryteriów oceny elementu. Jest to określone słowem warunku podczas definiowania właściwości, jak pokazano poniżej:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Gdy program MSBuild przetwarza tę definicję właściwości, najpierw sprawdza, czy dostępna jest wartość właściwości **$(OutputRoot)**. Jeśli wartość właściwości jest pusta — innymi słowy, użytkownik nie podał wartości tej właściwości — warunek przyjmuje wartość **true**, a wartość właściwości jest ustawiona na **..\Publish\Out.**

### Przedmioty i grupy przedmiotów

Plik projektu definiuje dane wejściowe do procesu kompilacji, które w rzeczywistości są różnymi typami plików. W nomenklaturze MSBuild te dane wejściowe są reprezentowane przez elementy Item i są zdefiniowane w elemencie [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Podobnie jak elementy **Property**, elementowi **Item** możesz nadać dowolną nazwę. Musisz jednak określić atrybut **Include**, aby zidentyfikować plik lub symbol wieloznaczny reprezentowany przez element.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Cele i zadania

Element [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) reprezentuje pojedynczą instrukcję kompilacji (lub zadanie). MSBuild zawiera wiele predefiniowanych zadań. Na przykład:

* Zadanie **Kopiuj** kopiuje pliki do nowej lokalizacji.
* Zadanie **Csc** wywołuje kompilator Visual C#.
* Zadanie **Vbc** wywołuje kompilator Visual Basic.
* Zadanie **Exec** uruchamia określony program.
* Zadanie **Message** zapisuje wiadomość do rejestratora.

Zadania muszą zawsze być zawarte w elementach [Target](https://msdn.microsoft.com/library/t50z2hka.aspx). Element **Target** to zestaw jednego lub więcej zadań, które są wykonywane sekwencyjnie, a plik projektu może zawierać wiele celów.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Bibliografia

* [Zrozumienie pliku projektu — MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

