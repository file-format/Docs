{
  "date" : "2021-03-11",
  "keywords" :["APNX", "Indeks numerów stron Amazon", "rozszerzenie", "plik", "format", "eBook", "Amazon Kindle"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie pliku Amazon APNX i interfejsach API, które mogą tworzyć i otwierać pliki APNX.",
  "title" :"APNX - indeks numerów stron Amazon",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Czym jest plik APNX? ##

Plik Amazon Page Number Index, który używa rozszerzenia .apnx, jest typem pliku eBook; używany przez Amazon Kindle. Pliki te są w rzeczywistości znane jako pliki stronicowania używane przez urządzenia Kindle. Tak więc pliki APNX są zwykle tworzone w celu oznaczania stron eBooków Kindle. Funkcja paginacji została uruchomiona na urządzeniach Amazon Kindle od czasu oprogramowania układowego 3.1. Sprawdza plik APNX w poszukiwaniu indeksów stron, a następnie odwzorowuje go na numery stron w oryginalnej książce drukowanej. Pliki te są zapisywane na urządzeniach Kindle wraz z plikami Amazon eBooks. Nie możesz otwierać ani edytować plików APNX.

## Specyfikacje formatu pliku APNX ##

### Układ

|bajty| zawartość| komentarze|
---|---|---|
|4 |00010001 | Identyfikator formatu. Wartość 65537 little-endian.|
|4 |początek następnego | Przesunięcie po końcowej lokalizacji pierwszego nagłówka. Rozpoczyna nową sekwencję nagłówka info|
|4 |długość| Długość pierwszego nagłówka|
|N |pierwszy nagłówek | Ciąg zawierający nagłówek treści. Rozpoczyna następną sekwencję|
|2 |nieznane | Zawsze 1|
|2 |długość | Długość drugiego nagłówka|
|2 |liczba stron | Całkowita liczba bajtów po drugim nagłówku reprezentujących strony. Ta suma zawiera bajty, które są ignorowane przez pageMap.|
|2 |nieznane | Zawsze 32|
|N |drugi nagłówek | Ciąg zawierający nagłówek mapowania strony|
|4*N |wypełnienie | Pierwsza liczba podana w nagłówku odwzorowania strony oznacza liczbę bajtów 0.|
|4*N |lista stron ||

### Nagłówek treści

Nagłówek treści składa się z łańcucha zamkniętego w {} zawierającego pary klucz, wartość:

|zawartość| komentarze|
---|---|
|guid zawartości| Przewodnik.|
|jak | Identyfikator Amazon dla wersji książki Kindle.|
|cdeTyp | MOBI cdeTyp. Powinien być zawsze EBOK dla e-booków.|
|identyfikator wersji pliku | Wersja tego pliku.|

#### Przykład
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Nagłówek mapowania strony
Nagłówek mapowania strony składa się z ciągu znaków zamkniętego w {} zawierającego pary klucz-wartość.

|zawartość | komentarze|
---|---|
|jak | ISBN 10 książki papierowej, której odpowiadają strony|
|Mapa strony| Krotka o trzech wartościach. Wygląda jak: "(N,N,N)\
1) Liczba bajtów po nagłówku rozpoczynającym sekwencję numeracji stron\
2) nieznany\
3) nieznany\|
#### Przykład
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Lista stron

Lista stron to sekwencja przesunięć w surowym kodzie HTML. Każdy
wartość to początek nowej strony. Każdy wpis to 4-bajtowy big endian
int.



## Bibliografia

* [Format pliku Amazon APNX] (https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX — autorstwa MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

