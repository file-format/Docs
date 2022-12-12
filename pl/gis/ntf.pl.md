{
  "date" : "2021-07-28",
  "keywords" :["plik ntf", "format pliku ntf", "co to jest plik ntf", "plik", "przykład ntf", "rozszerzenie pliku ntf", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - Krajowe Formaty Transferu Plików",
  "description":"Poznaj format pliku NTF i interfejsy API, które mogą tworzyć i otwierać pliki NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Czym jest plik NTF?
Pliki z rozszerzeniem .ntf nazywane są plikami **National Transfer Format (NTF)**; najczęściej używany przez UK Ordnance Survey (OS); specjalnie do przesyłania danych geoprzestrzennych. Zarządza nim British Standards Institution. Stał się standardowym formatem przesyłania danych cyfrowych Ordnance Survey. Projekcja National Grid w Wielkiej Brytanii, która jest rodzajem Transverse Mercator, zawiera wszystkie informacje georeferencyjne dla plików NTF.

## Format pliku NTF
Format pliku NTF jest własnością Ordnance Survey w Wielkiej Brytanii; obsługiwane przez bibliotekę GDB do importu. Obecna wersja formatu pliku NTF to 2.0. Ten format pliku został wprowadzony w celu rozwiązania problemu ograniczenia segmentu wektora **PCIDSK**, który ma tylko jedno pole atrybutu na strukturę, ale istnieje wiele atrybutów, które można wyodrębnić za pomocą danych wektorowych. Aby obejść format pliku NTF, składa się on z dwóch segmentów. Każdy segment składa się z tych samych wektorów, ale z różnymi atrybutami. Pierwszy segment pliku wektorowego NTF zawiera wektory z numerem kodu funkcji jako atrybutem. Drugi segment zawiera wektory z wartością jako atrybutem.

### System odniesień do współrzędnych
Biblioteka GDB reprezentuje dane rastrowe i wektorowe z odpowiednią charakterystyką projekcji TM:

- Referencyjna długość geograficzna: 49,0
Szerokość geograficzna odniesienia: 2,0
- Fałszywa współrzędna wschodnia: 400000
- Fałszywa północ: -100000
- Skala: 0,9996012717
- Elipsoida: Airy 1830 (E009)
Nie jest dostępne żadne wsparcie dla aktualizowania lub zapisywania plików NTF, ani nie można łączyć plików DTM.

### Przykład Ogrinfo
Poniższy przykład wykorzystuje **ogrinfo** w pliku NTF do pobrania numerów warstw:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Bibliografia

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Mapowanie sieciowe – zilustrowane przez Tylera Mitchella](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

