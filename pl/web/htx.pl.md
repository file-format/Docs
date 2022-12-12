{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik HTX - format pliku rozszerzenia HTML",
  "description" :"Twój przewodnik po formacie pliku, aby dowiedzieć się, co to jest plik HTX i interfejsy API, które mogą tworzyć i otwierać plik HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik HTX?

Plik HTX jest w rzeczywistości plikiem HTML, który zawiera zmienne danych do wyświetlania wyników zapytania do bazy danych jako strony internetowej. Pliki HTX, tworzone głównie za pomocą oprogramowania programistycznego Microsoft FrontPage Web, są zapisywane w tym samym folderze, co odpowiedni plik Internet Database Connector (.IDC).

Pliki HTX można otwierać za pomocą aplikacji takich jak Microsoft FrontPage i dowolnego edytora tekstu, takiego jak Notatnik, TextEdit lub Atom.

## Format pliku HTX

Pliki HTX są zapisywane jako zwykły plik tekstowy z kodem do pobierania danych z bazy danych i zapisywania zmiennych do wyświetlenia.


### Przykład pliku HTX

Przykład pliku HTX jest następujący, który definiuje nagłówek strony do wyświetlania ograniczeń zapytania i dokumentów wyświetlanych na stronie do wyświetlenia użytkownikowi.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

Dane wyjściowe tego przykładowego kodu są następujące.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Jak widać, plik HTX jest szablonem, który formatuje sposób, w jaki wyniki są zwracane i wyświetlane użytkownikom końcowym. Jest napisany w formacie HTML z niektórymi rozszerzeniami IIS i usługą indeksowania. Te rozszerzenia obejmują nazwy zmiennych i inne kody do przetwarzania wyników.

## Bibliografia

* [Formatowanie wyników w pliku .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

