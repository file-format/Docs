{
  "date" : "2021-03-18",
  "keywords" :["plik qgz", "format pliku qgz", "co to jest plik qgz", "plik", "przykład qgz", "rozszerzenie pliku qgz", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - skompresowany projekt Quantum GIS",
  "description":"Dowiedz się o formacie pliku QGZ, który jest po prostu skompresowanym QGS i interfejsami API, które mogą tworzyć i otwierać pliki QGZ.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Czym jest plik QGZ?

Format pliku **QGZ** to skompresowane archiwum zawierające plik [QGS](/gis/qgs/) i plik QGD. Natomiast plik QGD jest bazą danych sqlite projektu qgis, która składa się z danych pomocniczych dla projektu. W przypadku braku danych pomocniczych plik QGD pozostanie pusty.

## Szczegółowe informacje o formacie pliku QGZ

QGZ został wprowadzony jako nowy wariant **formatu pliku projektu QGIS 3**. Ten format jest spakowanym kontenerem dla pliku QGS xml. Jeśli użytkownicy wybiorą QGD, który jest formatem opcjonalnym, w tym przypadku kontener jest korzystny do przechowywania bazy danych pamięci dyskowej.

W trybie klasycznym pomocnicza baza danych zapisywana jest jako plik z rozszerzeniem .qgd wraz z plikiem xml. Wybierając spakowany kontener, plik .qgd zawiera się w .qgz, po prostu ułatwia użytkownikom bez żadnego problemu, użytkownicy nie mogą go usunąć ani zapomnieć o skopiowaniu podczas udostępniania plików projektu!


## Bibliografia

* [QGZ – Nowy domyślny format pliku projektu dla QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formaty plików QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

