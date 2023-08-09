{
  "date" : "2019-12-09",
  "keywords" :["plik 3mf", "format pliku 3mf", "co to jest plik 3mf", "plik", "przykład 3mf", "rozszerzenie pliku 3mf","rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Poznaj format plików 3MF i interfejsy API, które mogą otwierać i tworzyć pliki 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Czym jest plik 3MF?

3MF, 3D Manufacturing Format, jest używany przez aplikacje do renderowania modeli obiektów 3D w wielu innych aplikacjach, platformach, usługach i drukarkach. Został zbudowany, aby uniknąć ograniczeń i problemów w innych formatach plików 3D, takich jak [STL](/pl/cad/stl/), do pracy z najnowszymi wersjami drukarek 3D. 3MF to stosunkowo nowy format plików, który został opracowany i opublikowany przez konsorcjum 3MF. Jest wystarczająco bogaty, aby w pełni opisać model, zachowując informacje wewnętrzne, kolor i inne cechy, dzięki którym jest rozszerzalny w celu wspierania nowych innowacji w druku 3D. Format jest rozszerzalny, może być szeroko stosowany i wolny od problemów nękających inne powszechnie używane formaty plików.

## Krótka historia formatu plików 3MF

Istniejące ograniczenia w dostępnych formatach plików opisujących modele, takich jak STL i inne, skłaniają wiodące marki do zebrania się i sformułowania bardziej rozszerzalnego formatu plików do druku 3D. Ważną kwestią było to, w jaki sposób aplikacje powinny przekazywać dane modelu do drukarek 3D. W związku z tym konsorcjum 3MF powstało w celu wsparcia nowego formatu plików 3D o nazwie 3MF w celu uczynienia go wystarczająco rozszerzalnym, aby zaspokoić potrzeby drukowania 3D. W skład tego konsorcjum wchodziło kilka firm, w tym Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP i inne. Firma Microsoft przekazała trwające prace nad formatem plików 3D jako punkt wyjścia do wspólnego dalszego rozwoju specyfikacji konsorcjum 3MF.

## Format pliku 3MF — więcej informacji

3MF to format danych oparty na XML – skompresowany XML czytelny dla człowieka – który zawiera definicje danych związanych z produkcją 3D, w tym rozszerzalność danych niestandardowych przez strony trzecie. Format pliku 3MF został zaprojektowany z myślą o ograniczeniach i problemach napotykanych przez inne formaty plików 3D. Doprowadziło to do sformułowania formatu pliku 3MF, który jest:

* **Kompletne:** Zawiera wszystkie niezbędne informacje o modelu, materiale i właściwościach w jednym archiwum
* **Czytelne dla człowieka:** Korzystanie z typowych struktur, takich jak OPC, [ZIP](/pl/compression/zip/) i XML w celu ułatwienia programowania
* **Prostota:** Krótka, przejrzysta specyfikacja ułatwiająca tworzenie i szybką weryfikację
* **Rozszerzalny:** Wykorzystanie przestrzeni nazw XML pozwala na stosowanie zarówno publicznych, jak i prywatnych rozszerzeń przy zachowaniu zgodności
* **Jednoznaczne:** Przejrzysty język i testy zgodności gwarantują, że plik jest zawsze spójny, od wersji cyfrowej do fizycznej
* **Bezpłatny:** dostęp do specyfikacji 3MF i jej wdrażanie jest i zawsze będzie wolny od opłat licencyjnych, patentów i licencji

Specyfikacje formatu plików 3MF są hostowane w [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) w celu publicznego dostępu i ciągłych aktualizacji. Obecna opublikowana wersja to 1.2.3, która opisuje zestaw konwencji dotyczących używania XML i innych powszechnie dostępnych technologii do opisywania zawartości i wyglądu jednego lub więcej modeli 3D. Deweloperzy, którzy chcą zbudować systemy do przetwarzania formatów plików 3MF, mogą zapoznać się z tymi specyfikacjami w celu wdrożenia.

## Specyfikacje formatu plików 3MF

Format pliku 3MF wykorzystuje specyfikacje Open Packaging w postaci archiwum ZIP dla swojego modelu fizycznego. Zawiera dobrze zdefiniowany zestaw części i relacji, które spełniają określony cel w dokumencie. Dzięki temu format jest zgodny z funkcją pakietu, w tym z podpisami cyfrowymi i miniaturami.

### Dokument 3MF — przegląd

Typowy dokument 3MF wygląda następująco:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

Ładunek zawiera pełny zestaw części wymaganych do przetworzenia części Modelu 3D. Cała zawartość, która ma być wykorzystana do wytworzenia obiektu opisanego w ładunku 3D MUSI być zawarta w Dokumencie 3MF. Opis każdej części dokumentu wraz z jej wymaganym statusem lub opcją przedstawiono w poniższej tabeli.


|**Imię**|**Opis**|**Źródło relacji**|**Wymagane/Opcjonalne**
--- | --- | --- | ---
|Model 3D|Zawiera opis jednego lub więcej obiektów 3D do produkcji.|Pakiet|WYMAGANE
|Podstawowe właściwości|Część OPC zawierająca różne właściwości dokumentu.|Pakiet|OPCJONALNIE
|Pochodzenie podpisu cyfrowego|Część OPC, która jest źródłem podpisów cyfrowych w pakiecie.|Pakiet|OPCJONALNIE
|Podpis cyfrowy|Części OPC, z których każda zawiera podpis cyfrowy.|Podpis cyfrowy Pochodzenie|OPCJONALNE
|Certyfikat podpisu cyfrowego|Części OPC zawierające certyfikat podpisu cyfrowego.|Podpis cyfrowy|OPCJONALNIE
|PrintTicket|Zawiera ustawienia, które mają być używane podczas wyprowadzania obiektów 3D w części modelu 3D.|Model 3D|OPCJONALNIE
|Miniatura|Zawiera mały obraz JPEG lub PNG reprezentujący obiekty 3D w pakiecie lub w pakiecie jako całości.|Pakiet|OPCJONALNIE
|Tekstura 3D|Zawiera teksturę używaną do nakładania koloru na obiekt 3D w części Model 3D (dostępna dla rozszerzeń)|Model 3D|OPCJONALNIE
|Części niestandardowe|Części OPC, które są powiązane z metadanymi|Pakiet|OPCJONALNE

[Części i relacje](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [Modele 3D](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Zasoby obiektów](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Zasoby materiałowe](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) i [Funkcje pakietu](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) sekcje specyfikacji dokumentu zawiera szczegółowe informacje na temat dokumentu 3MF.

## Bibliografia ##

* [Specyfikacje formatu plików 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF – z Wikipedii](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

