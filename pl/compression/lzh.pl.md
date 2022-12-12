{
  "date" : "2021-06-16",
  "keywords" :["LZH", "Skompresowany", "Plik", "Rozszerzenie", "Format pliku", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku LZH",
  "description":"Dowiedz się o formacie pliku LZH i interfejsach API, które mogą tworzyć i otwierać pliki LZH.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Czym jest plik LZH? ##

Plik z rozszerzeniem .lzh i .lha zwykle odnosi się do formatu pliku kompresji archiwum. Ten format pliku jest taki sam jak inne formaty kompresji plików, takie jak [ZIP](/pl/compression/zip/), [RAR](/pl/compression/rar/) itp. Głównym celem tych formatów plików jest zmniejszenie rozmiaru formacie do łatwego wysyłania, a także do przechowywania ich razem w formie skompresowanej. AS w porównaniu do innych zachodnich firm Pliki LZH są bardzo popularne w Japonii i zwykle używane do kompresji danych gier wideo. Dodatek LZH dla systemu Windows 7 jest wbudowany w japońską wersję systemu Windows 7. Firma Microsoft jako pierwsza wydała dodatek Microsoft Compressed (LZH) Folder Add-on dla japońskiej wersji systemu Windows XP. Ten format pliku jest zaimplementowany z uwzględnieniem kompresji i funkcji używanych przez algorytm Lempel-Ziv i Haruyasu

## Specyfikacja LZH ##

Metoda kompresji archiwum LZH jest pokazana jako pięciobajtowy ciąg tekstowy, na przykład -lz1-. Są to bajty od trzeciego do siódmego w skompresowanym pliku.

|Specyfikacja|Opis|
---|---|
|Rozszerzenie | .lzh, .lha|
|Typ nośnika| application/x-lzh-skompresowane|
|Kod typu| "LHA_" (LHA-PRZESTRZEŃ)|
|UTI| archiwum.publiczne.lha|
|Opracowany przez| Haruyasu Yoshizaki (Yoshi)|
|Wpisz| Kompresja|
|Rozszerzony od| LArc|

## Problemy z otwarciem pliku LZH ##

Poniżej przedstawiono kilka problemów, które mogą powodować słabe działanie formatu pliku LZH:
  

* Plik może być uszkodzony. Aby rozwiązać ten problem, ponownie pobierz plik lub poproś nadawcę o ponowne wysłanie pliku
* Drugim powodem jest zainfekowany plik, w tym przypadku przeskanuj plik poprawnie
* Niewłaściwe linki do pliku LZH
* Usunięcie opisu LZH
* Za mało zasobów sprzętowych
* Nieaktualne sterowniki sprzętu

## Bibliografia ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
