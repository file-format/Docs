{
  "date" : "2021-08-16",
  "keywords" :[ "plik nrg", "format pliku nrg", "co to jest plik nrg", "plik", "przykład nrg", "rozszerzenie pliku nrg", "rozszerzenie", "format", "stopka nrg", "plik format nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Poznaj format plików NRG i interfejsy API, które mogą tworzyć i otwierać pliki NRG.",
  "title" :"NRG - Format pliku obrazu dysku",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Czym jest plik NRG?

Format pliku obrazu utworzony przy użyciu dysku optycznego jest uważany za format pliku NRG. Ten format został stworzony przez firmę Nero specjalnie na potrzeby narzędzia Nero Burning Rom. Ten format jest uważany za używany do przechowywania obrazów dysków, ponieważ jest odpowiedni dla tych konkretnych plików. Pliki te mogą mieć postać dokładnej kopii dysku CD lub DVD lub mogą zawierać kilka plików, które można zamontować jako dysk. Inne bardziej popularne formaty plików, takie jak formaty plików [ISO](/pl/compression/iso/), to te, w które te pliki można przekonwertować na niektóre podstawowe narzędzia. Przeważnie pliki NRG służą do tworzenia kopii zapasowych lub kopii niektórych ważnych danych lub dysków.

## Format pliku NRG ##

Ten format pliku został opracowany przez firmę Nero AG jako format obrazu dysku. Miał specyficzną właściwość narzędzia Nero Burning Rom, ponieważ został opracowany do przechowywania obrazów płyt. Jego pierwsza wersja została określona do przechowywania wartości jako 32-bitowych liczb całkowitych. Jednak jego druga wersja została uruchomiona i zawierała obsługę 64-bitowych liczb całkowitych.

## Specyfikacja techniczna ##

Na początku pliku ten format nie przechowuje swoich danych jako nagłówka. Podobnie jak stopka, jest dołączana na końcu pliku. Informacje o obrazie są przechowywane w postaci fragmentów IFF. Przesunięcie pierwszego fragmentu można uzyskać, odczytując stopkę NRG na ostatnich 8 do 12 bajtach pliku. We wszystkich wersjach formatu pliku NRG są dołączone fragmenty, DAOI, tekst CD, typ nośnika informacji o sesji, informacje o dysku, Relo i koniec łańcucha. Kolejność bajtów jest big-endian, a wszystkie wartości całkowite są bez znaku w momencie przechowywania.

### Główne fragmenty ###

#### Zapasowe prześcieradło ####

Ten arkusz cue jest łatwo dostępny we wszystkich wersjach formatu plików NRG. Kawałek **CUEX** oznacza bloki konkatenacji o stałym rozmiarze, a każdy z nich reprezentuje punkt kontrolny.

#### Informacje DAO ####

Informacje te są również obecne we wszystkich wersjach formatu NRG. Fragmenty **DAOI** przechowują odpowiednie szczegółowe informacje w 2 częściach. Jego pierwsza część składa się wyłącznie z danych specyficznych dla sesji. Jego druga część po prostu powtarza szare informacje związane ze śledzeniem i jest to tylko raz dla każdego śladu.

#### Tekst CD ####

Jest to dostępne w drugiej wersji NRG. Kawałek **CDTX** składa się z surowej konkatenacji pakietu CD-text, mającej po 18 bajtów na każdy.

#### Rozszerzone informacje o utworze ####

Jest to dostępne w każdej wersji formatu plików NRG. Te fragmenty są wykorzystywane do przechowywania informacji o śledzeniu dla ścieżki jednoczesnych sesji. Dane te powtarzane są tylko raz w przypadku każdego toru.

#### Informacje o sesji ####

Jest to również dostępne w każdej wersji formatu pliku NRG. Informacje o fragmentach sesji należy wykorzystać do szybkiego przeskanowania obrazu sesji, a następnie zliczenia ścieżek.

#### Koniec łańcucha ####

Kawałek końca oznacza sygnał, że teraz nie ma już żadnych fragmentów do odczytania i jest to również dostępne we wszystkich wersjach NRG.


## Bibliografia ##

* [NRG – z Wikipedii](https://en.wikipedia.org/wiki/NRG_(file_format))


