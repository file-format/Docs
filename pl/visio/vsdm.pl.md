{
  "date" : "2019-10-11",
  "keywords" :["plik vsdm", "format pliku vsdm", "co to jest plik vsdm", "plik", "przykład vsdm", "rozszerzenie pliku vsdm", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM — format pliku rysunkowego programu Microsoft Visio",
  "description":"Poznaj format pliku VSDM i interfejsy API, które mogą tworzyć i otwierać pliki VSDM.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik VSDM?

Pliki z rozszerzeniem .vsdm to pliki rysunków utworzone za pomocą aplikacji Microsoft Visio obsługującej makra. Pliki VSDM to rysunki OPC/XML, które są podobne do VSDX, ale zapewniają również możliwość uruchamiania makr podczas otwierania pliku. Makra to akcje/kroki zdefiniowane przez użytkownika, które są opracowywane w języku Visual Basic for Applications (VBA) i mogą być używane do wykonywania powtarzalnych zadań. Format pliku VSDM został wprowadzony wraz z uruchomieniem Microsoft Visio 2013. Pliki Visio służą do tworzenia rysunków zawierających obiekty wizualne, schematy blokowe, diagram UML, przepływ informacji, schematy organizacyjne, diagramy oprogramowania, układ sieci, modele baz danych, mapowanie obiektów i inne podobne informacje. Pliki wygenerowane za pomocą Visio można również eksportować do różnych formatów plików, takich jak [PNG](/pl/image/png/), [BMP](/pl/image/bmp/), [PDF](/pl/pdf/) i inne.

## Format pliku VSDM

Pliki VSDM są oparte na Open Packaging Conventions i XML, a programiści mogą korzystać z tego formatu, ucząc się, jak programowo pracować z tymi plikami. Format dziedziczy wiele takich samych struktur XML, jak jego części, z formatu pliku rysunku XML programu Visio (vdx). Współdziałanie z plikami programu Visio jest znacznie zwiększone, ponieważ oprogramowanie innych firm może manipulować plikami programu Visio na poziomie formatu pliku.

Każdy plik programu Visio jest określany jako pakiet zawierający inne pliki lub części. Częścią pakietu może być plik XML, obraz, a nawet rozwiązanie VBA. Części w pakiecie można podzielić na części „dokumentowe” i „relacyjne”.

### Dokument ###

Części dokumentu zawierają rzeczywistą zawartość i metadane pliku programu Visio, takie jak nazwa pliku, pierwsza strona i wszystkie zawarte w nim kształty, a nawet połączenia danych dla kształtów. Obrazy i pliki tekstowe w paczce są uważane za części dokumentu.

### Relacje ###

Części relacji pliku Visio są przechowywane w folderze „\_rels” i opisują, w jaki sposób części w pakiecie są ze sobą powiązane. Zapewnia również strukturę pliku. Autonomiczny dokument XML używa relacji nadrzędny/podrzędny elementów w celu określenia relacji między jednostkami. Prawidłowy format pliku Visio 2013 zawiera poprawny zestaw części, a pakiet zawiera relacje między częściami.

Części relacji to dokumenty XML, które opisują relacje między różnymi częściami dokumentu w pakiecie. Definiują powiązanie między dwoma elementami: określonym źródłem (zdefiniowanym przez nazwę i lokalizację pliku relacji) oraz określoną docelową częścią dokumentu. Na przykład części relacji służą do opisywania, które wzorce kształtów są powiązane z plikiem, w jaki sposób strony odnoszą się do pliku i do siebie nawzajem lub w jaki sposób obrazy i obiekty odnoszą się do określonej strony.

## Bibliografia ##

* [Wprowadzenie do formatu plików programu Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

