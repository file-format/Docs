{
  "date" : "2021-04-08",
  "keywords" :[ "plik pkg", "format pliku pkg", "co to jest plik pkg", "plik", "przykład pkg", "rozszerzenie pliku pkg", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - rozszerzalny format pliku archiwum",
  "description":"Poznaj format pliku PKG i interfejsy API, które mogą tworzyć i otwierać pliki PKG.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Czym jest plik PKG?

Plik z rozszerzeniem .pkg to plik pakietu instalacyjnego, który służy do instalowania oprogramowania w systemie macOS. Oprócz komputerów Macintosh jest również używany na iPhonie. Wbudowana aplikacja instalatora Apple może być wykorzystana do zainstalowania zawartości pliku PKG. Plik PKG jest podobny do pliku MSI używanego w systemie operacyjnym Windows do instalacji oprogramowania. Podczas instalacji te pliki pakietów mogą rejestrować komunikaty, które dają wyobrażenie o tym, jakie dodatkowe rzeczy są instalowane przez ten pakiet.

## Format pliku PKG

PKR to pliki binarne, które są kompresowane w celu zmniejszenia ogólnego rozmiaru pliku. Od wersji OSX 10.5 firma Apple wprowadziła płaskie pakiety z pojedynczymi plikami instalacyjnymi. Różnią się one od wcześniejszych formatów opakowań, które były dostarczane jako pakiety, a nie jako pojedyncze pliki. Te dołączone pakiety zawierały uporządkowaną hierarchię katalogów, w której przechowywane były pliki w sposób ułatwiający ich odzyskiwanie za pomocą pliku indeksu. Płaski format pliku PKG to tak naprawdę archiwum [XAR](/pl/compression/xar/), które ma:

* Nagłówek — określa rozmiar, sumę kontrolną i informacje o wersji
* Spis treści — dokument XML, który jest (i musi) być zakodowany jako UTF-8 i jest przechowywany na początku pliku, co ułatwia przeglądanie archiwum w celu wyodrębnienia pojedynczego pliku
* Sterta — nieustrukturyzowana sterta danych, do których odwołuje się spis treści

## Bibliografia

* [Format pliku pakietu płaskiego](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

