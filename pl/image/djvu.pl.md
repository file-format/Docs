{
  "date" : "2019-10-11",
  "keywords" :["plik djvu", "format pliku djvu", "co to jest plik djvu", "plik", "przykład djvu", "rozszerzenie pliku djvu", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku DJVU",
  "description":"Dowiedz się o formacie plików DJVU i interfejsach API, które mogą tworzyć i otwierać pliki DJVU.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik DJVU?

DjVu, wymawiane jako „déjà vu”, to format pliku graficznego przeznaczony do zeskanowanych dokumentów i książek, zwłaszcza tych, które zawierają kombinację tekstu, rysunków, obrazów i fotografii. Został opracowany przez AT&T Labs. Wykorzystuje wiele technik, takich jak separacja warstw obrazu tekstu i obrazów tła, progresywne ładowanie, kodowanie arytmetyczne i kompresja stratna dla obrazów bitonalnych. Ponieważ plik DJVU może zawierać skompresowane, ale wysokiej jakości kolorowe obrazy, zdjęcia, tekst i rysunki i można go zapisać na mniejszej przestrzeni, dlatego jest używany w Internecie jako książki elektroniczne, podręczniki, gazety, starożytne dokumenty itp.

DjVu można ocenić jako lepszą alternatywę dla [PDF](/pl/pdf/). Rozszerzenia plików związane z DjVu to .DJVU lub .DJV. DjVu może osiągnąć współczynniki kompresji około 5 – 10 lepsze niż istniejące metody, takie jak [JPEG](/pl/image/jpeg/) i [GIF](/pl/image/gif/) dla dokumentów kolorowych i 3 – 8 razy lepsze niż [TIFF]( /image/tiff/) w dokumentach czarno-białych. Zeskanowane dokumenty w rozdzielczości 300 DPI w pełnym kolorze do 25 MB można skompresować do rozmiaru od 30 do 100 KB. Podobnie dokumenty czarno-białe można skompresować do rozmiaru od 5 do 30 KB. Średnia strona HTML może mieć do 50 KB, dlatego dokumenty te można bez problemu przesyłać do sieci.

## Krótka historia ##

Technologia DjVu została opracowana w laboratoriach AT&T przez [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3% A9on_Bottou), Patrick Haffner i Paul G od 1996 do 2001. Format pliku DjVu przeszedł różne wersje, z których ostatnia pochodzi z 2005 roku.


|Wersja|Data wydania|Uwagi
---|---|---|
|1–19|1996–1999|To są wersje rozwojowe.
|20|kwiecień 1999|format pojedynczej strony został zmieniony na format wielostronicowy.
|23|lipiec 2002|fragment CID
|24|lutego 2003|LTAnno fragment
|21|września 1999|Zastąpiono pośredni format przechowywania. Dodano warstwę wyszukiwania tekstowego.
|22|kwietnia 2001|Orientacja strony, kolor JB2
|25|maja 2003|fragment NAVM. Dodano obsługę zakładek DjVu.
|26|kwietnia 2005|Adnotacje tekstowe/wierszowe

## Format pliku DjVu ##

Dokumenty DjVu to pliki IFF85. Struktura zapewnia hierarchię kontenerów, które przechowują informacje w pliku DjVu. Pojemniki te są również nazywane „kawałkami”. Typ porcji i Identyfikator porcji opisują, w jaki sposób porcja jest używana. Istnieje 4-bajtowy nagłówek, po którym następuje struktura IFF. Pierwsze cztery bajty pliku DjVu to 0x41 0x54 0x26 0x54. Ta sekcja omawia różne rodzaje dokumentów DjVu i odpowiadające im fragmenty, z których się składają.


|Identyfikator fragmentu|Użycie
---|---|
|FORM|Punkt złożony zawierający pierwsze cztery bajty danych fragmentu FORM, które są identyfikatorem drugorzędnym.
|FORM:DJVM|Wielostronicowy dokument DjVu. Fragment złożony zawierający fragment DIRM.
|FORM:DJVU|Jednostronicowy dokument DjVu. Fragment złożony, który zawiera fragmenty tworzące stronę w dokumencie djvu.
|FORM:DJVI|„Wspólny” plik DjVu, który jest dołączany przez fragment INCL. Wspólne adnotacje i słownik kształtów.
|FORM:THUM|Punkt złożony zawierający fragmenty TH44, które są osadzonymi miniaturami.
|DIRM|Informacje o nazwie strony dla dokumentów wielostronicowych.
|NAVM|Informacje o zakładkach
|ANTa, ANTz|Adnotacje, w tym zarówno początkowe ustawienia widoku, jak i nałożone hiperłącza, pola tekstowe itp.
|TXTa, TXTz|Unicode Tekst i informacje o układzie.
|Djbz|Wspólna tabela kształtów.
|Sjbz|BZZ skompresowane dane bitonalne JB2 używane do przechowywania maski.
|FG44|IW44 dane używane do przechowywania pierwszego planu
|BG44|IW44 dane używane do przechowywania tła
Dane |TH44|IW44 używane do przechowywania osadzonych miniatur
Dane |WMRM|JB2 wymagane do usunięcia znaku wodnego
|FGbz|Koloruj dane JB2. Zapewnia kolor dla każdego (blitu lub kształtu?) W odpowiedniej porcji Sjbz.
|INFO|Informacje o stronie a DjVu
|INCL|Identyfikator uwzględnionego fragmentu FORM:DJVI.
|BGjp|Tło zakodowane w formacie JPEG
|FGjp|Pierwszy plan zakodowany w formacie JPEG
|Smmr|Maska zakodowana w G4

### Kompresja DJVU

Pojedynczy obraz jest dzielony na wiele różnych obrazów, a następnie każdy obraz jest oddzielnie kompresowany. Aby utworzyć plik DjVu, obraz jest najpierw dzielony na trzy obrazy: tło, pierwszy plan i obraz maski. Zazwyczaj obrazy tła i pierwszego planu są kolorowymi obrazami o niższej rozdzielczości; ale obraz maski jest obrazem o wyższej rozdzielczości i zazwyczaj jest tam przechowywany tekst. Po separacji obrazy pierwszego planu i tła są kompresowane za pomocą algorytmu kompresji opartego na falkach IW44, podczas gdy obraz maski jest kompresowany przy użyciu innej metody zwanej JB2.

Metoda kodowania JB2 eliminuje znaczną część redundancji obrazu tekstowego, identyfikując identyczne kształty na stronie, takie jak wielokrotne występowanie znaku w określonej czcionce. JB2 najpierw koduje mapę bitową każdego unikalnego kształtu, wykorzystując redundancję między podobnymi kształtami. Następnie koduje lokalizacje, w których każdy kształt pojawia się na stronie. Zarówno JB2, jak i IW44 opierają się na nowym typie adaptacyjnego binarnego kodera arytmetycznego zwanego koderem ZP, który eliminuje pozostałą redundancję w granicach kilku procent limitu Shannona. Koder ZP jest adaptacyjny i szybszy niż inne przybliżone binarne kodery arytmetyczne.

## Bibliografia ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [Format pliku DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

