{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik VDISCO - Format pliku dokumentu DISCO Dynamic Discovery",
  "description":"Dowiedz się co to jest plik VDISCO?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## Czym jest plik VDISCO?

Plik VDISCO to plik odnajdywania używany przez Microsoft Visual Studio w jego usługach internetowych. Zawiera informacje o dostępnych usługach internetowych, takie jak ich adresy URL, przestrzenie nazw i metody. Plik VDISCO jest podobny do formatu pliku [DISCO](/pl/web/disco/), ale jest generowany w czasie wykonywania. Jest on przechowywany w aplikacji usługi sieci Web i używany przez program Visual Studio do dynamicznego odnajdywania usług sieci Web i korzystania z nich w projekcie. Pliki VDISCO są używane w połączeniu z plikiem [.asmx](/pl/web/asmx/), który zawiera rzeczywisty kod usługi internetowej.

Możesz otworzyć plik VDISCO w dowolnym edytorze tekstu, takim jak Microsoft Notatnik, Github Atom i Apple TextEdit. Można go również otworzyć w programie Microsoft Visual Studio 2012 i nowszych wersjach, aby z nim pracować.

## Format pliku VDISCO

Plik VDISCO jest zapisywany i hostowany w formacie pliku [XML](/pl/web/xml/), który jest uniwersalnym formatem do tworzenia i publikowania danych. Zawiera adres URL usługi, przestrzenie nazw i metody w standardowych znacznikach XML, gdzie każdy znacznik zawiera odpowiednią wartość swoich informacji.

## Bibliografia

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Wykrywanie usług internetowych](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Przykład C# klasy DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

