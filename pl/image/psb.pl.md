{
  "date" : "2019-10-11",
  "keywords" :[ "plik psb", "format pliku psb", "co to jest plik psb", "plik", "przykład psb", "rozszerzenie pliku psb", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB — format dużego pliku obrazu programu Photoshop",
  "description":"Poznaj format pliku PSB i interfejsy API, które mogą tworzyć i otwierać pliki PSB.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik PSB?
Adobe Photoshop zapisuje pliki w dwóch formatach. Pliki o rozmiarze 30 000 na 30 000 pikseli są zapisywane z rozszerzeniem PSD, a pliki większe niż PSD do 300 000 na 300 000 pikseli są zapisywane z rozszerzeniem PSB znanym jako „Photoshop Big”. Mówiąc dokładniej, pliki PSB mogą mieć rozmiar nawet 4 EB (ponad 4,2 miliarda GB) z obrazami o wysokości i szerokości do 300 000 pikseli. Z drugiej strony pliki PSD mogą mieć maksymalnie 2 GB i wymiary obrazu 30 000 pikseli.

PSB jest również znany jako rozmiar dużego formatu dla Photoshopa i obsługuje wszystkie funkcje Photoshopa, takie jak warstwy, efekty i filtry. Photoshop może konwertować plik PSB do formatu [PSD](/pl/image/psd/), [JPG](/pl/image/jpeg/) , [PNG](/pl/image/png/), [EPS](/pl/page-description-language/eps/), [GIF](/pl/image/gif/) oraz inne formaty. Duży format dokumentu programu Photoshop jest dostępny po włączeniu funkcji panelu obsługi plików w oknie dialogowym preferencji programu Photoshop.

## Informacje o formacie pliku ##

Format pliku programu Photoshop jest podzielony na pięć głównych części z wieloma znacznikami długości do przemieszczania się między sekcjami.

|Format pliku
---|
|Nagłówek pliku
|Dane trybu koloru
| Zasoby obrazu
|Informacje o warstwie i masce
|(((
Dane obrazu
)))

### Nagłówek pliku ###

Nagłówek pliku ma stałą długość 26 bajtów i zawiera podstawowe właściwości obrazu.

Sygnatura BYTE [4] – Odpowiada '8BPS'.

WORD Wersja [2] – Numer wersji, PSD nr 1, PSB nr 2.

BYTE Zarezerwowany [6] – Zarezerwowany i zawsze zero.

Kanały WORD [2] – Liczba kanałów kolorów w obrazie, w tym kanały alfa. Jego wartość waha się od 1 do 56.

LONG Rows [4] – Wysokość obrazu w pikselach, PSD 1-30 000, PSB 1-300 000.

Kolumny LONG [4] – Szerokość obrazu w pikselach, PSD 1-30 000, PSB 1-300 000.

WORD Depth [2] – Liczba bitów na kanał. Obsługiwane wartości to 1,8,16 i 32.

Tryb WORD [2] – Tryb koloru pliku.

#### Tryb Opis ####


|Tryb|Opis
---|---|
|0|Mapa bitowa (monochromatyczna)
|1|Skala szarości
|2|Indeksowane
|3|RGB
|4|CMYK
|7|Wielokanałowy
|8|Bichromia (półtony)
|9|Laboratorium

### Dane trybu koloru ###

Po sekcji nagłówka pliku następuje sekcja danych trybu koloru. Blok zaczyna się od LONG Number, która podaje długość bloku w bajtach. Struktura danych trybu koloru jest następująca:

4 bajty — długość następujących danych kolorów.

Zmienna — dane koloru

Jeśli wartość pola trybu w sekcji nagłówka nie jest Kolorem indeksowanym ani bichromią, długość bloku będzie równa 0 i po polu długości nie będzie żadnych danych.

W przypadku obrazów w kolorze indeksowanym długość będzie wynosić 768 bajtów, co będzie zawierać paletę 256 kolorów. W przypadku bichromii dane będą zawierać parametry ekranu i inne powiązane informacje.

### Zasoby obrazów ###

Po sekcji danych trybu koloru trzeci blok to sekcja zasobów obrazu. Pierwsze cztery bajty to liczba LONG określająca długość bloku, po której następuje seria bloków zasobów. Struktura bloku zasobów obrazu jest następująca:

Typ BYTE [4] – Podpis '8BIM'

WORD ID [2] – Identyfikator zasobu obrazu. Istnieje lista identyfikatorów zasobów, które można zobaczyć, klikając łącze referencyjne.

BYTE Nazwa [Zmienna] – Nazwa: Ciąg Pascala o parzystej długości. ** **

LONG Size [4] – Rzeczywisty rozmiar następujących danych zasobów.

BYTE Dane [Zmienna} – Dane zasobu. Jest wyściełany, aby uzyskać równy rozmiar.

Niektóre formaty zasobów są pokrótce wyjaśnione poniżej:

**Format zasobów siatki i prowadnic:** Informacje o siatkach i prowadnicach są przechowywane w bloku zasobów. Te bloki zasobów zawierają 16-bajtową siatkę i nagłówek prowadzący, po których następują 5-bajtowe bloki informacji prowadzącej.

**Format zasobów miniatur:** Informacje o miniaturach są przechowywane w bloku zasobów obrazu do wyświetlania podglądu, który składa się z 28-bajtowego nagłówka i miniatury JFIF w RGB.

**Format zasobów próbników kolorów:** Informacje o próbnikach kolorów są przechowywane w bloku zasobów obrazu z 8-bajtowym nagłówkiem, po którym następuje blok informacji o próbnikach kolorów o zmiennej długości.

### Informacje o warstwie i masce ###

Czwarty blok jest blokiem informacji o warstwie i masce i zawiera informacje o warstwach i maskach. Najpierw zapisywane są informacje o warstwach, a następnie informacje o maskach.

**Informacje o warstwie:** Informacje o warstwie zaczynają się od wartości LONG, która pokazuje długość informacji o warstwie. Następnie następuje zliczanie wartości WORD, które pokazuje liczbę kolejnych rekordów warstw.

[8] – długość warstw

[2] – Liczba warstw

[Zmienna] – Informacje o każdej warstwie.

[Zmienna] – Dane obrazu kanału.** **

**Informacje o masce:** Struktura maski ma następujący format:


|Struktura danych|Nazwa pola| Opis
---|---|---|
|SŁOWO| Przestrzeń kolorów nakładki| (Nieudokumentowane)
|BAJT[8]| Komponenty kolorów| Komponenty koloru 4x2 bajty
|SŁOWO| Nieprzezroczystość| 0#przezroczysty, 1#nieprzezroczysty
|BAJT| miły| 0#odwrócone, 1#chronione, 128#użyj zapisanej wartości
|BAJT| wyściółka| ustawić na zero

### Dane obrazu ###

Ostatnia sekcja zawiera dane dotyczące pikseli obrazu. Dane obrazu są przechowywane jako seria sekwencji w płaszczyznach, tj. najpierw wszystkie dane czerwone, następnie wszystkie dane zielone itd. WORD na początku każdej linii pokazuje rozmiar w bajtach odnoszący się do każdej linii skanowania.

[2] – Metoda kompresji:

[Zmienna] – Dane obrazu w porządku planarnym, tj. RRRR, GGGG, BBBB itp.

Metody kompresji:

0 – Raw Dane obrazu

1 – RLE skompresowany

2 – Zip bez przewidywania

3 – Zip z przewidywaniem

## Odniesienie ##

* [Format pliku PSB — firma Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB – Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

