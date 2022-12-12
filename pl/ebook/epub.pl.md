{
  "date" : "2019-12-12",
  "keywords" :["EPUB", "plik", "rozszerzenie", "format", "E-Book", "Książka cyfrowa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku EPUB i interfejsy API, które mogą tworzyć i otwierać pliki EPUB.",
  "title" :"Co to jest plik EPUB?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Czym jest plik EPUB?

Pliki z rozszerzeniem .epub to format pliku e-booka, który zapewnia standardowy format publikacji cyfrowej dla wydawców i konsumentów. Format ten jest już tak powszechny, że jest obsługiwany przez wiele e-czytników i aplikacji. Na przykład w systemie Mac OS preinstalowane oprogramowanie **Books** zapewnia obsługę otwierania takich plików. Ponadto dostępnych jest wiele kompatybilnych programów na smartfony, tablety i komputery. Standardy plików EPUB są utrzymywane przez [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). Wersja EPUB 3 jest również zatwierdzona przez Book Industry Study Group (BISG), wiodące stowarzyszenie handlu książkami w zakresie standardowych najlepszych praktyk, badań, informacji i wydarzeń dotyczących pakowania treści.

## Krótka historia formatu pliku EPUB

* **Październik 2007** — zatwierdzono EPUB 2.0
* **Wrzesień 2010** - Wydano aktualizację serwisową
* **Październik 2011** - Weszły w życie specyfikacje EPUB 3.0
* **Czerwiec 2014** — wydano niewielką aktualizację konserwacyjną, która zastąpiła wersję 3.0
* **Styczeń 2017** - weszła w życie wersja EPUB 3.1

## Format pliku EPUB

Format pliku EPUB to archiwum, którego nazwę można zmienić na rozszerzenie [ZIP](/pl/compression/zip/), a jego zawartość można przeglądać, rozpakowując archiwum dowolnym ekstraktorem archiwów. Jest to otwarty format oparty na XML i składa się z plików HTML, obrazów, arkuszy stylów CSS i innych elementów. Można go również przekonwertować na PDF, Mobi i kilka innych formatów plików za pomocą wielu aplikacji i interfejsów API.

{{< figure src="../epub.png" alt="Format pliku EPUB" >}}

**E-Book EPUB otwarty w aplikacji Mac OS Books**

Format pliku EPUB oparty jest na trzech otwartych standardach.

### Otwarta struktura publiczna (OPS) ###

Plik EPUB 2.0 używa XHTML 1.1 do konstruowania treści publikacji. Zasadniczo oznacza to, że plik EPUB składa się z jednej lub więcej stron internetowych. Nawet jeśli możesz zawrzeć całą treść książki lub gazety na jednej stronie, lepiej, aby taki plik nie przekraczał 300 KB, zarówno ze względu na wydajność, jak i kompatybilność. Podobnie jak w przypadku zwykłych stron internetowych, styl i układ definiuje się za pomocą kaskadowych arkuszy stylów (CSS). W plikach EPUB należy zastosować podzbiór (ograniczoną serię poleceń) CSS2. Wiele nowych funkcji CSS3, takich jak zaokrąglone pola lub cienie, nie jest jeszcze dostępnych. Aby zapewnić kompatybilność wsteczną, twórca może również użyć DTBook zamiast XHTML do kodowania treści.

### Otwarty format opakowania (OPF) ###

Ta część specyfikacji dotyczy informacji strukturalnych, takich jak metadane (kto jest autorem i wydawcą, jaki jest tytuł,…), manifest (lista wszystkich plików w pliku epub) oraz spis treści. Wszystkie te dane są osadzone przy użyciu XML.

### Format otwartego kontenera (OCF) ###

Jak wynika z powyższych opisów, dokument EPUB składa się z serii plików. Specyfikacje OCF określają, w jaki sposób wszystkie te pliki są pakowane w jeden plik kontenera. Służy do tego kompresja ZIP.

## Obsługiwane formaty plików graficznych ##

Format pliku EPUB obsługuje następujące formaty plików graficznych.

* [GIF](/pl/image/gif/)
* [JPG](/pl/image/jpeg/)
* [PNG](/pl/image/png/)
* [SVG](/pl/page-description-language/svg/)

## Bibliografia ##

* [EPUB – z Wikipedii](https://en.wikipedia.org/wiki/EPUB)

