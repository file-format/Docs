{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku PDB - Plik Bazy Danych Programu",
  "description":"Dowiedz się o formacie pliku PDB i interfejsach API, które mogą tworzyć i otwierać pliki PDB.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Czym jest plik PDB?

Plik z rozszerzeniem .pdb to plik bazy danych programu, który zawiera informacje debugowania dla skompilowanego pliku wykonywalnego (EXE/DLL). Pliki PDB są generowane przez Microsoft Compilers, gdy aplikacja jest kompilowana w trybie debugowania. Obecność pliku PDB może pomóc w inżynierii wstecznej pliku wykonywalnego, ponieważ zawiera istotne informacje o wszystkich symbolach modułów. Z tego powodu pliki te są przechowywane oddzielnie od ostatecznego pliku wykonywalnego. [DgbHelp API](https://docs.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) firmy Microsoft może otworzyć plik PDB w celu uzyskania informacji, takich jak informacje publiczne i eksporty, symbole globalne, symbole lokalne, wpisz dane, pliki źródłowe i numery linii.

## Format pliku PDB

PDB jest zastrzeżonym formatem plików firmy Microsoft i nie został jeszcze nigdzie oficjalnie udokumentowany. Jednak dokumentacja początkowa jest dostępna [tutaj](https://github.com/Microsoft/microsoft-pdb) i można się do niej odwoływać.

### Strumienie PDB

Pliki PDB składają się z wielu strumieni, z których każdy działa jako wirtualny pojedynczy plik i zawiera informacje. Twórcy plików PDB mogą zapisywać w tych plikach, a plik jest finalizowany dopiero po wydaniu jawnego zatwierdzenia. Kompilator może nadal zapisywać do pliku PDB, ale zatwierdzać tylko wtedy, gdy cały kod użytkownika skompiluje się pomyślnie. Plik PDB składa się z następujących strumieni:

|Nr strumienia |Zawartość |Krótki opis|
---|---|---|
|1| Pdb (nagłówek) |Informacje o wersji i informacje o połączeniu tego PDB z EXE|
|2| Tpi (menedżer typów) |Wszystkie typy użyte w pliku wykonywalnym.|
|3| Dbi (informacje o debugowaniu) |Przechowuje wkład sekcji i listę „modów”|
|4| NazwaMapa| Przechowuje zaszyfrowaną tablicę łańcuchów|
|4-(n+4)| n Mody (informacje o module)| Każdy strumień modów zawiera symbole i numery linii dla jednej kompilacji|
|n+4| Hash globalnego symbolu| Indeks umożliwiający wyszukiwanie w symbolach globalnych według nazwy|
|n+5| Skrót symbolu publicznego| Indeks umożliwiający wyszukiwanie w symbolach publicznych według adresów|
|n+6| Rekordy symboli| Rzeczywiste zapisy symboli globalnych i publicznych symboli|
|n+7| Wpisz hash| Hash używany przez strumień TPI.|

Każdy strumień w pliku PDB składa się z kilku stron, które niekoniecznie są kolejno numerowane.

### nagłówek PDB

Plik PDB ma nagłówek, który składa się z podpisu do identyfikacji i sprawdzania poprawności określonego formatu. Długość podpisu zależy od formatu PDB. Nagłówek może być dłuższy niż pojedyncza strona.

### Metadane PDB
Metadane PDB są odpowiedzialne za rozpoznawanie wszystkich strumieni składowych, podając długość i kolejność stron dla każdego strumienia. Rozkazy są wydawane strumieniom po kolei; począwszy od 0. Istnieje również nieuporządkowany strumień główny, który zawiera niektóre metadane.

## Bibliografia
* [WPB – Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

