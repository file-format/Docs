{
  "date" : "2019-10-11",
  "keywords" :[ "plik odg", "format pliku odg", "co to jest plik odg", "plik", "przykład odg", "rozszerzenie pliku odg", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku ODG",
  "description":"Poznaj format plików ODG i interfejsy API, które mogą tworzyć i otwierać pliki ODG.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik ODG?

Format pliku ODG jest używany przez aplikację Draw Apache OpenOffice do przechowywania elementów rysunku jako obrazu wektorowego. Jest zgodny ze specyfikacjami formatu plików opartymi na XML określonymi przez Advancement of Structural Information Standards (OASIS). ODG przedstawia rysunki jako obrazy wektorowe za pomocą punktów, linii i krzywych. Oprócz OpenOffice, LibreOffice i inne aplikacje obsługują również pracę z formatem plików ODG. Inne formaty obsługiwane przez OpenOffice to na przykład [ODT](/pl/word-processing/odt/), ODF, [ODP](/pl/presentation/odp/) i [ODS](/pl/spreadsheet/ods/).


## Specyfikacje formatu plików ODG

Format pliku ODG jest oparty na formacie OpenDocument, który jest ustrukturyzowanym formatem dokumentu XML z dobrze zdefiniowanym schematem.
Każdy komponent strukturalny formatu OpenDocument jest reprezentowany przez element, który ma powiązane atrybuty. Struktura oparta na XML jest wspólna dla wszystkich typów dokumentów, takich jak dokument tekstowy, arkusz kalkulacyjny czy plik rysunkowy. Dokument może zawierać różne style. Struktura pliku OpenDocument składa się z następujących elementów.
* Korzeń dokumentu
* Metadane dokumentu
* Typy elementów ciała i dokumentów
* Ustawienia aplikacji
* Skrypty
* Deklaracje czcionek
* Style
* Style i układy stron

## Korzenie dokumentu ##

Element główny dokumentu zawiera cały dokument i jest podstawowym elementem pliku w formacie OpenDocument. Te same typy elementów głównych dokumentu mają zastosowanie do wszystkich typów dokumentów, takich jak tekst, dokumenty, arkusze kalkulacyjne i dokumenty rysunkowe.

### Elementy korzeni ###
Pojedynczy dokument XML jest reprezentowany przez swój własny element główny. Oto pięć różnych obsługiwanych elementów głównych.

`<office:document>` - Kompletny dokument biurowy w pojedynczym dokumencie XML.
`<office:document-content>` - Treść dokumentu i automatyczne style użyte w treści.
`<office:document-styles>` - Style używane w treści dokumentu i style automatyczne używane w samych stylach.
`<office:document-meta>` — metadane dokumentu, takie jak autor lub czas ostatniej operacji zapisu.
`<office:document-settings>` - Ustawienia specyficzne dla aplikacji, takie jak rozmiar okna lub informacje o drukarce.

### Metadane dokumentu ODG ###
OpenDocument zawiera wszystkie elementy metadanych w \<office:meta> element. Te ogólne informacje o dokumencie są zawarte na początku dokumentu, a aplikacje mogą aktualizować wiele wystąpień tych samych elementów.

### Element treści i typy dokumentów ###
Treść dokumentu wskazuje typ treści zawartej w dokumencie za pomocą elementu typu dokumentu. Te typy dokumentów to:
* dokumenty tekstowe
* dokumenty rysunkowe
* dokumenty prezentacji
* dokumenty arkusza kalkulacyjnego
* dokumenty wykresów
* dokumenty wizerunkowe

### Ustawienia aplikacji ###
Ustawienia aplikacji biurowych reprezentują różne ustawienia związane z konfiguracją dokumentu lub wyglądem dokumentu. Każda kategoria jest reprezentowana przez `<config:config-item-set>`. Przykłady takich kategorii ustawień obejmują:
* Ustawienia dokumentu, np. drukarka domyślna
* Wyświetl ustawienia, np. poziom powiększenia

### Skrypty ###
Często zdarza się, że dokument zawiera kilka skryptów. Każdy skrypt w pliku OpenDocument jest reprezentowany przez `<office:script>` element. Te elementy skryptu są zawarte w pojedynczym pliku `<office:scripts>` element. Skrypty nie aktualizują dokumentu podczas jego ładowania.

### Deklaracje kroju czcionki ###

Deklaracja kroju czcionki zawiera informacje o czcionkach użytych przez autora dokumentu. Te informacje pomagają zlokalizować te czcionki w innych systemach.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Style ###
Format OpenDocument obsługuje następujące style.

`Wspólne style` — reprezentacje XML takich stylów są określane jako style
`Style automatyczne` — zawierają właściwości formatowania, które w widoku interfejsu użytkownika dokumentu są przypisane do obiektu, takiego jak akapit.
`Style podstawowe` — powszechny styl zawierający informacje o formatowaniu i dodatkową zawartość, która jest wyświetlana wraz z treścią dokumentu po zastosowaniu stylu. Przykładem stylu wzorcowego są strony wzorcowe.

## Bibliografia ##
* [Format otwartego dokumentu OASIS dla aplikacji biurowych](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

