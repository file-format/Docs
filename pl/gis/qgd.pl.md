{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Baza danych Sqlite projektu QGIS", "rozszerzenie", "format", "QGIS", "Pomocnicza baza danych", "Co to jest plik QGD"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - baza danych Sqlite projektu QGIS",
  "description":"Dowiedz się o QGD, która jest bazą danych sqlite projektu QGIS i API, które mogą tworzyć i otwierać pliki QGD.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Czym jest plik QGD?

Plik z rozszerzeniem .QGD jest w rzeczywistości powiązaną bazą danych sqlite projektu **QGIS**, która zawiera dane pomocnicze projektu. Plik QGD pozostanie pusty, jeśli zabraknie danych pomocniczych dla projektu.

## Szczegóły dotyczące formatu pliku QGD

W trybie klasycznym pomocnicza baza danych zapisywana jest jako plik z rozszerzeniem .qgd wraz z plikiem xml. System **Pomocnicza Baza Danych** umożliwia alternatywny odczyt i zapis danych w systemie. Podczas tworzenia QGZ, który jest spakowanym kontenerem, plik .qgd zawiera plik .qgz.

## Co to jest pomocnicza baza danych?
Pomocnicza baza danych jest w rzeczywistości rezerwowym systemem db, który jest tworzony jako odpowiedź na duplikację docelowej bazy danych. Pomocnicza baza danych jest w rzeczywistości przypadkiem zduplikowanej bazy danych, która byłaby bazą danych, do której duplikujesz. Np. jeśli ustawisz rezerwową bazę danych przy użyciu zduplikowanej bazy danych, źródłowa baza danych będzie docelowa, a rezerwowa baza danych będzie nazywana pomocniczą.


## Bibliografia

* [QGZ – Nowy domyślny format pliku projektu dla QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formaty plików QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

