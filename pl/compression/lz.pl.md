{
  "date" : "2021-04-08",
  "keywords" :[ "plik lz", "format pliku lz", "co to jest plik lz", "plik", "przykład lz", "rozszerzenie pliku lz", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Format skompresowanego pliku Lzip",
  "description":"Dowiedz się o formacie pliku LZ i interfejsach API, które mogą tworzyć i otwierać pliki LZ.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Czym jest plik LZ?

Plik z rozszerzeniem .lz to skompresowany plik archiwum utworzony za pomocą Lzip, który jest darmowym narzędziem wiersza poleceń do kompresji. Obsługuje konkatenację w celu kompresji plików pomocniczych. Pliki LZ mają typ nośnika application/lzip i obsługują wyższe współczynniki kompresji niż [BZ2](/pl/compression/bz2/). LZ są oparte na algorytmie LZMA (łańcuch Lempel-Ziv-Markov) i zawierają 32-bitową sumę kontrolną CRC oraz bajty identyfikacyjne do sprawdzania integralności pliku.

## Format skompresowany LZMA

Skompresowany format LZMA składa się ze skompresowanego strumienia bitów, który jest kodowany przy użyciu adaptacyjnego kodera zakresu binarnego. Strumień jest dzielony na pakiety. Każdy pakiet opisuje pojedynczy bajt lub sekwencję LZ77. Długość i odległość każdego pakietu jest zakodowana jawnie lub niejawnie.

Oto siedem rodzajów pakietów ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Kod spakowany (sekwencja bitów) |Nazwa pakietu |Opis pakietu|
---|---|---|
|0 + kod bajtowy| ŚWIECI| Pojedynczy bajt zakodowany przy użyciu adaptacyjnego kodera zakresu binarnego.|
|1+0 + dł. + odl.| MECZ| Typowa sekwencja LZ77 opisująca długość i odległość sekwencji.|
|1+1+0+0| KRÓTKI| Jednobajtowa sekwencja LZ77. Odległość jest równa ostatnio używanej odległości LZ77.|
|1+1+0+1 + długość| LONGREP[0]| Sekwencja LZ77. Odległość jest równa ostatnio używanej odległości LZ77.|
|1+1+1+0 + dł.| LONGREP[1]| Sekwencja LZ77. Odległość jest równa drugiej ostatnio użytej odległości LZ77.|
|1+1+1+1+0 + dł.| LONGREP[2]| Sekwencja LZ77. Odległość jest równa trzeciej ostatnio użytej odległości LZ77.|
|1+1+1+1+1 + dł.| LONGREP[3]| Sekwencja LZ77. Odległość jest równa czwartej ostatnio użytej odległości LZ77.|


## Bibliografia

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

