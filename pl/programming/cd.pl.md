{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd", "co to jest plik cd", "jak otworzyć plik cd", "rozszerzenie", "plik", "plik cd", "format pliku cd", "rozszerzenie pliku cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - plik diagramu klas programu Visual Studio",
  "description":"Poznaj format plików CD i interfejsy API, które mogą tworzyć i otwierać pliki CD.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Czym jest plik CD?

Plik z rozszerzeniem .cd to plik diagramu klas programu Visual Studio, który zawiera informacje o strukturze i relacjach między wszystkimi klasami w bieżącym rozwiązaniu. Rozwiązanie programu Visual Studio (reprezentowane przez [.sln](/pl/programming/sln/)) może zawierać jeden lub więcej projektów, z których każdy ma wiele różnych klas. Plik diagramu klas można wygenerować, klikając projekt prawym przyciskiem myszy i wybierając opcję diagramu klas.

## Format pliku diagramu klas (.cd) — więcej informacji

Plik diagramu klas jest zapisywany w standardowym formacie pliku XML, który reprezentuje klasy w projekcie jako węzły XML. Jeśli program Visual Studio nie jest dostępny, te pliki diagramów klas można otworzyć w dowolnej aplikacji obsługującej otwieranie plików XML.

### Jak dodać diagramy klas do projektu programu Visual Studio

W programie Visual Studio otwórz rozwiązanie/projekt, dla którego chcesz dodać diagram klas. Następnie kliknij prawym przyciskiem myszy węzeł projektu i wybierz polecenie Dodaj > Nowy element. Lub naciśnij klawisze Ctrl+Shift+A.

* Zostanie otwarte okno dialogowe Dodaj nowy element.

* Rozwiń Typowe elementy > Ogólne, a następnie wybierz Diagram klas z listy szablonów. W przypadku projektów Visual C++ poszukaj w kategorii Narzędzia, aby znaleźć szablon Diagram klas.

### Eksportuj diagramy klas (CD) do obrazów

Visual Studio umożliwia konwertowanie/eksportowanie diagramów klas do obrazów takich jak [PNG](/pl/image/png/), [JPEG](/pl/image/jpeg/) i [BMP](/pl/image/bmp/). Te wyeksportowane pliki diagramów klas mogą być używane do celów dokumentacji i przechowywania danych technicznych (TDP). Aby przekonwertować diagram klas na obraz, można wykonać następujące kroki z poziomu programu Microsoft Visual Studio.

1. Otwórz plik diagramu klas (.cd).
1. Z menu Diagram klas lub menu skrótów powierzchni diagramu wybierz Eksportuj diagram jako obraz.
1. Wybierz schemat.
1. Wybierz żądany format.
1. Wybierz opcję Eksportuj, aby zakończyć eksport.

## Bibliografia

* [Klasy projektowania w programie Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

