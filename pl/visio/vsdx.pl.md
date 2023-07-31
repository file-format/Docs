{
  "date" : "2019-10-11",
  "keywords" :["plik vsdx", "format pliku vsdx", "co to jest plik vsdx", "plik", "przykład vsdx", "rozszerzenie pliku vsdx", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"Poznaj format plików VSDX i interfejsy API, które mogą tworzyć i otwierać pliki VSDX.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik VSDX?

Pliki z rozszerzeniem .vsdx reprezentują format pliku Microsoft Visio wprowadzony od pakietu Microsoft Office 2013 i nowszych. Został opracowany w celu zastąpienia binarnego formatu pliku [.VSD](/pl/image/vsd/), który jest obsługiwany przez wcześniejsze wersje programu Microsoft Visio. Jest również obsługiwany w usługach programu Visio w programie Microsoft SharePoint Server 2013 i nie wymaga pośredniego formatu pliku do publikowania w programie SharePoint Server. Pliki Visio służą do tworzenia rysunków zawierających obiekty wizualne, schematy blokowe, diagram UML, przepływ informacji, schematy organizacyjne, diagramy oprogramowania, układ sieci, modele baz danych, mapowanie obiektów i inne podobne informacje. Pliki wygenerowane za pomocą Visio można również eksportować do różnych formatów plików, takich jak [PNG](/pl/image/png/), [BMP](/pl/image/bmp/), [PDF](/pl/pdf/) i inne.

## Format pliku ##

Pliki VSDX są oparte na Open Packaging Conventions i XML, a programiści mogą korzystać z tego formatu, ucząc się, jak programowo pracować z tymi plikami. Format dziedziczy wiele takich samych struktur XML, jak jego części, z formatu pliku rysunku XML programu Visio (vdx). Współdziałanie z plikami programu Visio jest znacznie zwiększone, ponieważ oprogramowanie innych firm może manipulować plikami programu Visio na poziomie formatu pliku.

Niektóre inne typy plików składające się na format pliku programu Visio 2013 obejmują:

* .vsdm (rysunek programu Visio z obsługą makr)
* .vssx (szablon programu Visio)
* .vssm (szablon programu Visio z obsługą makr)
* .vstx (szablon programu Visio)
* .vstm (szablon programu Visio z obsługą makr)

Pod maską format pliku Visio 2013 wykorzystuje ustrukturyzowane środki do przechowywania danych aplikacji wraz z powiązanymi zasobami w archiwum, takim jak [ZIP](/pl/compression/zip/). Plik ZIP można wyodrębnić za pomocą dowolnego standardowego narzędzia do wyodrębniania, w którym zawiera również inne typy plików. Możesz po prostu zamienić rozszerzenie pliku .vsdx na .zip w Eksploratorze Windows, aby zobaczyć zawartość pliku VSDX.

Każdy plik programu Visio jest określany jako pakiet zawierający inne pliki lub części. Częścią pakietu może być plik XML, obraz, a nawet rozwiązanie VBA. Części w pakiecie można podzielić na części „dokumentowe” i „relacyjne”.

### Dokument ###

Części dokumentu zawierają rzeczywistą zawartość i metadane pliku programu Visio, takie jak nazwa pliku, pierwsza strona i wszystkie zawarte w nim kształty, a nawet połączenia danych dla kształtów. Obrazy i pliki tekstowe w paczce są uważane za części dokumentu.

### Relacje ###

Części relacji pliku Visio są przechowywane w folderze „\_rels” i opisują, w jaki sposób części w pakiecie są ze sobą powiązane. Zapewnia również strukturę pliku. Autonomiczny dokument XML używa relacji nadrzędny/podrzędny elementów w celu określenia relacji między jednostkami. Prawidłowy format pliku Visio 2013 zawiera poprawny zestaw części, a pakiet zawiera relacje między częściami.

Części relacji to dokumenty XML, które opisują relacje między różnymi częściami dokumentu w pakiecie. Definiują powiązanie między dwoma elementami: określonym źródłem (zdefiniowanym przez nazwę i lokalizację pliku relacji) oraz określoną docelową częścią dokumentu. Na przykład części relacji służą do opisywania, które wzorce kształtów są powiązane z plikiem, w jaki sposób strony odnoszą się do pliku i do siebie nawzajem lub w jaki sposób obrazy i obiekty odnoszą się do określonej strony.

## Bibliografia ##

* [Wprowadzenie do formatu plików programu Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

