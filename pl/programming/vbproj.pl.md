{
  "date" : "2019-10-11",
  "keywords" :["vbproj", "plik", "rozszerzenie", "format pliku", "Plik projektu VB", "Przewodnik programowania"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Poznaj format pliku VBPROJ i interfejsy API, które mogą tworzyć i otwierać pliki VBPROJ.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Czym jest plik VBPROJ?

Plik z rozszerzeniem .vbproj to plik projektu Microsoft Visual Basic, który jest używany przez silnik MSBuild firmy Microsoft do budowania projektów w rozwiązaniu Visual Studio. Jest podobny do pliku [CSPROJ](/pl/programming/csproj/) dla projektów .NET napisanych w [C#](/pl/programming/cs/). Silnik MSBuild odczytuje informacje zawarte w różnych grupach z plików VBPROJ i generuje plik wyjściowy. Plik VBPROJ może zawierać informacje związane z globalnymi identyfikatorami, klasami i właściwościami definiującymi projekt. Pliki VBPROJ można otwierać i edytować za pomocą Microsoft Visual Studio i dowolnego popularnego edytora tekstu, takiego jak Notatnik w systemach operacyjnych Windows i MacOS.

## Format pliku VBPROJ — więcej informacji

Pliki VBPROJ to pliki tekstowe zapisane w formacie [XML](/pl/web/xml/) opartym na [schemacie MSBuild XML](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild- plik-schematu-referencji-pliku projektu?view=vs-2019). Plik VBPROJ zawiera informacje w postaci znaczników XML, które definiują informacje związane z tą konkretną grupą ustawień. Zdecydowanie zaleca się otwieranie i edytowanie tych plików ustawień w środowisku Microsoft Visual Studio IDE.

### Elementy VBPROJ

Elementy składowe pliku ustawień VB są pokazane na poniższym obrazku.

{{< figure src="../vbproj.png" alt="Format pliku VBPROJ" >}}

Poniższa tabela zawiera krótki opis tych elementów.

|Element|Opis|
---|---|
|Projekt| Element główny każdego pliku projektu i może zawierać atrybuty określające punkty wejścia dla procesu budowania oprócz identyfikowania schematu XML dla pliku projektu|
|Właściwości i warunki| Właściwości składają się z par klucz-wartość i są zdefiniowane w elemencie PropertyGroup. Nazwa elementu właściwości reprezentuje klucz właściwości, a zawartość elementu określa wartość właściwości.|
|Elementy i grupy elementów|Elementy w pliku projektu to dane wejściowe do procesu budowania, takie jak pliki z kodem, pliki konfiguracyjne, pliki poleceń i inne wymagane w ramach procesu budowania. Elementy są i muszą być zdefiniowane w elemencie ItemGroup.|
|Cele i zadania| Element Task reprezentuje pojedynczą instrukcję kompilacji (lub zadanie). MSBuild zawiera wiele predefiniowanych zadań, takich jak kopiowanie, CSC, VBC, Exec. Zadania muszą zawsze być zawarte w elemencie `Target`, który jest zestawem jednego lub więcej zadań wykonywanych sekwencyjnie, a plik projektu może zawierać wiele celów.|

## Bibliografia

* [Zrozumienie pliku projektu](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [Elementy schematu MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

