{
  "date" : "2019-12-03",
  "keywords" :["doc", "plik", "rozszerzenie", "format pliku", "Word", "Dokument"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - plik dokumentu programu Microsoft Word",
  "description":"Poznaj format plików DOC i interfejsy API, które mogą tworzyć i otwierać pliki DOC.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Czym jest plik DOC?

Pliki z rozszerzeniem .doc reprezentują dokumenty wygenerowane przez program Microsoft Word lub inne dokumenty tekstowe w formacie pliku binarnego. Rozszerzenie było początkowo używane do dokumentacji zwykłego tekstu w kilku różnych systemach operacyjnych. Może zawierać kilka różnych typów danych, takich jak obrazy, sformatowany i zwykły tekst, wykresy, wykresy, obiekty osadzone, linki, strony, formatowanie strony, ustawienia drukowania i wiele innych. Format był popularny w przypadku wszelkiego rodzaju dokumentacji ze względu na różnorodność opcji, jakie oferuje użytkownikom w zakresie pisania instrukcji, propozycji, specyfikacji, życiorysów, artykułów lub wszelkich podobnych dokumentów. Zaktualizowana wersja DOC to [DOCX](/pl/Word%20Processing/DOCX/), która jest oparta na pakiecie Office OpenXML, którego specyfikacje są powszechnie dostępne.

## Krótka historia ##

WordPerfect, produkt [Corel](https://www.corel.com/en/), używał DOC jako rozszerzenia swojego zastrzeżonego formatu. W latach 80-tych WordPerfect był wybierany na większości komputerów ze względu na jego łatwą dostępność, zgodność z większością komputerów i systemów operacyjnych. Jednak WordPerfect odnotował upadek w systemie operacyjnym Windows, kiedy Microsoft wprowadził Microsoft Word jako swój produkt do formatu plików dokumentów i wybrał rozszerzenie DOC dla swojego zastrzeżonego formatu. W miarę jak Microsoft Word stawał się coraz bardziej popularny, format pliku DOC przeszedł kilka zmian od Microsoft Word 97 - 2003. W 2007 roku domyślny format pliku DOC został zastąpiony przez format Office Open XML (znany jako DOCX) i nowe wersje Microsoft Word używa teraz tego nowego rozszerzenia jako domyślnego formatu pliku.

## Specyfikacje formatu plików DOC — więcej informacji

Firma Microsoft nie publikowała specyfikacji formatu plików DOC przez długi czas, aż do 2008 r. W lutym 2008 r. Wydano specyfikacje formatu plików .doc w ramach obietnicy Microsoft Open Specification Promise. Chociaż specyfikacja nie opisuje wszystkich funkcji używanych przez format DOC, zawiera obszerne informacje na temat wiedzy wymaganej do pracy z tym formatem plików. Mimo to, aby wykorzystać dostępne informacje, wymagana jest inżynieria odwrotna. Specyfikacje były aktualizowane kilka razy, a najnowsza [wersja](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) to 8.0, która została zaktualizowana w sierpniu 2018 r. .

### Niektóre podstawowe pojęcia ###

Zanim przejdziemy do szczegółów dotyczących specyfikacji formatu plików DOC, konieczne jest zrozumienie kilku podstawowych pojęć, aby móc pracować z tym formatem plików.

**Baza informacji o pliku (Fib):** Struktura Fib zawiera informacje o dokumencie i określa wskaźniki pliku do różnych części składających się na dokument.
Fib jest strukturą o zmiennej długości. Z wyjątkiem części podstawowej, której rozmiar jest stały, każda sekcja jest poprzedzona polem zliczania, które określa rozmiar następnej sekcji.

**Pozycja znaku:** CP lub pozycja znaku reprezentuje 32-bitową liczbę całkowitą bez znaku, która służy jako liczony od zera indeks znaku w tekście dokumentu. Lokalizacji i rozmiaru każdego znaku w pliku nie można pobrać bezpośrednio i należy je obliczyć przy użyciu wcześniej określonego algorytmu. Postacie obejmują:

* Tekst dokumentu
* Kotwice obiektów, takich jak przypisy lub pola tekstowe
* Znaki kontrolne, takie jak znaki akapitu i znaki komórek tabeli

**PLC:** Struktura PLC to tablica CP, po której następuje tablica elementów danych. Elementy danych dla dowolnego sterownika PLC muszą mieć ten sam rozmiar równy zero lub więcej bajtów iz tego powodu liczba CP musi być o jeden większa niż liczba elementów danych. Struktury PLC są różnych typów, gdzie każdy typ określa, czy duplikaty CP są dozwolone dla tego typu, czy nie. Struktura PLC składa się z:

* **aCP (zmienna długość):** Tablica elementów CP. Każdy typ struktury **PLC** określa znaczenie elementów CP i dozwolony zakres.
* **aDane (zmienna długość):** Każdy typ struktury **PLC** określa strukturę i znaczenie elementów danych, wszelkie ograniczenia dotyczące liczby elementów danych oraz wszelkie ograniczenia dotyczące zawartych w nich danych. Określa również związek między elementami danych a odpowiednimi CP.

**Prawidłowy wybór:** Konstrukcje plików .DOC są opisywane głównie przez szereg CP. Istnieje wiele [reguł](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) określonych przez firmę Microsoft, których należy przestrzegać w takim przypadku.

**STTB:** STTB to tablica łańcuchów składająca się z nagłówka, po którym następuje tablica elementów. Wartość **cData** określa liczbę elementów zawartych w tablicy.

**Przechowywanie właściwości:** plik Word może zawierać różne elementy, takie jak tekst, akapity, tabele, obrazy i sekcje, z których każdy może mieć własne właściwości. Ich właściwości są przechowywane w pliku programu Word jako różnice w stosunku do wartości domyślnych. Takie różnice są określone przez PRl, który składa się z pojedynczego modyfikatora właściwości (Sprm) i jego operandu. Aplikacja może określić ostateczny zestaw właściwości, stosując listy **Prl**s.

**Ochrona hasłem:** Pliki programu Word mogą być również chronione hasłem, do czego można użyć jednego z poniższych mechanizmów.

* Zaciemnianie XOR
* Szyfrowanie dokumentów binarnych pakietu Office RC4
* Dokument binarny pakietu Office Szyfrowanie RC4 CryptoAPI

Jeśli FibBase.fEncrypted i FibBase.fObfuscation mają wartość 1, plik jest zaciemniany przy użyciu zaciemniania XOR.

Jeśli właściwość FibBase.fEncrypted ma wartość 1, a FibBase.fObfuscation ma wartość 0, plik jest szyfrowany przy użyciu szyfrowania Office Binary Document RC4 lub Office Binary Document RC4 CryptoAPI Encryption, z nagłówkiem EncryptionHeader przechowywanym w pierwszych bajtach FibBase.lKey strumienia tabeli. EncryptionHeader.EncryptionVersionInfo określa, który mechanizm szyfrowania został użyty do zaszyfrowania pliku.

### Struktura plików ###

Binarny plik Word w swojej oryginalności jest plikiem złożonym OLE, który składa się z kilku magazynów i strumieni. Te magazyny i strumienie mają własną strukturę i rozmiary, które określają parametry zapisu i odczytu. To są:

#### Strumień WordDocument ####

Ten strumień zawiera tekst dokumentu i inne informacje, do których odniesienia znajdują się w innych częściach pliku. Strumień nie ma predefiniowanej struktury innej niż FIB na początku, która jest obowiązkowa i powinna mieć przesunięcie 0. Ten strumień nie może być większy niż 2147 MB.

#### 1TableStream lub 0TableStream ####

Binarny plik Word może zawierać strumienie tabel znane jako strumień 1Table lub strumień 0Table. Przynajmniej jeden z nich powinien być obecny w dokumencie. Jeśli jednak dokument zawiera zarówno strumienie 1Table, jak i 0Table, używany jest tylko strumień, do którego odwołuje się base.fWhichTblStm. Strumień bez odniesienia MUSI zostać zignorowany.
Strumień tabeli NIE MOŻE być większy niż 2147 MB.

#### Strumień danych ####

Strumień danych nie ma predefiniowanej struktury. Zawiera dane, do których odwołuje się FIB lub inne części pliku. Ten strumień nie musi być obecny, jeśli nie ma do niego odniesień. Strumień danych NIE MOŻE być większy niż 2147 MB.

#### Przechowywanie puli obiektów ####

Magazyn puli obiektów zawiera magazyny dla osadzonych obiektów OLE. Ta pamięć nie musi być obecna, jeśli w dokumencie nie ma osadzonych obiektów OLE.

#### Niestandardowe przechowywanie danych XML ####

Niestandardowy magazyn danych XML to opcjonalny magazyn, którego nazwa MUSI brzmieć „MsoDataStore”.

#### Strumień informacji podsumowujących ####

Strumień informacji podsumowujących jest opcjonalnym strumieniem, którego nazwa MUSI być „\005SummaryInformation”, gdzie \005 to znak o wartości 0x0005, a nie literał łańcuchowy „\005”.

#### Strumień informacji podsumowujących dokument ####

Strumień informacji podsumowujących dokument jest opcjonalnym strumieniem, którego nazwa MUSI mieć postać „\005DocumentSummaryInformation”, gdzie \005 to znak o wartości 0x0005, a nie literał łańcuchowy „\005”.

#### Strumień szyfrowania ####

Strumień Encryption jest opcjonalnym strumieniem, którego nazwa MUSI brzmieć „encryption”. Ten strumień NIE MOŻE być obecny, chyba że spełnione są oba poniższe warunki:

* Dokument jest szyfrowany za pomocą szyfrowania Office Binary Document RC4 CryptoAPI.
* Wartość fDocProps jest ustawiona w pliku EncryptionHeader.Flags.

#### Przechowywanie makr ####

Magazyn makr to opcjonalny magazyn zawierający makra dla pliku. Jeśli jest obecny, MUSI to być główny magazyn projektu.

#### Przechowywanie podpisów XML ####

Magazyn podpisów XML jest opcjonalnym magazynem, którego nazwa MUSI być „_xmlsignatures”.

#### Strumień podpisów ####

Strumień podpisów jest opcjonalnym strumieniem, którego nazwa MUSI być „_signatures”. Ten strumień zawiera podpisy cyfrowe.

#### Zarządzanie prawami do informacji Przestrzeń danych Przechowywanie ####

Przestrzeń danych zarządzania prawami do informacji jest magazynem opcjonalnym, którego nazwa MUSI być „\006DataSpaces”, gdzie \006 to znak o wartości 0x0006, a nie literał łańcuchowy „\006”. Jeśli ta pamięć jest obecna, strumień chronionych treści MUSI być również obecny.
Jeśli to miejsce przechowywania jest obecne, wszystkie określone strumienie i miejsca przechowywania inne niż to miejsce przechowywania i strumień chronionych treści POWINNY być odczytywane ze strumienia chronionych treści, jak określono w [MS-OFFCRYPTO] i jeśli którykolwiek z tych strumieni i miejsc przechowywania istnieje poza chronionymi treściami Stream, POWINNY być ignorowane.

#### Chroniony strumień treści ####

Strumień chronionych treści to opcjonalny strumień, którego nazwa MUSI mieć postać „\009DRMContent”, gdzie \009 to znak o wartości 0x0009, a nie literał łańcuchowy „\009”.
Jeśli ten strumień jest obecny, MUSI również być obecny magazyn przestrzeni danych zarządzania prawami do informacji.

## Bibliografia ##

* [Specyfikacje tworzenia plików MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))

