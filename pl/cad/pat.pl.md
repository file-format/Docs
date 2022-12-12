{
  "date" : "2020-03-16",
  "keywords" :["Plik PAT", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku PAT i interfejsy API, które mogą tworzyć i otwierać pliki PAT.",
  "title" :"Format Pliku PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Czym jest plik PAT?

Plik z rozszerzeniem .pat to plik CAD używany przez oprogramowanie AutoCAD. Aplikacje, które mogą otwierać pliki PAT, używają wzoru kreskowania zapisanego w tych plikach, aby uzyskać informacje o teksturze / wypełnieniu obszaru. Zawarte wzorce dostarczają informacji o wyglądzie materiału rysowanych obiektów. Pliki PAT można otwierać w aplikacjach takich jak Autodesk AutoCAD, CorelDRAW Graphics Suite i Ketron Software. Pliki PAT można konwertować do różnych formatów graficznych, takich jak JPG, PNG, BMP itp.

## Format pliku PAT

Pliki PAT są zapisywane w formacie zwykłego tekstu i można je otwierać w dowolnym edytorze tekstu. Wzory kreskowania w tych plikach są oparte na wektorach i są zgodne ze składnią opisaną w dokumentacji programu AutoCAD.

Wszystkie wzory zaczynają się w punkcie 0,0, wzór jest obliczany tak, aby obejmował granicę kreskowania.

### Definicja wzoru

Wszystkie definicje wzorców składają się z następujących pól:
* Wiodący '\*'
* Nazwa — nazwa nie może zawierać spacji, znaków interpunkcyjnych, nawiasów ani ukośników.
* Opis

Standardowym formatem wzorów kreskowania jest `<\*><name> <, opis>`. Nazwa i opis oddzielone są przecinkiem, a długość linii opisu nie może przekraczać osiemdziesięciu znaków. Wzory kreskowania są definiowane po tej informacji.

### Przykłady wzorów kreskowania
Poniżej znajduje się przykład kwadratowego wzoru
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Inny przykład przedstawiający wzór równoległoboku jest następujący.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Bibliografia ##

* [Wzorce mieszania firmy Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

