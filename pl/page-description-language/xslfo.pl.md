{
  "date" : "2019-10-11",
  "keywords" :["XSLFO", "Obiekty formatowania XSL", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzalny język arkuszy stylów"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Poznaj format pliku XSLFO i interfejsy API, które mogą tworzyć i otwierać pliki XSLFO.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Czym jest plik XSL-FO? ##

XSL-FO (XSL Formatting Objects) to potężny język arkuszy stylów do formatowania dokumentów XML. Semantyka ograniczonej formy papieru i druku jest wyrażona przez XSL-FO, gdy wymiary są ustalone. W przeciwieństwie do HTML, który reprezentuje semantykę nieograniczonej formy okna przeglądarki o zmiennych wymiarach. Dokumenty XML sformatowane przez XSL-FO są najczęściej używane do generowania plików PDF. XSL (Extensible Stylesheet Language) to zestaw kompletnych technologii W3C przeznaczonych do projektowania formatowania i wymiany dokumentów XML i części XSL-FO tego języka. XSLT i XPath to także inne części XSL.

Proponuje się, aby dokumenty XML były najpierw przekształcane w XSL-FO, PDF jest przykładem tego kryterium. W formacie PDF wyniki są renderowane najpierw przy użyciu formatera XSLT, a następnie XSL-FO. W ten sposób dokumenty XML mogą być formatowane losowo. Chociaż XSL-FO wykorzystuje właściwości Cascading Style Sheet (CSS) i rozszerza je tam, gdzie jest to konieczne dla rzeczywistego formatu, zawiera szablony stron zwane wzorcami stron w terminologii XSL-FO. XSL-FO zapewnia również formatowanie dość skomplikowanych dokumentów i obsługuje generowanie indeksów.

## Historia i podstawowe pojęcia ##

W styczniu 2012 r. Roboczy Szkic XSL-FO został po raz ostatni zaktualizowany, aw listopadzie 2013 r. jego Grupa Robocza została zamknięta. Arkusz stylów XSL określa prezentację klasy dokumentów XML, opisując, w jaki sposób instancja klasy jest przekształcana w dokument XML, który używa słownika formatującego. XSL-FO jest zintegrowanym językiem prezentacji i nie ma znaczników semantycznych, które są używane w HTML. Co więcej, język ten przechowuje wszystkie dane dokumentu w sobie, w przeciwieństwie do CSS, który zmienia domyślne ustawienia zewnętrznego dokumentu HTML lub XML.

Ogólne kryteria używania XSL-FO są takie, że użytkownik pisze dokument w języku XML, a nie w FO. Następnie następuje transformacja XSLT. Ta transformacja XSLT jest odpowiedzialna za konwersję XML do XSL-FO. Zaraz po wygenerowaniu dokumentu XSL-FO jest on przekazywany do aplikacji zwanej procesorem FO. Procesory FO są odpowiedzialne za przekształcenie tego dokumentu w czytelny i nadający się do wydrukowania dokument. Pliki PDF lub PS to przykłady najczęściej spotykanych danych wyjściowych XSL-FO. Nie oznacza to jednak, że procesor FO może generować tylko te dwa typy formatów jako dane wyjściowe. Niektóre procesory FO mogą wyprowadzać dane w plikach RTF lub nawet w GUI użytkownika może pojawić się okno, w którym wyświetlana jest kolejność stron i ich zawartość.

Dokument XSL-FO różni się od PDF czy PS w tym sensie, że ostatecznie nie definiuje układu tekstu na różnych stronach. Być może stylizuje strony i określa miejsca wyświetlania treści. Ponadto procesor FO organizuje tekst w granicach określonych przez dokument FO. Ta specyfikacja pozwala nawet różnym procesorom FO zachowywać się odpowiednio do stron tworzonych w wyniku. Przykładem takiego zachowania jest dzielenie wyrazów, niewiele procesorów FO może dzielić wyrazy w celu zaoszczędzenia miejsca w przypadku łamania linii, podczas gdy niektóre procesory nie wybierają tej opcji. Wybór różnych algorytmów dzielenia wyrazów, które odpowiadają ich wymaganiom, zależy od procesorów. Te algorytmy dzielenia wyrazów mogą być bardzo proste lub bardziej złożone. W niektórych sytuacjach specyfikacja XSL-FO wyraźnie sankcjonuje procesory FO, pewien stopień wyboru w kontekście układu.

Ta różnorodność procesorów FO generuje różne wyniki, którymi procesory często nie przejmują się. Ponieważ głównym celem XSL-FO jest tworzenie stronicowanych/drukowanych dokumentów. Same dokumenty XSL-FO zwykle działają jako pośrednicy, ich główną funkcją jest generowanie plików PDF lub dokumentu, który można wydrukować jako dane wyjściowe do dystrybucji. W HTML/CSS lub XSL-FO dystrybucja pliku PDF jako rezultatu końcowego zamiast wprowadzania języka formatowania wskazuje, że na odbiorców nie ma wpływu wynikająca z tego wszechstronność wynikająca z różnic między interpretatorami języka formatowania. Z drugiej strony oczywiste jest, że nie ma łatwej drogi, aby dokument mógł zaspokoić różne potrzeby odbiorców, np. zmienny rozmiar strony lub żądany rozmiar czcionki, czy dostosowanie strony lub druku.

## Format pliku XSLFO ##

Dokumenty SL-FO są w zasadzie dokumentami XML, ale nie są zgodne z żadnym schematem. Zamiast tego dokumenty SL-FO stosują składnię zdefiniowaną w specyfikacji ich własnego języka. W każdym dokumencie XSL-FO wymagane są dwie sekcje:

1. Sekcja określająca listę oznaczonych układów stron.
1. Sekcja ze wszystkimi szczegółami danych dokumentu, ze znacznikami, które określają wyświetlanie treści na różnych stronach poprzez różne układy stron.

Właściwości strony są wymienione w układach stron, które mogą określać organizację tekstu, aby zachować zgodność z konwencjami dla określonego języka. Ponadto rozmiar strony, ich marginesy i kolejność stron (co sankcjonuje różne właściwości stron parzystych i nieparzystych) są również określane przez układy stron.

Część dokumentu zawierająca dane jest podzielona na serię przepływów, z których każdy jest połączony z układem strony. Przepływy zawierają w sobie listę bloków. Ta lista bloków może zawierać wbudowane znaczniki lub listę danych tekstowych, a może oba jednocześnie. Marginesy dokumentu mogą również zawierać numery stron lub nagłówki rozdziałów. Funkcjonalność zarówno bloków, jak i elementów śródliniowych pozostaje taka sama jak w CSS, jednak niektóre zasady wypełniania i marginesów różnią się w przypadku FO i CSS.

Kierunek orientacji strony jest całkowicie określony dla rozszerzeń bloków i śródlinii, dzięki czemu dokumenty FO działają w językach innych niż angielski. Język specyfikacji FO używa słów początek i koniec zamiast lewego i prawego do opisu kierunków. Podstawowe zasady znaczników treści i kaskadowania XSL-FO zostały zaczerpnięte z CSS. Język XSL-FO jest zgodny z następującymi specyfikacjami.

## Wiele kolumn ##

Strona może mieć wiele kolumn i bloków i domyślnie może rozciągać się od jednej kolumny do drugiej. Wiele stron może mieć różne szerokości i liczby kolumn. Wszystkie cechy FO są zgodne z ograniczeniami strony wielokolumnowej.

### Listy ###

Lista XSL-FO jest tworzona przez dwa zestawy bloków ułożonych policzek przy policzku. Koncepcyjnie na liście blok po lewej stronie wskazuje liczbę, punktor lub ciąg tekstu, podczas gdy blok po prawej stronie może działać zgodnie z oczekiwaniami. Numeracja list XSL-FO jest zwykle wykonywana przez XSLT.

### Stoły ###

Tabela FO jest podobna do tabeli HTML/CSS. Użytkownik może wybrać wiersze danych, informacje o stylizacji, kolor tła dla każdej pojedynczej komórki. Korzystając z odrębnych informacji o stylach, użytkownik ma przywilej wyboru pierwszego wiersza jako wiersza nagłówka tabeli. Procesor FO może być wyraźnie poinformowany o specyfikacji miejsca w każdej kolumnie lub automatycznie dopasować tekst do tabeli.

### Indeksowanie ###

XSL-FO 1.1 posiada funkcje, które pomagają generować indeks poprzez odwoływanie się do odpowiednio oznaczonych elementów.

### Korzyści ###

* Odpowiednie do publikowania opartego na treści
* Łatwość użycia
* Niska cena

## Bibliografia ##

* [Co to jest XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [Obiekty formatowania XSL](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

