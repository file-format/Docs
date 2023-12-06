{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik MASTER - Format pliku strony wzorcowej ASP.NET",
  "description" :"Dowiedz się o formacie pliku MASTER i interfejsach API umożliwiających tworzenie i otwieranie plików MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Czym jest plik MASTER?

Plik MASTER to główny plik szablonu strony internetowej utworzony za pomocą ASP.NET. Służy jako punkt wyjścia do tworzenia wielu stron o tym samym układzie i ustawieniach, co plik MASTER. Plik szablonu MASTER zawiera ustawienia nagłówka, menu nawigacyjnych, stopki, czcionki i informacji o stylu. Korzystanie z pliku MASTER pomaga szybko utworzyć wiele stron internetowych.

Możesz otworzyć plik MASTER za pomocą Microsoft Visual Studio 2022 i nowszych wersji.

## Format pliku MASTER — więcej informacji

Plik MASTER jest tworzony i zapisywany w formacie pliku HTML i jest podobny do każdego innego pliku strony internetowej. Jest on podzielony na sekcje edytowalne i nieedytowalne. Sekcje edytowalne to te, które można modyfikować w celu spełnienia wymagań użytkownika. Sekcje nieedytowalne są wyszarzone, gdy plik MASTER jest otwierany w Microsoft Visual Studio.

Strony wzorcowe składają się z dwóch części, tj. samej strony wzorcowej i jednej lub większej liczby stron z treścią.

### Strona główna

Strona wzorcowa ma rozszerzenie .master i jest wykonana w ASP.NET. Ma predefiniowany układ, który składa się ze statycznego tekstu, znaczników HTML i elementów sterujących po stronie serwera. Na zwykłych stronach .aspx używana jest dyrektywa @ Page. W przypadku plików .master jest to zastępowane dyrektywą @ Master.

### Strony z treścią

Strona zawartości reprezentuje zawartość kontrolek zastępczych strony wzorcowej. Są to strony .aspx, które w rzeczywistości stanowią kod strony wzorcowej. Strony treści są powiązane za pomocą dyrektywy @ Page poprzez dołączenie atrybutu MasterPageFile wskazującego stronę wzorcową, która ma być używana, jak pokazano poniżej.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Bibliografia

* [Omówienie stron wzorcowych ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

