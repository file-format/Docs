{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Rozszerzenie pliku INC - Co to jest plik INC?",
  "description":"Dowiedz się o formacie pliku INC Include i interfejsach API, które mogą tworzyć i otwierać pliki INC.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Czym jest plik INC?

Plik INC to plik dołączany, który jest używany przez kod źródłowy programu do odwoływania się do informacji nagłówków. Jest podobny do formatu pliku [.h](/pl/programming/h/) i zawiera deklaracje, funkcje, nagłówki lub makra, które mogą być ponownie wykorzystywane przez pliki kodu źródłowego, takie jak C++. Pliki INC są używane przez różne języki programowania, takie jak C, [C++](/pl/programming/cpp/), Pascal, [PHP](/pl/programming/php/) i [Java](/pl/programming/java/). Edytory tekstu, takie jak Microsoft Notepad, Notepad ++ i TextEdit, mogą być używane do otwierania plików INC.

## Format pliku INC — więcej informacji

Plik INC jest zapisywany jako zwykły plik tekstowy ze wszystkimi deklaracjami zawartymi zgodnie ze składnią deklaracji. Jeden plik INC może również odwoływać się do innych plików INC. Po utworzeniu plik INC staje się częścią projektu i można do niego odwoływać się z plików źródłowych, takich jak C++. Można do niego odwoływać się w wielu plikach źródłowych, aby uniknąć powielania.

## Zawartość pliku INC

Pliki INC mogą zawierać następujące informacje.

**`Zmienne`** — w przypadku programowania obiektowego (OOP) plik nagłówka klasy zawiera definicje wszystkich zmiennych na poziomie klasy, które są dostępne w plikach kodu źródłowego implementacji

**`Deklaracja metod`** — wszystkie deklaracje metod są zawarte w plikach nagłówkowych .h, aby były dostępne w wielu plikach implementacji.

**`Definicje funkcji nieliniowych`** — pliki nagłówkowe mogą również zawierać definicje metod nieliniowych.

## Wada używania pliku INC w PHP

PHP to skrypty po stronie serwera, które działają na serwerze i zwracają wyniki do wywołujących stron internetowych. Jeśli plik PHP odwołuje się do pliku INC, a serwer nie jest skonfigurowany do analizowania plików .inc (co jest bardzo powszechne), użytkownik może wyświetlić kod źródłowy php w pliku .inc, odwiedzając katalog URL. Należy więc zachować ostrożność podczas używania plików INC jako plików dołączanych w PHP.

## Bibliografia

* [Korzystanie z INC w PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

