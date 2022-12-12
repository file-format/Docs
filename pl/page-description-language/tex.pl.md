{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku TEX",
  "description":"Poznaj format plików TEX i interfejsy API, które mogą tworzyć i otwierać pliki TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik TEX? ##

**TeX** to język, który obejmuje funkcje programowania i znaczników, używane do składu dokumentów. Donald Knuth z Uniwersytetu Stanforda jest twórcą tego pomysłowego systemu składu. Na całym świecie TeX jest najlepszym wyborem autorów i wydawców do tworzenia wysokiej jakości dokumentów technicznych. TeX doskonale radzi sobie z formatowaniem złożonych wyrażeń matematycznych. W połączeniu z wysokiej jakości fotoskładem, TeX konkuruje z wynikami generowanymi przez najlepsze tradycyjne systemy składu. Dlatego uważane za najbardziej klasyczne cyfrowe systemy typograficzne.

Pliki wejściowe TeX-a są oparte na kodzie ASCII, umożliwiając w ten sposób udostępnianie manuskryptów pisarzom, menedżerom wydawniczym i krytykom. Szeroka gama środowisk komputerowych, prawie każda nowoczesna platforma i wiele starszych platform obsługuje TeX. Co więcej, TeX jest darmowym oprogramowaniem, dostępnym dla szerokiego grona konsumentów. Wiele instalacji systemu UNIX używa zarówno systemu UNIX troff, jak i TeX jako systemu formatowania do różnych celów. Inne zadania składu są wykonywane ogromnie w postaci LaTeX, ConTeXt i innych pakietów makr.

## Krótka historia ##

TeX został zaprojektowany i napisany przez Donalda Knutha w 1978 roku. Guy Steele z Massachusetts Institute of Technology poprawił dane wejściowe/wyjściowe TeX-a, aby działał w niezgodnym systemie operacyjnym, takim jak Timesharing System (ITS). Pierwsza wersja TeX-a została opracowana w systemie operacyjnym WAITS firmy Stanford w języku programowania (SAIL) i przetestowana pod kątem działania na PDP-10. Knuth wprowadził ideę programowania z umiejętnością pisania dla wersji zaawansowanych. Literackie programowanie to sposób generowania kompilowalnego kodu źródłowego i składu (w TeX) dla połączonej dokumentacji przy użyciu oryginalnego pliku. Język używany do tworzenia tych zaawansowanych wersji TeX-a nazywa się WEB i jest mieszanką programów DEC PDP-10 Pascal, aby zapewnić przenośność.

Poprawiona nowa wersja TeX-a opublikowana w 1982 roku i nosiła nazwę TeX82. Główną zmianą jest zastąpienie oryginalnego algorytmu dzielenia wyrazów nowo napisanym algorytmem przez Franka Lianga. Aby zapewnić przenośność między różnymi platformami, zamiast używania liczb zmiennoprzecinkowych, TeX82 używa arytmetyki stałoprzecinkowej wraz z prawdziwym językiem programowania Turinga. W 1989 roku ukazały się nowe wersje TeX-a i Metafonta. Tak więc wersja 3.0 TeX-a umożliwia wprowadzanie 8-bitowe, pozwalając na 256 różnych znaków w tekście. Po wersji 3 aktualizacje są oznaczane przez dodanie dodatkowej cyfry na końcu przecinka, np. obecna wersja TeX-a jest oznaczona jako 3.14159265. Ta wersja była ostatnio aktualizowana 12-1-2014.

## Wejście TeX-owe ##

Plik wejściowy do TEX-a można przygotować za pomocą edytora tekstu, używając zwykłego tekstu. W przeciwieństwie do typowego edytora tekstu, ten plik wejściowy nie zezwala na żadne niewidoczne znaki kontrolne. Jeden plik może być osadzony w innym pliku, zawierającym definicje makr i definicje pomocnicze, które zwiększają możliwości TeX-a. Jeśli instalacja TeX-a jest dostarczana z plikami makr, lokalne informacje o TeX-ie pokazują, jak używać plików makr. Standardowa forma TeX-a, integruje kombinację makr i innych definicji znanych jako zwykły TEX.

Na podstawie dokładnej znajomości rozmiarów wszystkich znaków i symboli oblicza optymalną organizację liter w wierszu i wierszy na stronie. Podczas przetwarzania dokumentu tworzony jest plik .dvi, gdzie „dvi” oznacza „niezależny od urządzenia”. Do drukowania lub podglądu dokumentu z rozszerzeniem dvi wymagane są programy sterownika urządzenia. Obecnie generowanie dvi jest pomijane przez powszechnie używany pdf-TeX. Podczas instalacji TeX-a nie jest dostępna żadna wcześniejsza wiedza na temat czcionek, więc do uzyskania informacji do dokumentu wykorzystywane są zewnętrzne pliki czcionek, które są częścią lokalnego środowiska TeX.

## System składu ##

Podstawowy system TeX może zrozumieć około 300 prymitywów (poleceń). Prymitywy to polecenia niskiego poziomu, dlatego zwykły użytkownik rzadko używa ich bezpośrednio, a większość funkcji jest wykonywana przez pliki formatu. Te pliki formatu to wstępnie załadowane obrazy pamięci TeX-a, po których następuje ładowanie dużych kolekcji makr. Oryginalny domyślny format języka, tj. zwykły TeX, dodaje około 600 poleceń.

Ukośnik odwrotny zgrupowany z nawiasami klamrowymi oznacza początek poleceń TeX-a. Ponieważ TeX jest językiem opartym na makrach i tokenach, prawie wszystkie właściwości składniowe TeX-a można zmieniać w czasie wykonywania, w tym te zdefiniowane przez użytkownika, z wyjątkiem nierozszerzalnych tokenów, które są następnie wykonywane. Sama rozbudowa jest praktycznie bezproblemowa. Niektóre polecenia muszą występować po argumentach, które pomagają wyjaśnić funkcję polecenia. Na przykład polecenie \vskip nakazuje TEX-owi pominięcie strony w dół/w górę, po czym następuje argument określający, ile miejsca należy pominąć.

## Wersje ##

LaTeX jest najczęściej używanym formatem, który został pierwotnie opracowany przez Leslie Lamport. LaTeX integruje różne style dokumentów dla plików, listów, książek i slajdów oraz oferuje odniesienia i automatyczną numerację dla różnych sekcji i wyrażeń matematycznych. AMS-TeX to kolejny popularny format opracowany przez Amerykańskie Towarzystwo Matematyczne.

AMS-TeX oferuje o wiele bardziej przyjazne dla użytkownika polecenia, które mogą być przedefiniowane przez czasopisma, aby pasowały do ich lokalnego stylu. LaTeX może czerpać korzyści z AMS-TeX, używając „pakietów” AMS, które są następnie określane jako AMS-LaTeX. ConTeXt to kolejny format napisany przez Hansa Hagena, używany głównie do DTP.

Oprogramowanie TeX oferuje kilka funkcji, które były niedostępne lub miały niższą jakość w innych systemach składu w czasie jego tworzenia. Niektóre z nowatorskich cech tego języka opierają się na ciekawych algorytmach wywodzących się z tez studentów Knutha. Podczas gdy inne programy do składu zawierają teraz przydatne funkcje TeX-a w swoich programach.

## Bibliografia ##

* [System składu TeX](https://en.wikipedia.org/wiki/TeX)

