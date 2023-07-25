{
  "date" : "2019-10-11",
  "keywords" :[ "plik emz", "format pliku emz", "co to jest plik emz", "plik", "przykład emz", "rozszerzenie pliku emz", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku EMZ - Skompresowany ulepszony plik meta systemu Windows",
  "description":"Poznaj format pliku EMZ i interfejsy API, które mogą tworzyć i otwierać pliki EMZ.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Czym jest plik EMZ?

Plik z rozszerzeniem .emz to skompresowany kontener rozszerzonego metapliku (plik [EMF](/pl/image/emf/)). Są one kompresowane przy użyciu techniki kompresji [GZIP](/pl/compression/gz/), która jest powszechnie stosowaną metodą kompresji w systemach operacyjnych UNIX i LINUX. Unlink ZIP (/pl/compression/zip/), GZIP kompresuje archiwum jako całość, zamiast kompresować poszczególne pliki. Pliki EMZ są mniejsze w porównaniu z plikami EMF i pomagają w szybkim przesyłaniu podczas udostępniania plików online. Niektóre aplikacje, które mogą otwierać pliki EMZ, to Microsoft Visio 2019, Microsoft Office 2019, XnView MP i File Viewer Plus.

## Format pliku EMZ

Pliki EMZ są skompresowane [Gzip](/pl/compression/gz/) i zawierają wewnątrz [EMF](/pl/image/emf/). Gzip używa algorytmu DEFLATE do kompresji archiwum i różni się w stosowaniu kompresji. Plik EMZ można rozpakować za pomocą narzędzi do kompresji GZip, takich jak GNU Zip. Format pliku składa się z:

* Nagłówek pliku
* Opcjonalne nagłówki
* Skompresowane dane
* Stopka pliku

Format pliku GZIP [wersja specyfikacji 4.3](https://datatracker.ietf.org/doc/html/rfc1952) opublikowany przez Internet Engineering Task Force (IETF) zawiera szczegółowe informacje o formacie pliku.

## Bibliografia

* [RFC1952: specyfikacja formatu pliku GZIP](https://datatracker.ietf.org/doc/html/rfc1952), przez [IETF](https://www.ietf.org/)
* [Metaplik systemu Windows – Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

