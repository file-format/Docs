{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Dowiedz się o formacie pliku MCA i interfejsach API, które umożliwiają tworzenie i otwieranie plików MCA.",
  "title": "MCA — format pliku regionu Minecraft Anvil",
  "linktitle": "MCA",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-pla"
}
},
  "lastmod": "2022-12-13"
}

## Czym jest plik MCA?

Format pliku regionu Minecraft Anvil to format przechowywania danych używany do przechowywania fragmentów terenu świata Minecraft w popularnej grze wideo **Minecraft**. Świat Minecrafta składa się z regionów, z których każdy jest podzielony na części. Format pliku MCA pozwala na wydajne przechowywanie dużych ilości danych gry, takich jak lokalizacja bloków i obiektów w określonym fragmencie świata gry. Pliki MCA należy połączyć z innymi plikami MCA, aby wygenerować cały świat.

Oprócz przechowywania danych gier, format pliku regionu Anvil obsługuje także różne inne typy danych, takie jak dane graczy i metadane. Pozwala to na efektywne przechowywanie wszystkich informacji potrzebnych do pełnego odtworzenia określonego fragmentu świata gry, w tym lokalizacji bloków, bytów i innych obiektów gry.

## Format pliku MCA — więcej informacji

Format pliku regionu Anvil jest odmianą formatu NBT (Named Binary Tag), który jest hierarchiczną strukturą przypominającą drzewo do przechowywania danych w pliku binarnym. Pozwala to na efektywne przechowywanie złożonych struktur danych w kompaktowym i łatwym do odczytania formacie.

### Kawałki w pliku MCA

W Minecrafcie fragment to obszar blokowy świata gry o wymiarach 16x16x16, który jest ładowany do pamięci i renderowany na ekranie gracza. Format pliku regionu Anvil przechowuje wszystkie dane dotyczące określonej porcji w jednym pliku, który w razie potrzeby można następnie szybko załadować do pamięci. Pozwala to na wydajne przechowywanie i szybki dostęp do danych gry, co jest ważne dla zapewnienia płynnej i bezproblemowej rozgrywki.

### Mały rozmiar pliku MCA

Jedną z kluczowych cech formatu pliku regionu Anvil jest zastosowanie kompresji. Pozwala to na efektywne przechowywanie dużych ilości danych, bez utraty jakości danych i szybkości, z jaką można do nich uzyskać dostęp. Osiąga się to za pomocą różnych technik, takich jak kompresja gzip i kompresja danych fragmentów.

Skompresowany format plików MCA sprawia, że są one ważną częścią systemu przechowywania i zarządzania danymi gry. Efektywne wykorzystanie kompresji i obsługa różnych typów danych pozwala na wydajne przechowywanie i szybki dostęp do danych gry, zapewniając graczom płynną i bezproblemową rozgrywkę.

## Struktura formatu pliku MCA

Wewnętrzna struktura formatu plików MCA składa się z:
 * Nagłówek i a
 * Ładunek

### Nagłówek MCA

Nagłówek pliku regionu MCA zaczyna się od nagłówka o rozmiarze 8 KB, który jest podzielony na dwie tabele o rozmiarze 4 KB. Pierwsza tabela zawiera przesunięcia fragmentów w samym pliku regionu, podczas gdy druga tabela zawiera znaczniki czasu dla ostatnich aktualizacji tych fragmentów.

### Ładunek MCA

Ładunek MCA składa się z fragmentów, przy czym każdy fragment danych zaczyna się od czterobajtowego pola (big-endian). To pole wskazuje dokładną długość pozostałej części danych w bajtach. Dane ostatniej porcji są dopełniane tak, aby miały długość stanowiącą wielokrotność 4096B. Pliki, w których ostatni fragment nie jest dopełniony, nie są akceptowane przez Minecraft.

## Jak otworzyć pliki MCA

Możesz otwierać i edytować pliki MCA za pomocą programu MCEdit, który jest bezpłatnym edytorem typu open source dla gry Minecraft. Możesz [download MCEdit](https://www.mcedit.net/) z oficjalnej strony internetowej i używać jej do otwierania i przeglądania zawartości pliku regionu Anvil.

Po zainstalowaniu MCEdit możesz otworzyć plik regionu Anvil, wykonując następujące kroki:

 1. Uruchom MCEdit i kliknij przycisk Otwórz” w lewym górnym rogu okna.

 1. W oknie dialogowym Otwarty świat” przejdź do lokalizacji pliku regionu Anvil i wybierz go.

 1. Kliknij przycisk Otwórz”, aby otworzyć plik w MCEdit.

 1. MCEdit załaduje plik i wyświetli jego zawartość w głównym oknie. Następnie możesz użyć narzędzi i funkcji MCEdit do przeglądania, edytowania i wyodrębniania danych z pliku regionu Anvil.

## Bibliografia

* [Edytor świata Minecrafta](https://www.mcedit.net/)

* [O Minecrafcie](https://www.minecraft.net/)

* [Format pliku regionu](https://minecraft.fandom.com/wiki/Region_file_format)


