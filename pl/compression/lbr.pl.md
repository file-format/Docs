{
  "date" : "2021-04-08",
  "keywords" :[ "plik mst", "format pliku mst", "co to jest plik mst", "plik", "przykład mst", "rozszerzenie pliku mst", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - Format pliku archiwum biblioteki LU",
  "description":"Poznaj format pliku LBR i interfejsy API, które mogą tworzyć i otwierać pliki LBR.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Czym jest plik LBR?

Plik z rozszerzeniem .lbr to plik archiwum utworzony za pomocą programu LU i używany w systemach operacyjnych CP / M i DOS w latach 80. Nie jest już używany i został zastąpiony nowoczesnymi formatami plików archiwizacji. Format nie kompresuje plików członkowskich i działa dla nich jako archiwum kontenerów. Funkcja archiwizacji była używana głównie do przesyłania zarchiwizowanych plików przez Internet. Ponieważ LBR nie oferował kompresji, inne narzędzia, takie jak SQ lub CRUNCH, były używane do kompresji plików członkowskich przed archiwizacją lub po archiwizacji wynikowego pliku archiwum w celu zmniejszenia jego rozmiaru.

## Format pliku LBR

Format pliku LBR został zaprojektowany przez Gary'ego P. Novosielskiego i nie ma publicznie dostępnych szczegółów technicznych. Pliki LBR zaczynają się od bajtu 0x00, po którym następuje 11 spacji (0x20), następnie dwa bajty 0x00, a następnie dwa bajty, które nie są jednocześnie 0x00. Będąc formatem pliku kontenera, można go wyodrębnić za pomocą LU.COM i NULU.COM.

## Bibliografia

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))

