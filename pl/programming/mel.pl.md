{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Język osadzony Maya", "plik", "rozszerzenie", "format pliku", "Maya 3D", "Przewodnik po programowaniu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL — format pliku z osadzonym językiem Majów",
  "description":"Poznaj format pliku MEL i interfejsy API, które mogą tworzyć i otwierać pliki MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Czym jest plik MEL?

Plik z rozszerzeniem .mel (Maya Embedded Language) to język skryptowy używany przez Autodesk Maya do tworzenia interfejsów graficznych. Pozwala zautomatyzować tworzenie elementów graficznych za pomocą skryptów wykonywalnych oprócz interfejsu graficznego Maya. MEL umożliwia tworzenie interfejsów graficznych bez nauki programowania. Osiąga się to poprzez tworzenie makr i niestandardowych akcji, które przyspieszają powtarzalne zadania. Te procedury i skrypty pozwalają tworzyć niestandardowe modelowanie, animacje, dynamikę i renderowanie zadań. Programu Autodesk Maya 2020 można używać do otwierania i przeglądania zawartości pliku EML.

## Format pliku MEL — więcej informacji

[Podręcznik referencyjny] dla programistów (https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) jest dostępny dla programistów w sekcji dokumentacji programu Maya. MEL opiera się na poleceniach skryptów powłoki, podobnych do UINX, aby osiągnąć różne cele. Polecenia oparte na skryptach sprawiają, że nie ma to znaczenia dla programowania konwencjonalnego i obiektowego (OOP), co skutkuje brakiem użycia struktur danych, wywoływania funkcji lub używania OOP, jak w innych językach.

Niektóre kluczowe punkty dotyczące MEL są następujące.

`Komentarze` - Każda instrukcja w MEL musi kończyć się średnikiem (;), nawet na końcu bloku.

`Zwracanie wartości` — podanie wyrażenia, które zwraca wartość, nie powoduje automatycznego wydrukowania wartości w MEL. Zamiast tego powoduje błąd.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Polecenia dotyczące tworzenia, edytowania i usuwania` — to samo polecenie służy do tworzenia, edytowania lub wyszukiwania informacji o istniejących rzeczach. Jednak flaga kontroluje, co robi polecenie (tworzenie, edytowanie lub zapytanie).

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Zwróć wartość z funkcji` — składnia funkcji automatycznie zwraca wartość. Aby uzyskać wartość zwracaną przy użyciu składni polecenia, należy ująć polecenie w cudzysłowy.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Bibliografia

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

