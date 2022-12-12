{
  "date" : "2021-04-08",
  "keywords" :[ "plik rpm", "format pliku rpm", "co to jest plik rpm", "plik", "przykład rpm", "rozszerzenie pliku rpm", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - plik menedżera pakietów Red Hat",
  "description":"Dowiedz się o formacie pliku RPM i interfejsach API, które mogą tworzyć i otwierać pliki RPM.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Czym jest plik RMP?

Plik z rozszerzeniem .rpm to pakiet systemu operacyjnego Red Hat Linux do instalacji programów w systemach Linux. Menedżer pakietów Red Hat używa formatu pliku RPM i jest darmowym systemem zarządzania pakietami typu open source. Chociaż pliki RPM mogą być używane do instalacji programów, można je konwertować na inne formaty pakietów, takie jak [DEB](/pl/compression/deb/) za pomocą programu Debiana o nazwie Alien.

## Format pliku RMP

Plik RPM to plik binarny, który może zawierać zestaw plików. W większości przypadków pliki RPM to „binarne RPM”, które są skompilowanymi plikami wykonywalnymi oprogramowania. Plik RPM może zawierać źródłowe pakiety RPM (SRPM), których można użyć do zbudowania pakietu z kodu źródłowego. Format pliku RPM składa się z czterech sekcji.

* Lead — identyfikuje plik jako plik RPM
* Podpis — może służyć do zapewnienia integralności i/lub autentyczności
* Nagłówek — zawiera metadane, w tym nazwę pakietu, wersję, architekturę, listę plików itp.
* Archiwum plików — znane również jako ładunek, zwykle w formacie cpio, skompresowane za pomocą [GZIP](/pl/compression/gz/)

## Bibliografia

* [RPM - Wikipedia](https://rpm.org)
* [Dokumentacja RPM](https://rpm.org/documentation.html)

