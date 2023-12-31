{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Plik MDE - Co to jest plik MDE i jak go otworzyć?",
  "description":"Dowiedz się o formacie pliku MDE i interfejsach API, które umożliwiają tworzenie i otwieranie plików MDE.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-pl-mde"
    }
  },
  "lastmod" : "2023-12-03"
}

Czym jest plik MDE?

Plik .MDE to skompilowana wersja bazy danych programu Access (.mdb lub .accdb). Po skompilowaniu bazy danych programu Access do pliku .MDE nie można jej już edytować przy użyciu standardowych narzędzi do projektowania programu Access. Podstawowym celem tworzenia pliku .MDE jest dystrybucja aplikacji bazodanowej bez ujawniania oryginalnego kodu źródłowego.

## Format pliku MDE

Plik MDE tworzony jest poprzez kompilację kodu VBA, formularzy, raportów i innych obiektów. Powoduje to utworzenie pliku binarnego w formacie MDE. Powstały plik .MDE można rozesłać użytkownikom, którzy mogą uruchamiać aplikację, ale nie mogą modyfikować projektu ani przeglądać oryginalnego kodu. Plik MDE jest w rzeczywistości skompilowaną wersją [pliku .MDA](/database/mda/). Dystrybucja plików .MDE może pomóc chronić własność intelektualną, uniemożliwiając użytkownikom dostęp do kodu źródłowego lub jego modyfikowanie. Może również zwiększyć wydajność podczas kompilowania i optymalizacji kodu.

## Bibliografia

* [Specyfikacje dostępu](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Nieoficjalny przewodnik MDB] (http://jabakobob.net/mdb/)