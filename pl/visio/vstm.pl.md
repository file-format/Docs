{
  "date" : "2019-10-11",
  "keywords" :[ "plik vstm", "format pliku vstm", "co to jest plik vstm", "plik", "przykład vstm", "rozszerzenie pliku vstm", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM — format pliku szablonu programu Microsoft Visio",
  "description":"Poznaj format pliku VSTM i interfejsy API, które mogą tworzyć i otwierać pliki VSTM.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik VSTM?

Pliki z rozszerzeniem VSTM to pliki szablonów utworzone za pomocą programu Microsoft Visio, które obsługują makra. W przeciwieństwie do plików VSDX, pliki utworzone z szablonów VSTM mogą uruchamiać makra opracowane w kodzie Visual Basic for Applications (VBA). Można utworzyć plik szablonu, aby zapewnić podstawowe ustawienia dokumentu, które można wykorzystać do generowania kolejnych dokumentów z tymi ustawieniami. Pliki Visio służą do tworzenia rysunków zawierających obiekty wizualne, schematy blokowe, diagram UML, przepływ informacji, schematy organizacyjne, diagramy oprogramowania, układ sieci, modele baz danych, mapowanie obiektów i inne podobne informacje. Pliki wygenerowane za pomocą Visio można również eksportować do różnych formatów plików, takich jak PNG, BMP, PDF i inne.

## Format pliku ##

Pliki VSTM są oparte na Open Packaging Conventions i XML, a programiści mogą skorzystać z tego formatu, ucząc się, jak programowo pracować z tymi plikami. Format dziedziczy wiele takich samych struktur XML, jak jego części, z formatu pliku rysunku XML programu Visio (vdx). Współdziałanie z plikami programu Visio jest znacznie zwiększone, ponieważ oprogramowanie innych firm może manipulować plikami programu Visio na poziomie formatu pliku.

Każdy plik programu Visio jest określany jako pakiet zawierający inne pliki lub części. Częścią pakietu może być plik XML, obraz, a nawet rozwiązanie VBA. Części w pakiecie można podzielić na części „dokumentowe” i „relacyjne”.

### Dokument ###

Części dokumentu zawierają rzeczywistą zawartość i metadane pliku programu Visio, takie jak nazwa pliku, pierwsza strona i wszystkie zawarte w nim kształty, a nawet połączenia danych dla kształtów. Obrazy i pliki tekstowe w paczce są uważane za części dokumentu.

### Relacje ###

Części relacji pliku Visio są przechowywane w folderze „_rels” i opisują, w jaki sposób części w pakiecie są ze sobą powiązane. Zapewnia również strukturę pliku. Autonomiczny dokument XML używa relacji nadrzędny/podrzędny elementów w celu określenia relacji między jednostkami. Prawidłowy format pliku Visio 2013 zawiera poprawny zestaw części, a pakiet zawiera relacje między częściami.

Części relacji to dokumenty XML, które opisują relacje między różnymi częściami dokumentu w pakiecie. Definiują powiązanie między dwoma elementami: określonym źródłem (zdefiniowanym przez nazwę i lokalizację pliku relacji) oraz określoną docelową częścią dokumentu. Na przykład części relacji służą do opisywania, które wzorce kształtów są powiązane z plikiem, w jaki sposób strony odnoszą się do pliku i do siebie nawzajem lub w jaki sposób obrazy i obiekty odnoszą się do określonej strony.

## Bibliografia ##

* [Wprowadzenie do formatu plików programu Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

