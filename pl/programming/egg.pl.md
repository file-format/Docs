{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku EGG — plik dystrybucyjny Pythona",
  "description":"Poznaj format plików EGG i API, które mogą tworzyć i otwierać pliki EGG.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Czym jest plik EGG?

Plik EGG, znany również jako jaja Pythona, jest starszym formatem dystrybucji Pythona. Jest to skompresowane archiwum [ZIP](/pl/compression/zip/) z rozszerzeniem .egg i zawiera pliki źródłowe aplikacji Python wraz z metainformacjami o dystrybucji. Pliki EGG są alternatywą dla pliku Windows Executable [EXE](/pl/executable/exe/), ale są wieloplatformowe. Ten starszy format dystrybucji Pythona został zastąpiony nowszym formatem pliku Wheel (WHL) na początku 2010 roku.

## Format pliku EGG

Pliki EGG są zapisywane jako skompresowane archiwa ZIP. Oznacza to, że jeśli zamienisz rozszerzenie .egg na .zip, będziesz mógł je otworzyć za pomocą standardowych narzędzi do dekompresji, takich jak Corel WinZIP, Microsoft Explorer lub RARLAB WinRAR.

Pliki EGG można tworzyć za pomocą pakietu **distutils** dostępnego w Pythonie. Innym narzędziem, które może tworzyć i otwierać pliki EGG, jest **SetupTools**. Pliki EGG można zainstalować jako pakiet za pomocą **easy_install**.

`UWAGA - format pliku EGG został zastąpiony nowym formatem WHL koła.`

## Odniesienie ##

* [Python EGG](https://python101.pythonlibrary.org/chapter38_eggs.html)

