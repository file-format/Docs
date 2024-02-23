{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Dowiedz się o formacie pliku DLIS i interfejsach API, które umożliwiają tworzenie i otwieranie plików DLIS.",
  "title" : "Format pliku DLIS — plik danych dziennika studni",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-pl",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Czym jest plik DLIS?

Format pliku .dlis to standardowy format pliku służący do przechowywania i wymiany danych z dzienników odwiertów w przemyśle naftowym i gazowym. Format został opracowany przez komitet ds. standardu danych Logging Industry Data Standard (LIDS) i oznacza Digital Log Information Standard”. Format został zaprojektowany do przechowywania danych dziennika w sposób łatwy do odczytania, zapisu i wymiany między różnymi systemami.

Pliki DLIS zawierają zestaw logicznych rekordów opisujących dane z dziennika odwiertu i jego cechy, takie jak rodzaj danych z dziennika (np. rezystywność, promieniowanie gamma), jednostki miary i lokalizacja danych w odwiercie. Rzeczywiste dane dziennika są przechowywane w oddzielnych plikach binarnych i odnoszą się do nich zapisy logiczne w pliku DLIS.

## Krótka informacja o danych dziennika studni

Dane z dziennika odwiertu to zapis pomiarów przeprowadzonych na różnych głębokościach odwiertu, zwykle podczas procesu wiercenia lub po wierceniu odwiertu. Pomiary te mogą obejmować różne właściwości fizyczne, chemiczne i/lub geofizyczne skały oraz płynów w odwiercie. Oto kilka przykładów danych z dziennika odwiertów:

- Opór elektryczny: miara zdolności skały do przeciwstawienia się przepływowi prądu elektrycznego
- Promień gamma: miara naturalnej radioaktywności skały
- Porowatość: miara ilości otwartych przestrzeni lub porów w skale
- Sonic: miara czasu potrzebnego fali dźwiękowej na przejście przez skałę
- Gęstość: miara masy skały na jednostkę objętości
- Litologia: miara rodzaju lub formacji skalnej

Dane dziennika odwiertów są wykorzystywane do różnych celów w przemyśle naftowym i gazowym, takich jak:

- Identyfikacja lokalizacji i jakości utworów węglowodorowych
- Ocena potencjału produkcyjnego odwiertu
- Planowanie i monitorowanie realizacji i stymulacji odwiertu
- Monitorowanie zachowania odwiertu w czasie

## Związek z PPDM

PPDM (Professional Petroleum Data Management) to standard zarządzania danymi dla przemysłu naftowego i gazowniczego, który zapewnia wspólny model danych do zarządzania danymi dotyczącymi odwiertów i produkcji. Model danych PPDM definiuje zestaw standardowych obiektów danych i relacji, które można wykorzystać do organizowania i zarządzania danymi dziennika studni, w tym danymi DLIS.

Model danych PPDM zawiera obiekty danych dotyczące odwiertów i danych produkcyjnych, takie jak odwierty, nagłówki odwiertów, dzienniki odwiertów i dane produkcyjne. Obejmuje także relacje między tymi obiektami danych, takie jak relacja między odwiertem a powiązanymi z nim dziennikami odwiertu.

Model danych PPDM zapewnia spójny, zgodny ze standardami branżowymi sposób organizowania danych z odwiertów i zarządzania nimi, w tym danych DLIS. Umożliwia różnym organizacjom udostępnianie i wymianę danych przy użyciu wspólnego modelu danych, poprawiając interoperacyjność danych i zmniejszając koszty integracji danych.

Łączne wykorzystanie modelu danych PPDM i danych DLIS umożliwia przechowywanie i zarządzanie danymi dziennika w sposób zgodny ze standardami branżowymi i łatwo dostępny dla innych systemów i aplikacji.


