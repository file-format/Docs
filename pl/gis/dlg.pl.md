{
  "date" : "2021-07-30",
  "keywords" :["plik dlg", "format pliku dlg", "co to jest plik dlg", "plik", "przykład dlg", "rozszerzenie pliku dlg", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG — format indeksu kształtu pliku kształtu",
  "description":"Poznaj format plików DLG i interfejsy API, które mogą tworzyć i otwierać pliki DLG.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Czym jest plik DLG?
Plik z rozszerzeniem .dlg zawiera cyfrowy wykres liniowy, który jest elementem mapy kartograficznej pokazanej w cyfrowej formie wektorowej, zarządzanej przez US Geological Survey (USGS). Pliki DLG są dostępne w dwóch różnych formatach:
1. **Format opcjonalny**: Prosty w użyciu format, który zawiera 80-bajtowy rekord logiczny, układ współrzędnych naziemnych UTM oraz powiązania topologii zawarte w elementach liniowych, węzłowych i powierzchniowych.
2. **Format Spatial Data Transfer Standard (SDTS)**: format ułatwiający przenoszenie danych przestrzennych między różnymi systemami komputerowymi.

## Format pliku DLG
Format pliku DLG jest przeznaczony dla map USGS i jest przesyłany w dużej, średniej i małej skali z maksymalnie dziewięcioma różnymi kategoriami obiektów. Pliki DLG są dostępne w formatach opcjonalnych i formatach Spatial Data Transfer Standard (SDTS), które mają strukturę topologiczną do użytku w mapowaniu i aplikacjach GIS.
### Specyfikacje formatu plików DLG
Pliki DLG są dystrybuowane w trzech różnych skalach:

1. **Duża skala** - zwykle odpowiada:
- USGS 7,5 o 7,5 minuty
- Serie map topograficznych czworokątów w skali 1:24 000 i 1:25 000
- Alaska w skali 1:63360
- Skala 1:30 000 dla Puerto Rico
 

2. **Skala pośrednia** - wyprowadzona z USGS:

- 30- na 60 minut

- Seria map w skali 1:100 000
3. **Mała skala** — pochodzi z map przekrojowych USGS w skali 1:2 000 000 z atlasu narodowego Stanów Zjednoczonych
### Kategorie danych
W plikach DLG dostępnych jest dziewięć różnych kategorii warstw lub funkcji:
1. Publiczny System Geodezyjny (PLSS)
2. Granice (BD)
3. Transport (TR)
4. Hydrografia (HY)
5. Hipsografia (HP)
6. Cechy niewegetatywne (NV)
7. Kontrola geodezyjna i znaczniki (SM)

8. Elementy stworzone przez człowieka (MS)

9. Wegetatywne pokrycie powierzchni (SC)

Pliki DLG o dużej skali oferują wszystkie dziewięć warstw, podczas gdy pliki o średniej skali oferują pięć warstw PLSS, BD, TR, HY i HP. DLG na małą skalę oferują pięć warstw PLSS, BD, TR, HY i MS.

## Bibliografia

* [Cyfrowy wykres liniowy – z Wikipedii)](https://en.wikipedia.org/wiki/Digital_line_graph)


