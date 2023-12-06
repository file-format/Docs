{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik HDR - Format pliku nagłówkowego ESRI BIL",
  "description":"Co to jest plik HDR?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Co to jest plik HDR?

Plik HDR to plik nagłówkowy GIS zawierający informacje nagłówkowe dla pliku typu Band przeplatanego linią (.BIL). Opisuje dane obrazu i ma taką samą nazwę jak plik obrazu. Plik HDR składa się z zestawu wpisów, z których każdy opisuje określony atrybut obrazu. Plik HDR opisuje układ i formatowanie pliku BIL do tłumaczenia na współrzędne świata rzeczywistego w połączeniu z oddzielnym plikiem georeferencyjnym.

## Format pliku HDR

Pliki HDR są zapisywane w formacie pliku tekstowego ASCII. Zawiera zestaw wpisów, z których każdy opisuje konkretny atrybut obrazu. Każdy plik HDR ma następujący format:

```
<keyword> <value>
```

`<keyword> ` - Wskazuje konkretny atrybut, który jest ustawiany
`<value> ` - Jest to wartość, na którą ustawiany jest atrybut

Nie ma ograniczeń co do kolejności wpisów w nagłówku. Jednak każdy wpis musi znajdować się w osobnej linii, aby zachować zgodność z metodą analizy używaną przez czytniki HDR.

## Podsumowanie słów kluczowych używanych w pliku HDR

|Słowo kluczowe |Dopuszczalna wartość |Domyślne|
---|---|---|
|nrows |dowolna liczba całkowita > 0| nic
|ncols |dowolna liczba całkowita > 0| nic
|npasm |dowolna liczba całkowita > 0| 1
|nbitów |1, 4, 8, 16, 32| 8
|kolejność bajtów| I = Intel;M = Motorola |taki sam jak komputer główny|
|układ| bil, bip, bsq| Bil|
|pomiń bajty| dowolna liczba całkowita ≥ 0| 0
|ulxmap |dowolna liczba rzeczywista| 0|
|ulymap |dowolna liczba rzeczywista |nrows - 1|
|xdim |dowolna liczba rzeczywista| 1
|ydim |dowolna liczba rzeczywista| 1
|bandrowbytes |dowolna liczba całkowita > 0| najmniejsza liczba całkowita ≥ (ncols x nbits) / 8|
|totalrowbytes |dowolna liczba całkowita > 0| dla bil: nbands x bandrowbytes;dla bip: najmniejsza liczba całkowita ≥ (ncols x nbands x nbits) / 8|
|bajty pasma pasma |dowolna liczba całkowita ≥ 0| 0|

## Bibliografia

* [Format pliku HRD — ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

