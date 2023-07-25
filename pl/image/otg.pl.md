{
  "date" : "2020-01-10",
  "keywords" :[ "plik otg", "format pliku otg", "co to jest plik otg", "plik", "przykład otg", "rozszerzenie pliku otg", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - format pliku szablonu rysunku OpenDocument",
  "description":"Poznaj format plików OTG i interfejsy API, które mogą tworzyć i otwierać pliki OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Czym jest plik OTG?

Plik OTG to szablon rysunku utworzony przy użyciu standardu OpenDocument zgodnego ze specyfikacją OASIS Office Applications [1.0](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Reprezentuje domyślną organizację elementów rysunku dla obrazu wektorowego, której można użyć do dalszego ulepszenia zawartości pliku. Pliki OTF są jak wszystkie inne pliki oparte na formacie OpenDocument, które są oparte na formacie XML do reprezentowania zawartości dokumentu. Pliki OTF można przeglądać, otwierając je w dowolnym edytorze tekstowym lub standardowym XML.

## Specyfikacje formatu plików OTG ##

Format pliku OTG jest oparty na formacie OpenDocument XML, który ma ugruntowany schemat. Struktura każdego składnika formatu OpenDocument jest reprezentowana przez element, który ma powiązane atrybuty i jest wspólny dla wszystkich typów dokumentów, takich jak dokument tekstowy, arkusz kalkulacyjny lub plik rysunku. OTG, będąc szablonem rysunkowym, szeroko wykorzystuje specyfikacje treści graficznych, które obejmują:

* Ulepszone funkcje strony dla aplikacji graficznych
* Rysowanie kształtów
* Ramki
* Kształty 3D
* Niestandardowy kształt
* Kształty prezentacji
* Animacje prezentacji
* Animacje prezentacji SMIL
* Imprezy prezentacyjne
* Obecne pola tekstowe
* Treść dokumentu prezentacji

### Ulepszone funkcje strony dla aplikacji graficznych ###
#### Mistrz materiałów informacyjnych ####

Element Handout Master to szablon do automatycznego generowania stron materiałów informacyjnych dla aplikacji obsługujących drukowanie takich stron.
Atrybuty, które mogą być powiązane z `<style:handout-master> ` elementem są:

|Układ|Atrybut|Opis
---|---|---|
|Układ strony prezentacji|prezentacja:nazwa-układu-strony-prezentacji|Linki do `<style:presentation-page-layout> ` atrybut
|Układ strony|`styl:nazwa-układu-strony` | Określa układ strony, który zawiera rozmiary, obramowanie i orientację strony wzorcowej materiałów informacyjnych.
|Styl strony|`draw:nazwa-stylu`|Przypisuje dodatkowe atrybuty formatowania do strony wzorcowej materiałów informacyjnych poprzez przypisanie stylu strony rysunku.|
|Deklaracja nagłówka| `prezentacja:użyj-nazwy-nagłówka`| Określa nazwę deklaracji pola nagłówka, która jest używana dla wszystkich pól nagłówka wyświetlanych na stronie wzorcowej materiałów informacyjnych.
|Deklaracja stopki| Presentation:use-footer-name|Określa nazwę deklaracji pola stopki, która jest używana dla wszystkich pól stopki wyświetlanych na stronie wzorcowej materiałów informacyjnych.
|Deklaracja daty i godziny|nazwa-daty-czasu-użytkowania|Określa nazwę deklaracji pola daty-godziny, która jest używana dla wszystkich pól daty-godziny wyświetlanych na stronie wzorcowej materiałów informacyjnych.

### Rysowanie kształtów ###
Format OpenDocument obsługuje kilka kształtów rysunków, które mogą być używane w dowolnym typie dokumentu.

|Kształt|Powiązane atrybuty| elementy
---|---|---|
Prostokąt - `<draw:rect> `|Pozycja, rozmiar, styl, warstwa, indeks Z, identyfikator, identyfikator podpisu, zakotwiczenie tekstu, tło tabeli, pozycja końcowa rysowania, zaokrąglone rogi|tytuł, długi opis, detektory zdarzeń, punkty klejenia, tekst
Linia `<draw:line> `|Styl, warstwa, indeks Z, identyfikator, identyfikator podpisu i transformacja, zakotwiczenie tekstu, tło tabeli, pozycja końcowa rysowania, punkt początkowy, punkt końcowy|tytuł, długi opis, detektory zdarzeń, punkty klejenia, tekst
Polilinia `<draw:polyline> `| Pozycja, rozmiar, pole widoku, styl, warstwa, indeks Z, identyfikator, identyfikator podpisu i transformacja, zakotwiczenie tekstu, tło tabeli, pozycja końcowa rysowania, punkty| Tytuł, długi opis, słuchacze zdarzeń, punkty klejenia, tekst
Wielokąt `<draw:polygon> `|Pozycja, rozmiar, pole widoku, styl, warstwa, indeks Z, identyfikator, identyfikator podpisu i transformacja, zakotwiczenie tekstu, tło tabeli, pozycja końcowa rysowania, punkty|tytuł, długi opis, detektory zdarzeń, punkty klejenia, tekst
|Wielokąt regularny `<draw:regular-polygon> `|Pozycja, rozmiar, styl, warstwa, indeks Z, identyfikator, identyfikator podpisu i transformacja, zakotwiczenie tekstu, tło tabeli, pozycja końcowa rysowania, wklęsłe, rogi, ostrość|tytuł, długi opis, odbiorniki zdarzeń, punkty klejenia, tekst
|Ścieżka `<draw:path> `|Pozycja, rozmiar, pole widoku, styl, warstwa, indeks Z, identyfikator, identyfikator podpisu i transformacja, zakotwiczenie tekstu, tło tabeli, pozycja końcowa rysowania, dane ścieżki| Tytuł, długi opis, słuchacze zdarzeń, punkty kleju, tekst

### Ramki ###
Ramka w dokumencie rysunkowym jest prostokątnym pojemnikiem zawierającym pola tekstowe, obrazy lub obiekty. Ramki obsługują dodatkowe funkcje, takie jak kontury, mapy obrazów i hiperłącza. Ramka może zawierać zarówno obiekt, jak i obraz, co pozwala na wielokrotne odwzorowanie obiektu. Aplikacje renderują dany element w oparciu o najlepsze wsparcie.

Ramki mogą zawierać:
* Pola tekstowe
* Obiekty reprezentowane w formacie OpenDocument lub w formacie binarnym specyficznym dla obiektu
* Obrazy
* Aplety
* Wtyczki
* Pływające ramki

Ramka jest zawarta w dokumencie, jak pokazano poniżej.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Bibliografia ##
* [Format otwartego dokumentu OASIS dla aplikacji biurowych](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

