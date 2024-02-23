{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AVL — plik legendy ArcView",
  "description":"Dowiedz się o formacie pliku AVL i interfejsach API, które umożliwiają tworzenie i otwieranie plików AVL.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl-pl",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## Czym jest plik AVL?

Plik AVL to plik legendy zawierający klucz do mapy wygenerowanej za pomocą oprogramowania ESRI ArcView GIS (System informacji geograficznej). Zawiera informacje o symbolice referencyjnej używane na odpowiedniej mapie w celu uzyskania dostępu. Plik AVL może zawierać więcej informacji, takich jak symbolika, ustawienia wyświetlania, takie jak przezroczystość, właściwości wyświetlania zależne od skali, informacje o połączonej tabeli/powiązanej tabeli, zapytanie o definicję, właściwości etykietowania dla warstw obiektowych i właściwości wyświetlania adnotacji dla warstw adnotacji w zależności od typu rodzaj warstwy.

Do pliku AVL można odwoływać się z pliku projektu ArcView [.APR](/gis/apr/).

## Format pliku AVL — więcej informacji

Pliki AVL są zapisywane w formacie zwykłego pliku tekstowego. Oznacza to, że możesz otwierać pliki AVL w dowolnym edytorze tekstu, takim jak Notatnik, Notepad ++ i Apple TextEdit. Po otwarciu możesz nie tylko przeglądać zawartość pliku, ale także ją modyfikować.

### Różnica między plikami .LYR i .AVL

 * **Różnica w formacie pliku** – .lyr to plik binarny, natomiast .avl to plik tekstowy
 * **Różnica w zawartości** — plik .lyr zawiera więcej informacji niż plik .avl. Plik AVL przechowuje tylko informacje o symbolice, podczas gdy plik LYR przechowuje wszystkie informacje dostępne w oknie dialogowym właściwości warstwy w ArcMap.

## Bibliografia

* [Różnica między plikami .lyr i .avl](https://support.esri.com/en/technical-article/000005936)


