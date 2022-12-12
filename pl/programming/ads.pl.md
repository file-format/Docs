
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik ADS - Format pliku specyfikacji Ada",
  "description":"Dowiedz się, czym jest format pliku ADS, z przykładami i interfejsami API, które mogą tworzyć i otwierać pliki ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Czym jest plik ADS?

Plik ADS to plik specyfikacji dla projektu programistycznego Ada. Jest to podobne do klasy dla Javy lub pary nagłówka i implementacji w przypadku C++. Publiczne i prywatne specyfikacje pakietu Ada są przechowywane w pliku .ads. Natomiast plik .adb zawiera implementację, czyli ciała Ada. Podobnie jak [C++](/pl/programming/cpp/), Ada oferuje separację specyfikacji i implementacji niezależnie od OOP.

Pliki ADS można otwierać w dowolnym edytorze tekstu, takim jak Microsoft Notepad, Notepad ++ i Atom.

## Format pliku ADS

Pliki ADS są w prostym formacie zwykłego pliku tekstowego i można je otwierać / edytować za pomocą dowolnego edytora tekstu. Pakiety Ada można organizować w hierarchie. Jednostkę podrzędną można zadeklarować w następujący sposób:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Bibliografia

* [Pakiety Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

