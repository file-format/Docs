{
  "date" : "2023-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik BROWSER - Format pliku definicji przeglądarki ASP.NET",
  "description":"Dowiedz się o formacie pliku PRZEGLĄDARKA i interfejsach API, które umożliwiają tworzenie i otwieranie plików PRZEGLĄDARKI.",
  "linktitle" : "BROWSER",
  "menu" : {
    "docs" : {
      "parent" : "web",
      "identifier": "web-browser"
}
},
  "lastmod" : "22023-06-06"
}

## Co to jest plik BROWSER?

Plik z rozszerzeniem .browser jest używany przez aplikacje internetowe ASP.NET do określenia możliwości i konfiguracji przeglądarek internetowych. Zawiera informacje o możliwościach, ograniczeniach i cechach przeglądarki. Te cechy pomagają platformie ASP.NET rozpoznać przeglądarkę żądającą i odpowiednio zaprezentować użytkownikom stronę internetową.

## Format pliku PRZEGLĄDARKI

Pliki definicji BROWSER służą aplikacji ASP.NET do określenia możliwości przeglądarki. To informacje zawarte w tym pliku są wykorzystywane przez serwer do generowania znaczników i innych zasobów kompatybilnych z przeglądarką wysyłającą żądanie.

Pliki BROWSER są zapisywane w formacie zwykłego pliku tekstowego. Możesz otworzyć plik BROWSER w edytorach tekstu, takich jak Notatnik, Notepad ++, Apple TextEdit i Visual Studio IDE.

### Struktura pliku w formacie PRZEGLĄDARKI

Pliki definicji PRZEGLĄDARKI mają strukturę hierarchiczną. Każdy plik .browser zawiera znaczniki XML, które obejmują możliwości i funkcje konkretnej przeglądarki lub grupy przeglądarek. Szczegóły te obejmują takie cechy, jak ciąg agenta, numery wersji i obsługę technologii, takich jak JavaScript, CSS i inne elementy HTML. Korzystając z tych plików definicji przeglądarki, programiści ASP.NET dostosowują środowisko użytkownika w oparciu o możliwości różnych przeglądarek.

## Bibliografia

* [Praca z plikami na stronach internetowych ASP.NET](https://learn.microsoft.com/en-us/aspnet/web-pages/overview/data/working-with-files)



