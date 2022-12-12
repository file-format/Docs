{
  "date" : "2020-08-20",
  "keywords" :["plik fon", "format pliku fon", "co to jest plik fon", "plik", "przykład fon", "rozszerzenie pliku fon", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Plik biblioteki czcionek",
  "description":"Dowiedz się o formacie plików FON i interfejsach API, które mogą tworzyć i otwierać pliki FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Czym jest plik FON?

Plik z rozszerzeniem .fon to biblioteka czcionek systemu Microsoft Windows 3.x, która w rzeczywistości jest plikiem wykonywalnym, ale zmieniono jej nazwę na .fon. Jest to sam w sobie zbiór plików [.fnt](/pl/font/fnt/), a aplikacje odwołują się do niego podczas uzyskiwania dostępu do czcionek systemowych. Dlatego działa jako plik zasobów. Można go otworzyć w systemie operacyjnym Windows za pomocą aplikacji Microsoft Windows Font View.

## Format pliku FON

Plik FON zawiera zasoby czcionek i ma format pliku Resource (.res). Format pliku .res określa nagłówek pliku oraz specyfikacje sekcji danych. .fnt to także plik danych zasobów, który jest dołączony do pliku zasobów. Pliki FON mają format binarny i typ MIME application/octet-stream.

Zasoby czcionek, w przeciwieństwie do innych typów zasobów, nie są dodawane do zasobów aplikacji. Zamiast tego są one dodawane do plików EXE i zmieniane ich nazwy na pliki .fon, co skutkuje plikami bibliotek zamiast aplikacji. Wiele pojedynczych czcionek stanowi składniki grupy czcionek, w której każda grupa jest zgodna ze strukturą grupy zasobów. Zasoby czcionek używają tych struktur grup zasobów. Nagłówek grupy zawiera wszystkie informacje wymagane do uzyskania dostępu do określonej czcionki z grupy. Zasób komponentu czcionki ma następujący format.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/pl/font/fnt/) file)
```
Pojedynczy plik zasobów .rc może mieć mieszane deklaracje zasobów. Grupy czcionek mogą znajdować się w dowolnym miejscu pliku zasobów i nie muszą być ciągłe. Programy tworzące pliki .RES muszą koniecznie dodać ręczne wprowadzanie FONTDIR. Poniżej przedstawiono strukturę nagłówka grupy.

```
[Zwykły nagłówek zasobu (typ = 7)]

WORD Liczba czcionek; // Całkowita liczba w pliku .RES
```     
The remaining data is repeated for every font in the .RES file.

```
Czcionka WORD Porządkowa;
struct FontDirEntry {
WORD dfVersion;
DWORD rozmiar df;
char dfCopyright[60];
WORD typ df;
WORD dfPunkty;
WORD dfVertRes;
WORD dfHorizRes;
SŁOWO dfAscent;
WORD dfInternalLeading;
WORD dfZewnętrznyProwadzący;
BYTE dfKursywa;
BYTE dfPodkreślenie;
BYTE dfStrikeOut;
WORD dfWaga;
BYTE dfCharSet;
WORD dfPixWidth;
WORD dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfŚrSzerokość;
WORD dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfWidthBytes;
DWORD dfUrządzenie;
DWORD dftwarz;
DWORD dfZarezerwowane;
char szNazwaUrządzenia[];
char szNazwaTwarzy[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

