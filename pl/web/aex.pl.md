{
  "date" : "2019-10-11",
  "keywords" :[ "aex","plik aex", "format pliku", "typ pliku", "co to jest plik aex" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AEX - skompilowany plik globalnych funkcji Alpha Five",
  "description" :"Dowiedz się, co to jest plik AEX i interfejsy API, które mogą tworzyć i otwierać pliki AEX.",
  "linktitle" : "AEX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-07"
}

## Czym jest plik AEX?

Plik AEX (z rozszerzeniem .aex) to skompilowany plik [Xbasic](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml), który zawiera skompilowany kod programu dla funkcji globalnych. Można go używać w aplikacjach internetowych, wywołując je od strony serwera [.a5w](/pl/web/a5w/). Pliki AEX zostały załadowane i rozładowane przez wywołanie odpowiednio funkcji a5w_load_aex i a5w_unload_aex z plików A5W. Jednak w nowej implementacji pliki te są ładowane do pamięci przez włączenie do pliku a5_application.5i. Język programowania Xbasic jest używany przez oprogramowanie Alpha Anywhere do tworzenia aplikacji mobilnych i internetowych.

## Format pliku AEX — więcej informacji

Pliki AEX są zapisywane na dysku w formacie pliku binarnego i zawierają skompilowany kod funkcji napisanych w Xbasic. Instrukcje poleceń skryptu Xbasic określają strukturę i przebieg wykonywania, w tym wykonywanie lub zatrzymywanie powtarzanej akcji lub dokonywanie wyboru pomiędzy dwoma lub więcej krokami w oparciu o warunki. [Xbasic Language Reference](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml) można znaleźć w celu uzyskania szczegółowych informacji na jego temat.

## Bibliografia

* [Alpha Five](https://www.alphasoftware.com/)
* [Dokumentacja Alpha Five](https://documentation.alphasoftware.com/documentation/pages/index.html)
* [Podręcznik Xbasic](https://documentation.alphasoftware.com/pages/Guides/Xbasic/index.xml)

