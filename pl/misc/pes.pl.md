{
  "date" : "2021-07-29",
  "keywords" :["plik pes", "format pliku pes", "co to jest plik pes", "plik", "przykład pes", "rozszerzenie pliku pes","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku PES — format haftu Brother PE",
  "description":"Poznaj format plików PES i interfejsy API, które mogą tworzyć i otwierać pliki PES.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Co to jest plik haftu PES?

Plik haftu PES to plik projektu, który zawiera instrukcje dla maszyn do haftowania/szycia. Został opracowany przez Brother Industries dla ich maszyn do haftowania, ale później został sformalizowany jako ogólny format pliku. Pliki PES są używane przez maszyny do szycia do odczytywania instrukcji szycia wzorów na tkaninie. Pliki te służą dwóm celom; po pierwsze dostarczanie informacji projektowych dla aplikacji PE-Design opracowanej przez Brother Industries, a po drugie, podanie nazwy projektu, kolorów i kodów hafciarki, takich jak „stop”, „skok” i „przycinanie”.

## Format pliku PES — więcej informacji

Plik PES jest zapisywany na dysku w formacie pliku binarnego. Zawiera wiele sekcji, w których przechowywane są informacje o szyciu przy użyciu predefiniowanej metody. Format pliku PES jest następujący.

* Dane wersji — podaje informacje o wersji i może mieć dowolną wartość `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* Wartość wyszukiwania PEC — 4-bajtowa liczba całkowita typu little-endian występująca bezpośrednio po danych wersji i reprezentująca wartość wyszukiwania dla sekcji PEC, która zawiera szczegóły projektu.
* Sekcja PSE — zawiera informacje projektowe odnoszące się do Brother PE-Design i mogą dotyczyć innych aplikacji do szycia
* Sekcja PCE — może znajdować się w dowolnym miejscu pliku PSE, ale odwołuje się do niej wartość wyszukiwania PEC.

## Typ maszyn do szycia korzystających z pliku PES

Pliki PES są tworzone głównie przez oprogramowanie PE-Design używane z maszynami do szycia Brother. Niektóre inne maszyny, które mogą obsługiwać pliki PES, to domowe hafciarki Babylock i Bernina.

## Jak przekonwertować pliki PSE?

Aplikacja PE-Design może [konwertować plik PSE](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+plik) na inne formaty, takie jak .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd lub .xxx. Można to zrobić za pomocą aplikacji PE-Design, otwierając plik i wybierając format konwersji.

## Bibliografia

* [Projekt PE — instrukcja obsługi](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

