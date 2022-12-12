{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku GDB - plik geobazy plików ESRI",
  "description":"Dowiedz się o formacie pliku GDB i interfejsach API, które mogą tworzyć i otwierać pliki GDB.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Czym jest plik GDB?

Plik ESRI Geodatabase (FileGDB) to zbiór plików w folderze na dysku, który zawiera powiązane dane geoprzestrzenne, takie jak zestawy danych obiektów, klasy obiektów i powiązane tabele. Aby działał, wymaga przechowywania pewnych innych plików obok pliku .gdb w tym samym katalogu. Zapytania mogą być wykonywane w pliku .gdb w celu zarządzania danymi przestrzennymi i nieprzestrzennymi.

## Format pliku GDB — więcej informacji

Geobazy plikowe składają się z siedmiu tabel systemowych oraz danych użytkownika. Dane użytkownika mogą być przechowywane w następujących typach zbiorów danych:

* Klasa funkcji
* Zestaw danych funkcji
* Zestaw danych mozaiki
* Katalog rastrów
* Zestaw danych rastrowych
* Schematyczny zbiór danych
* Stół (nieprzestrzenny)
* Skrzynki narzędziowe

Zestawy danych obiektów mogą zawierać klasy obiektów, a także następujące typy zestawów danych:

* Załączniki
* Adnotacja powiązana z funkcją
* Sieci geometryczne
* Zestawy danych sieciowych
* Tkaniny paczkowe
* Zajęcia z relacji
* Tereny
* Topologie

Domyślny maksymalny rozmiar zbiorów danych w geobazach plikowych to 1 TB. Maksymalny rozmiar można zwiększyć do 256 TB w przypadku dużych zbiorów danych (zwykle rastrowych). Jest to kontrolowane przez słowo kluczowe konfiguracji. Zobacz Słowa kluczowe konfiguracji dla geobaz plikowych, aby uzyskać więcej informacji.

Geobazy plikowe mogą również zawierać podtypy i domeny oraz uczestniczyć w replikacji pobierania/rejestrowania i replikach jednokierunkowych.

Dostęp do geobazy plikowej może mieć jednocześnie kilku użytkowników. Jeśli użytkownicy edytują, muszą edytować różne zestawy danych.

## Specyfikacje formatu plików GDB ##

Plik GDB jest zastrzeżonym formatem ESRI, a jego specyfikacje nie są dostępne publicznie. Z tego powodu szczegóły formatu pliku dla FIle GDB nie mogły zostać udokumentowane nigdzie indziej niż niektóre źródła, które to zrobiły [częściowo] (https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) przez inżynierię wsteczną .

## Bibliografia ##

* [Specyfikacje FGDB] (https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

