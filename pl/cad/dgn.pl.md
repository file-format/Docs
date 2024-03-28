{
  "date" : "2020-01-12",
  "keywords" :["DGN", "Plik", "Format", "Otwórz", "Odczyt", "API", "MicroStation", "Intergraph Interactive Graphics Design System"],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN — format pliku projektu MicroStation CAD",
  "description" :"Poznaj format plików DGN i interfejsy API, które mogą tworzyć i otwierać pliki DGN.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Czym jest plik DGN?

Plik z rozszerzeniem .dgn (Projekt) to plik rysunku utworzony i obsługiwany przez aplikacje CAD, takie jak MicroStation i Intergraph Interactive Graphics Design System. Służy do tworzenia i zapisywania projektów projektów budowlanych, takich jak autostrady, mosty i budynki. Format jest podobny do formatu pliku [DWG](/pl/cad/dwg/) firmy Autodesk i jest uważany za jego konkurenta. Pliki DNG można zapisywać w formacie Intergraph Standard File Format lub V8 DGN. DGN można przekonwertować na kilka innych formatów, takich jak DWG, [BMP](/pl/image/bmp/), [JPEG](/pl/image/jpeg/), [PDF](/pl/pdf/), [GIF](/pl/image/gif/) i inne. Można go otworzyć za pomocą Autodesk AutoCAD, Bentley View i Bentley Systems MicroStation, a także innych aplikacji, takich jak wersje Corel PaintShop Photo Pro i IMSI TurboCAD Deluxe.

## Format pliku V8 DGN

Plik MicroStation V8 DGN składa się z co najmniej jednego modelu. Model to pojemnik na elementy. V8 DGN usuwa wszystkie ograniczenia związane z formatami plików, które występowały w poprzednich wersjach MicroStation. Poniżej znajduje się lista ulepszeń w formacie pliku DGN.

* Usunięto ograniczenie liczby poziomów w pliku DGN, a każdy poziom ma nazwę i jest przechowywany jako element.
* Maksymalny fizyczny rozmiar pliku DGN nie ma żadnych ograniczeń i jest ograniczony tylko przez system operacyjny (np. limit NT wynosi 4 GB)
* Maksymalny rozmiar pojedynczego elementu to 128 KB.
* Nie ma ograniczeń co do maksymalnego rozmiaru komórki.
* Nazwy komórek są ograniczone do około 500 znaków.
* Nie ma ograniczeń co do liczby odniesień, które można dołączyć do pliku DGN.
* Ciąg linii, kształt lub krzywa punktowa może mieć do 5000 wierzchołków.
* Nie ma ograniczeń co do liczby elementów w złożonym łańcuchu lub złożonym kształcie.
* Nie ma ograniczeń co do liczby grup graficznych w pliku DGN.
* Płot jest równoległy do widoku, w którym jest umieszczony.
* Pojedynczy wiersz tekstu może zawierać 65 535 znaków.
* Nie ma ograniczeń co do maksymalnego rozmiaru węzła tekstowego.
* Nie ma ograniczeń co do liczby węzłów tekstowych w pliku DGN.
* Każdy element ma unikalny 64-bitowy identyfikator, który nie zmienia się przez cały cykl życia elementu.
* Każdy element ma znacznik czasu, który wskazuje czas ostatniej zmiany.

## Bibliografia

* [DNG – z Wikipedii](https://en.wikipedia.org/wiki/DGN)
* [Format pliku MicroStation V8 DGN](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

