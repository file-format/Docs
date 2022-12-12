{
  "date" : "2019-10-11",
  "keywords" :["plik dcm", "format pliku dcm", "co to jest plik dcm", "plik", "przykład dcm", "rozszerzenie pliku dcm", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku DCM - Plik Cyfrowych Informacji Medycznych",
  "description":"Poznaj format pliku DCM i interfejsy API, które mogą tworzyć i otwierać pliki DCM.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Czym jest plik DCM?

Pliki z rozszerzeniem .dcm reprezentują obraz cyfrowy, który przechowuje informacje medyczne pacjentów, takie jak MRI, tomografia komputerowa i obrazy ultrasonograficzne. Pliki DCM używają formatu pliku obrazu [DICOM](/pl/image/dicom) (Digital Imaging and Communications in Medicine) i mogą zawierać informacje o pacjencie w celach informacyjnych. Został opracowany przez [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) i miał na celu standaryzację formatu plików obrazowania do dystrybucji i przeglądania obrazów medycznych.

## Format pliku DCM

Pliki DCM przechowują informacje w formacie obrazu DICOM. Pliki te przechowują zestaw danych, który jest informacją ze świata rzeczywistego, która reprezentuje instancję SOP powiązaną z DICOM IOD. Metainformacje pliku DICOM są przechowywane w pliku, po którym następuje strumień bajtów rzeczywistego zestawu danych.

### Metainformacje o pliku DICOM ##

Każdy plik DICOM zawiera nagłówek informacji identyfikacyjnej dla zamkniętego zestawu danych, który składa się z:
* 128-bajtowy preambuła pliku
* 4-bajtowy prefiks DICOM
* Elementy meta pliku

Ten nagłówek jest obowiązkowy dla każdego pliku DICOM.

### Metaelementy pliku ###
|Nazwa atrybutu|Etykieta|Typ| Opis atrybutu
---|---|---|---|
|Preambuła pliku|Brak pól znacznika lub długości|1|Stałe pole 128-bajtowe dostępne dla profilu aplikacji lub zastosowania określonego w implementacji. Jeśli nie są używane przez profil aplikacji lub konkretną implementację, wszystkie bajty powinny być ustawione na 00H. Czytelnicy lub aktualizatorzy zestawu plików nie mogą polegać na treści niniejszej Preambuły w celu ustalenia, czy ten plik jest plikiem DICOM, czy nie.
|Prefiks DICOM|Brak pól znacznika lub długości|1|Cztery bajty zawierające ciąg znaków "DICM". Ten przedrostek jest przeznaczony do rozpoznawania, czy ten plik jest plikiem DICOM, czy nie.
|Długość grupy metadanych pliku|(0002,0000)|1|Liczba bajtów następujących po tym elemencie metadanym pliku (koniec pola wartości) do ostatniego metaelementu metadanego grupy 2 włącznie
|Wersja metadanych pliku|(0002,0001)|1|To jest dwubajtowe pole, w którym każdy bit identyfikuje wersję tego nagłówka metadanych pliku. W wersji 1 wartość pierwszego bajtu to 00H, a wartość drugiego bajtu to 01H. Implementacje odczytujące pliki z metainformacjami, w których ten atrybut ma bit 0 (lsb) drugiego bajtu ustawiony na 1, mogą interpretować metainformacje pliku zgodnie z tym wersja PS3.10. Wszystkie pozostałe bity nie są sprawdzane.
|Media Storage SOP Class UID|(0002,0002)|1|Niepowtarzalnie identyfikuje klasę SOP powiązaną ze zbiorem danych. Identyfikatory UID klasy SOP dozwolone dla przechowywania multimediów są określone w PS3.4 — Media Storage Application Profiles.
|Media Storage SOP Instance UID|(0002,0003)|1|Niepowtarzalnie identyfikuje instancję SOP powiązaną ze zbiorem danych umieszczonym w pliku i następującym po metainformacjach pliku.
|UID składni przesyłania|(0002,0010)|1|Unikalnie identyfikuje składnię przesyłania używaną do kodowania następującego zbioru danych. Ta składnia transferu nie ma zastosowania do metainformacji pliku.
|Implementation Class UID|(0002,0012)|1|Niepowtarzalnie identyfikuje implementację, która napisała ten plik, oraz jego zawartość. Zapewnia jednoznaczną identyfikację rodzaju implementacji, która jako ostatnia zapisała plik w przypadku problemów z wymianą.
|Nazwa wersji implementacji|(0002,0013)|3|Identyfikuje wersję identyfikatora UID klasy implementacji (0002,0012) przy użyciu maksymalnie 16 znaków z repertuaru.
|Tytuł jednostki aplikacji źródłowej|(0002,0016)|3|Tytuł jednostki aplikacji DICOM (AE) jednostki AE, która zapisała zawartość tego pliku (lub ją ostatnio zaktualizowała). Wykorzystanie pozwala na śledzenie źródła błędów w przypadku problemów z wymianą mediów.
|UID twórcy informacji prywatnych|(0002,0100)|3|Identyfikator UID twórcy informacji prywatnych (0002,0102).
|Prywatne informacje|(0002,0102)|1C|Zawiera prywatne informacje umieszczone w pliku Metainformacje. Twórca zostanie zidentyfikowany w (0002,0100). Wymagane, jeśli obecny jest identyfikator UID twórcy informacji prywatnych (0002,0100).

### Enkapsulacja zestawu danych ###

Plik DICOM zawiera pojedynczy zbiór danych, który reprezentuje pojedynczą instancję SOP powiązaną z pojedynczą klasą SOP. Identyfikator UID składni przesyłania metainformacji pliku DICOM definiuje składnię przesyłania używaną do kodowania zbioru danych.

### Obsługa informacji o zarządzaniu plikami ###

Warstwa formatu multimediów udostępnia następujące informacje o zarządzaniu plikami, jeśli jest to konieczne dla danego profilu aplikacji DICOM.

* Identyfikacja właściciela zawartości pliku

* Statystyki dostępu do plików (np. data i godzina utworzenia)

* Kontrola dostępu do plików aplikacji

* Kontrola dostępu do nośników fizycznych (np. ochrona przed zapisem)

## Bibliografia ##
* [Standard DICOM](https://www.dicomstandard.org/current/)
* [Format pliku DICOM] (http://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

