{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku PDF/UA",
  "description":"Poznaj format plików PDF/UA i API, które mogą tworzyć i otwierać pliki PDF/UA.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Co to jest plik PDF/UA? #

PDF/UA został opublikowany jako [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) w sierpniu 2012 roku i jest zdecydowanie pierwszą kompletną definicją zestawu wymagań dla powszechnie dostępnych dokumentów PDF. Termin „powszechnie dostępny” odnosi się do zrozumienia, że informacje zawarte w dokumencie [PDF](/pl/pdf/) powinny być jednakowo i niezależnie dostępne dla wszystkich ogółem, aw szczególności dla osób niepełnosprawnych. Wprowadzenie standardu PDF/UA można uznać za ważny krok w tworzeniu narzędzi i aplikacji do tworzenia i odczytywania treści PDF.

## Wymagania dotyczące formatu pliku ##

PDF/UA ma u podstawy pewne określone wymagania, które stanowią istotę tego standardu. Zasadniczo opierają się one na tagowaniu plików PDF, co oznacza, że wszystkie dokumenty PDF/UA muszą być odpowiednio oznakowane. Wymaga również, aby tagi były semantycznie odpowiednie i ułożone w logicznej kolejności. Gwarantuje to, że dokument końcowy utworzony ze specyfikacją PDF/UA jest bardziej niezawodny i dostępny. Może to skłonić autorów plików PDF do zastanowienia się, czy muszą wiedzieć wszystko o wszystkich takich wymaganiach? Na szczęście tak nie jest, ponieważ narzędzia zgodności PDF/UA przejmują odpowiedzialność za dodawanie i zachowanie dostępności pliku PDF.

Wymagania dotyczące formatu pliku PDF/UA są następujące.

* Treść jest kategoryzowana na jeden z dwóch sposobów: istotna treść i artefakty, takie jak dekoracyjne elementy strony. Cała znacząca treść musi być oznaczona i zintegrowana z drzewem struktury wszystkich znaczników w dokumencie. Z drugiej strony artefakty muszą być jedynie oznaczone jako takie.
* Znacząca treść musi być oznaczona tagami i razem z innymi tagami w dokumencie tworzyć kompletne drzewo struktury.
* Znaczące treści muszą być oznaczone odpowiednimi tagami semantycznymi.
* Drzewo struktury utworzone przez znaczniki dokumentu musi odzwierciedlać logiczną kolejność czytania dokumentu.
* Można używać tylko standardowych znaczników zdefiniowanych w PDF 1.7; jeśli używane są jakiekolwiek inne znaczniki, wpis przypisania roli musi rejestrować, który standardowy znacznik reprezentuje każdy z nich.
* Informacje nie mogą być przekazywane wyłącznie za pomocą środków wizualnych (np. kontrastu, koloru lub pozycji na stronie).
* Migotanie, miganie lub miganie treści jest niedozwolone, zarówno jako efekty kontrolowane przez JavaScript, jak i jako część jakichkolwiek filmów osadzonych w pliku PDF.
* Należy podać tytuł dokumentu i ustawić dokument tak, aby tytuł (a nie nazwa pliku) pojawiał się w tytule okna.
* Należy zwrócić uwagę na język wszystkich treści, a zmiany językowe muszą być wyraźnie oznaczone jako takie.

## Zgodność PDF/UA ##

Standard PDF/UA określa specyfikacje treści, czytników i technologii wspomagających. Te trzy aspekty są ze sobą powiązane na podstawie treści dokumentu. Wymagania dotyczące zgodności dla każdego z nich są wymienione poniżej.

## Zgodność plików ##

Pliki zgodne ze standardem PDF/UA powinny zawierać funkcje zgodne z [specyfikacją PDF 1.7](http://www.adobe.com/go/pdfreference). Należy jednak wykluczyć funkcje zabronione przez PDF/UA.

## Zgodni czytelnicy ##

Zgodny czytelnik musi przestrzegać zasad zapisanych w specyfikacjach PDF 1.7. W szczególności powinien wspierać:

* wszystkie znaczniki, atrybuty i wartości kluczy określone dla ułatwień dostępu. Powinien również mieć możliwość przetwarzania i przedstawiania podpisów cyfrowych, adnotacji i Treści opcjonalnych.
* przetwarzanie i reprezentowanie podpisów cyfrowych, adnotacji i treści opcjonalnych
* Poruszaj się po dokumencie na różne sposoby

## Zgodność technologii wspomagającej ##

Zgodna technologia wspomagająca jest zobowiązana do obsługi funkcji PDF/UA. Obejmują one na przykład cechy treści i czytelnika oraz powinny umożliwiać nawigację po etykietach stron, strukturze dokumentu lub zarysie. Powinien również umożliwiać użytkownikowi zastąpienie domyślnego powiększenia nawigacji.

## Bibliografia ##

* [PDF/UA – z Wikipedii](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA w pigułce](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

