{
  "date" : "2021-06-16",
  "keywords" :["LZO", "Skompresowany", "Plik", "Rozszerzenie", "Format pliku", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku LZO",
  "description":"Dowiedz się o formacie pliku LZO i interfejsach API, które mogą tworzyć i otwierać pliki LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Czym jest plik LZO? ##

Plik z rozszerzeniem .lzo jest połączony z funkcjami archiwizacji plików, które mogą zmniejszyć rozmiar wszystkich plików w skompresowanym pliku. Wszystkie skompresowane pliki mogą składać się z jednego lub więcej plików lub nawet grup segregatorów z kilkoma plikami różnego rodzaju i rozmiarów. Rozmiar skompresowanego pliku jest mniejszy w porównaniu do łącznego rozmiaru wszystkich plików i folderów przechowywanych w skompresowanym pliku LZO. Wszystkie skompresowane pliki LZO są przechowywane w formacie LZO i są jawnie wykonywane z funkcjami kompresji używanymi przez oprogramowanie do kompresji i dekompresji plików LZO. Wszystkie specyfikacje kompresji są połączone w ten program do kompresji i dekompresji plików, który pochodzi z biblioteki kompresji plików Lempel-Ziv-Oberhume. Większa prędkość dekompresji i rozwinięte współczynniki kompresji są również łączone w te pliki LZO.

## Specyfikacja LZO ##

Markus Franz Xaver Johannes Oberhumer opracował oryginalny algorytm „lzop”, oparty na wcześniejszych algorytmach Abrahama Lempla i Jacoba Ziva, w 1996 roku. Ta biblioteka implementuje różnorodne algorytmy o następujących cechach:

* Szybsza kompresja niż DEFLATE
* Szybka dekompresja
* Dodatkowe bufory potrzebne podczas kompresji (o wielkości 8 KB lub 64 KB, w zależności od poziomu kompresji)
* Bufory źródłowy i docelowy to cała pamięć wymagana do dekompresji
* Zapewnia kontrolę zarówno nad współczynnikiem kompresji, jak i szybkością kompresji

Jako algorytm kompresji blokowej, LZO wykonuje kompresję nakładającą się, jak również dekompresję w miejscu. Aby uzyskać nakładającą się kompresję, rozmiar bloku zarówno kompresji, jak i dekompresji musi być taki sam. Algorytm kompresji LZO dzieli dane wejściowe na dopasowania (słownik przesuwny) i literały, które nie pasują, dając dobre wyniki z wysoce redundantnymi danymi i akceptowalne wyniki z danymi nieskompresowanymi, zwiększając dane nieskompresowane tylko o 1/64 oryginału rozmiar.

## Problemy z otwarciem pliku LZO ##

Poniżej przedstawiono kilka problemów, które mogą powodować słabe działanie formatu pliku LZO:
  


* Plik może być uszkodzony. Aby rozwiązać ten problem, ponownie pobierz plik lub poproś nadawcę o ponowne wysłanie pliku
* Drugim powodem jest zainfekowany plik, w tym przypadku przeskanuj plik poprawnie
* Niewłaściwe linki do pliku LZO
* Usunięcie opisu LZO
* Za mało zasobów sprzętowych
* Nieaktualne sterowniki sprzętu
  


## Bibliografia ##

* [LZO – przez Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

