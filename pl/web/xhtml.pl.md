{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "rozszerzalny html"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML — rozszerzalny format pliku hipertekstowego języka znaczników",
  "description":"Dowiedz się, czym jest format pliku XHTML i interfejsy API, które mogą tworzyć i otwierać pliki XHTML.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik XHTML?

XHTML to tekstowy format pliku ze znacznikami w XML, wykorzystujący przeformułowanie HTML 4.0. Pliki te dobrze nadają się do otwierania lub przeglądania w przeglądarce internetowej. XHTML został zaprojektowany tak, aby był bardziej ustrukturyzowany, mniej skryptowy, ogólny; przy użyciu wszystkich istniejących funkcji XML i większej niezależności od urządzeń. XHTML zapewnia ogólnie wartościowy zestaw elementów i atrybutów, z opcjami rozszerzeń w połączeniu z arkuszami stylów. Atrybuty są używane z kolekcji atrybutów metadanych. XHTML zapewnia elastyczność i dostępność dzięki podporządkowaniu wszystkich **[HTML](/pl/web/html/)** elementów prezentacji arkuszom stylów. Arkusze stylów są bardziej wszechstronne niż te elementy prezentacji. Specyfikacje HTML 4.01, HTML5 i XHTML są dynamicznie rozwijane przez World Wide Web Consortium (W3C).

## Krótka historia formatu plików XHTML

Historia XHTML zaczyna się od szkicu dokumentu opublikowanego w grudniu 1998 roku przez World Wide Web Consortium. Ten dokument odnosi się do „Przeformułowania HTML w XML”, specyfikacji o nazwie XHTML 1.0. Ta nowa specyfikacja przeformułowała HTML w XML przy użyciu istniejących elementów lub atrybutów. W maju 1999 r. Konsorcjum W3 ogłosiło, że HTML 4.0 został ponownie utworzony jako aplikacja XML. czyli XHTML. 26 stycznia 2000 roku W3C wydało pierwszą specyfikację definiującą XHTML 1.0. Ponadto 31 maja 2001 roku W3C ogłosiło XHTML jako niezależny język i rozpoczęło prace nad rozwojem HTML 5.0. Jednak w 2005 roku utworzono grupę roboczą (WHATWG), której celem było ulepszenie zwykłego HTML niezależnego od XHTML. WHATWG ostatecznie zaczął pracować nad HTML5 równolegle do XHTML 2.

## Format pliku XHTML

XHTML to format, który jest zbiorem różnych typów dokumentów i modułów, które naśladują, kategoryzują i rozszerzają HTML 4. Pliki w XHTML są oparte na XML i przeznaczone do pracy z aplikacjami klienckimi opartymi na XML. Pliki XHTML są zgodne z XML. Standardowe narzędzia XML służą do przeglądania, edytowania i sprawdzania poprawności plików XHTML. Aplikacje zależne od HTML Document Object Model lub XML Document Object Model [DOM] mogą działać za pośrednictwem dokumentów XHTML. Decydując się dzisiaj na XHTML, twórcy treści mogą cieszyć się wszystkimi korzyściami płynącymi z XML, nie martwiąc się o kompatybilność swoich treści w przód lub w tył.

Zestaw powiązanych ze sobą elementów buduje moduł w XHTML. Moduł formularzy lub tabel może zawierać różne elementy formularzy lub tabel, które można wyświetlić na stronie internetowej. Modularyzacja miała na celu wyodrębnienie elementów HTML w zestawy wielu połączonych elementów. Aby twórcy treści mogli skorzystać z wyboru modułów dla różnych typów urządzeń. Ponadto moduły pozwalają agentom użytkownika wybierać elementy bez utraty spójności ze standardem XHTML. Wymagania dotyczące parsowania XHTML są takie same jak XML, podczas gdy HTML ćwiczy własne.

### Zgodność dokumentu

XHTML2 oferuje specyfikacje zgodne z dokumentami XHTML 1.0, które wykorzystują elementy i atrybuty przestrzeni nazw z XML i XHTML 1.0. Zgodność dokumentu jest dwojakiego rodzaju.

Dokument ściśle zgodny jest oparty na języku XML i wymaga jedynie usług obowiązkowych zdefiniowanych w niniejszej specyfikacji. Następujące kryteria muszą być spełnione dla plików XHTML:

* Plik musi być zgodny z ograniczeniami określonymi w DTD oraz w Dodatku B.
* Podstawowym elementem pliku musi być html.
* Podstawowy element pliku musi zawierać deklarację dla przestrzeni nazw XHTML i powinien być zdefiniowany jako:

```
http://www.w3.org/1999/xhtml.
```

* Element bazowy można zapisać jako:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Wcześniej niż element podstawowy należy zadeklarować DOCTYPE, którego publiczny identyfikator musi odwoływać się do jednej z trzech definicji typu dokumentu (DTD). Identyfikator systemu można zmodyfikować, aby był zgodny z bieżącymi konwencjami systemowymi.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

W dokumentach XML nie jest konieczne określanie deklaracji XML we wszystkich dokumentach; jednak twórcy treści są zachęcani do używania deklaracji XML we wszystkich swoich dokumentach XHTML. Deklaracja ta jest obowiązkowa, gdy kodowanie znaków w dokumencie różni się od UTF-8/16 lub gdy protokół regulujący nie określa kodowania. Poniższy przykład dokumentu XHTML definiuje deklaracje XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Zgodny agent użytkownika musi spełniać następujące zasady:

* Parsowanie i ocena dokumentu XHTML jest wykonywana przez agenta użytkownika, który zapewnia jego zgodność z rekomendacją XML 1.0.
* W przypadku walidacji agenta użytkownika musi sprawdzić poprawność dokumentów pod kątem DTD, do których się odwołują, zgodnie z XML. Kiedy plik XHTML jest przetwarzany przez agenta użytkownika jako ogólny XML, cechy typu ID zostaną uznane za identyfikatory fragmentów.

Jeśli agent użytkownika natrafi na nierozpoznany element, poniżej przedstawiono obowiązkowe kryteria, które musi spełnić

* przetworzyć zawartość tego nieznanego elementu
* zignoruj atrybut i jego wartość
* Użyj wartości podanego atrybutu jako domyślnej.

Gdy agent użytkownika natrafi na deklarację referencyjną encji, która nie została wcześniej przetworzona, należy ją przetworzyć jako znaki (zaczynające się od znaku „&” i kończące się średnikiem). Podczas przetwarzania treści znaki lub odwołania do encji znakowych, które są przewidywalne przez agenta użytkownika, ale których nie można renderować, mogą wykorzystywać dowolne alternatywne renderowanie, które daje podobne znaczenie. W takim przypadku dokument musi być wyświetlony w sposób, który uzmysłowi użytkownikowi fakt, że proces renderowania nie przebiegał normalnie. Aby przetwarzać białe znaki, agent użytkownika musi szukać definicji ze znaków CSS [CSS2].

## Kompatybilność wsteczna XHTML

Kompatybilność wsteczna dokumentów XHTML 1. jest dobrze zaznajomiona z programami użytkownika HTML 4, jeśli przestrzegane są odpowiednie zasady. XHTML 1.1 jest w pełni kompatybilny, z wyjątkiem adnotacji ruby, mimo że są one generalnie ignorowane przez przeglądarki HTML 4. XHTML 2.0 jest stosunkowo mniej kompatybilny, niemniej jednak problem został rozwiązany do pewnego stopnia poprzez użycie skryptów.

## Bibliografia

* [Historia XHTML: od lat 90. do dziś](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

