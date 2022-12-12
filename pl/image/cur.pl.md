{
  "date" : "2021-06-29",
  "keywords" :["CUR", "rozszerzenie", "plik", "format", "obraz", "Mapa bitowa niezależna od urządzenia", "Format pliku kursora", "Kursor", "Windows", "aplikacja"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - Format pliku kursora",
  "description":"Poznaj format pliku CUR i interfejsy API, które mogą tworzyć i otwierać pliki CUR.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Czym jest plik CUR? ##

Plik CUR to statyczny format pliku kursora systemu Microsoft Windows. Zasadniczo są to stacjonarne obrazy identyczne z plikami ICO (ikona) pod każdym względem, z wyjątkiem rozszerzenia. Zarówno CUR, jak i [ICO](/pl/image/ico/) są tworzone na podstawie specyfikacji Device-Independent Bitmap [DIB](/pl/image/dib/) (Device-Independent Bitmap). Domyślny, jak również niestandardowy kursor, taki jak wskaźnik myszy Windows dla systemu operacyjnego Windows, są przechowywane w plikach CUR. Może to być strzałka do normalnego użytku, obracająca się klepsydra do demonstrowania okresów oczekiwania lub I-bar do edycji tekstu. Pliki CUR są dostarczane wraz z pakietem instalacyjnym niestandardowych motywów pulpitu, aby upewnić się, że kursor systemu Windows pasuje do niestandardowego motywu pulpitu.

## Specyfikacja techniczna ##

Pliki CUR są binarnymi plikami systemowymi, które spotkać można na urządzeniach działających pod kontrolą systemu operacyjnego Microsoft Windows. Obrazy wskaźników CUR są dostępne w różnych standardowych rozmiarach, takich jak 16 × 16, 32 × 32 itp. Pliki CUR są bardzo podobne do plików ICO; oba składają się z małych nieruchomych obrazów. Różnią się jedynie rozszerzenia plików CUR oraz ICO. Ponadto wyjaśnienie hotspotu w nagłówku pliku CUR różni się od pliku ICO. Hotspot interpretuje przesunięcie pikseli od lewego górnego rogu do miejsca, w które wskazujesz myszą. Systemy Windows nadal używają plików CUR, ale teraz animowane kursory mają zwykle rozszerzenie pliku ANI zamiast CUR.

## Krótka historia ##

Plik CUR jest tworzony z pliku ICO. Pierwszy format pliku CUR został włączony do systemu operacyjnego Microsoft Windows 1.0 w 1981 r., aby ułatwić komercyjne wykorzystanie. Wkrótce wprowadzono więcej interaktywnych kursorów, umożliwiając użytkownikom zmianę preferencji kursora za pomocą dostępnych fabrycznie opcji. Samodzielna edycja pliku CUR jest jednak łatwa, nawet jeśli nie masz wystarczającej wiedzy technicznej.


## CUR Przykład ##

Pliki CUR można znaleźć w *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="Format pliku CUR" >}}

