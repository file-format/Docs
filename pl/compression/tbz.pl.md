{
  "date" : "2019-10-11",
  "keywords" :["plik tbz", "format pliku tbz", "co to jest plik tbz", "plik", "przykład tbz", "rozszerzenie pliku tbz","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - skompresowane archiwum tar Bzip",
  "description":"Dowiedz się o formacie pliku TBZ i interfejsach API, które mogą tworzyć i otwierać pliki TBZ.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Czym jest plik TBZ?

Plik z rozszerzeniem .tbz to skompresowane archiwum, które wykorzystuje kompresję BZIP do zmniejszania rozmiaru plików zawartości. Pliki TBZ są w rzeczywistości zarchiwizowanymi plikami UNIX [TAR](/pl/compression/tar/), które następnie są kompresowane za pomocą BZIP. Najnowsza kompresja drugiego poziomu to [BZIP2](/pl/compression/bz2/), która zastąpiła BZIP. Format pliku TBZ jest odpowiedni do przesyłania dużych plików. Pliki TBZ można otwierać / wyodrębniać za pomocą aplikacji, takich jak 7-Zip, PeaZip i jZip. Użytkownicy systemów Linux i macOS mogą również otwierać TBZ za pomocą polecenia BZIP2 z okna terminala.

## Format pliku TBZ

Pliki TBZ to w rzeczywistości skompresowane archiwa utworzone za pomocą kompresji BZIP/[BZIP2](/pl/compression/bz2). Dla tego formatu pliku nie są dostępne żadne formalne specyfikacje. Jednak nieoficjalne [specyfikacje poddane inżynierii wstecznej](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) pokazują, że strumień .bz2 składa się z 4-bajtowego nagłówka, po którym następuje przez zero lub więcej skompresowanych bloków.

## Bibliografia ##

* [Specyfikacje formatu BZIP2] (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

