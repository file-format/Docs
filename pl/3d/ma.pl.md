{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma plik", "format pliku ma", "format pliku", "3d", "pobieranie pliku ma", "plik .ma", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku MA i interfejsy API, które mogą otwierać i tworzyć pliki MA.",
  "title" :"Format Pliku MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Czym jest plik MA?

Plik z rozszerzeniem .ma to plik projektu 3D utworzony za pomocą aplikacji Autodesk Maya. Zawiera obszerną listę poleceń tekstowych służących do określania informacji o pliku. Plik **.ma** można otworzyć i edytować w dowolnym edytorze tekstu, aby naprawić wszelkie problemy z poleceniami w przypadku uszkodzenia pliku. Pliki te zawierają informacje do definiowania informacji o scenie 3D, takich jak geometria, oświetlenie, animacja i renderowanie.

## Format pliku MA

Pliki MA są zapisywane na dysku w formacie tekstowym ASCII, w przeciwieństwie do plików MB, które są zapisywane na dysku w formacie binarnym. Szczegółowe odniesienie do formatu pliku MA jest dostępne w [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) i można się do niego odnieść do w celach informacyjnych dla programistów.

### Nagłówek pliku MA

Nagłówek pliku MA zaczyna się od sekcji komentarzy, która zawiera informacje o utworzeniu pliku i datę modyfikacji. Czytniki plików Maya ignorują ten blok, ponieważ jest on używany wyłącznie w celach informacyjnych. Nagłówek musi jednak zaczynać się od pierwszych sześciu znaków, takich jak „//Maya”.

Nagłówek pliku ASCII wygląda następująco.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Odnośniki do plików

Sekcja odniesień do pliku pliku .ma zawiera informacje o wszystkich innych plikach Maya, do których odwołuje się ten plik. Każdy plik, do którego istnieje odwołanie, można odczytać za pomocą pojedynczego polecenia pliku zawartego w tym samym pliku. Składnia polecenia file używanego do odwoływania się jest następująca:

```
file -r -rpr prefixString fileName;
```
lub

```
file -r -ns nameSpace fileName
```
Oto przykładowy ciąg.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Ten przykład pokazuje, że obiekt słońca zawarty w pliku `solar` byłby dostępny w tym pliku przy użyciu nazwy "solar_sun".

### Wymagania

Sekcja wymagań w pliku .ma składa się z serii wymaganych poleceń i zawiera informacje May, takie jak informacje o wersji i wtyczce, które są wymagane do odczytania plików. Przykładowa sekcja wymagań jest następująca.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Następna sekcja określa wymagania. Składa się z serii wymaganych poleceń. Ta sekcja pliku informuje Mayę, jakie oprogramowanie jest potrzebne do prawidłowego załadowania pliku. Konkretnie, jaka wersja Mayi i jakie wtyczki.

## Pobieranie pliku MA
Trochę trudno jest znaleźć i pobrać plik MA modelu 3D. Dlatego możesz pobrać przykładowy plik MA stąd:

- [Sample.ma](../sample.ma)


## Bibliografia

* [Organizacja plików Maya ASCII — Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

