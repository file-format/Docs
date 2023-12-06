{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik AXD - Format pliku modułu obsługi sieci Web ASP.NET",
  "description" :"Dowiedz się, czym jest plik AXD i interfejsach API, które umożliwiają tworzenie i otwieranie plików AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Czym jest plik AXD?

Plik AXD to plik ustawień sieciowych używany do obsługi i pobierania żądań zasobów osadzonych w ASP.NET. Zawiera instrukcje umożliwiające odzyskanie osadzonych zasobów, takich jak obrazy, pliki JavaScript ([.JS](/pl/web/js/)) i pliki [.CSS](/pl/web/css/). Pliki AXD służą do wstrzykiwania zasobów na strony po stronie klienta. Dzięki temu strony klienckie mają dostęp do tych zasobów na serwerze w standardowy sposób.

## Format pliku AXD

Pliki AXD są przechowywane jako pliki binarne po stronie serwera. Odnosi się do pliku modułu obsługi sieci Web w ASP.NET, który jest komponentem generującym odpowiedzi na określone żądania kierowane do serwera WWW. Pliki AXD wykonują niestandardowe przetwarzanie przed wygenerowaniem odpowiedzi na podstawie żądań stron po stronie klienta. Są one zazwyczaj zapisywane jako pliki **WebResource.axd**.

### Co to jest plik WebResource.axd?

Większość projektów ASP.NET zapisuje pliki AXD jako pliki WebResource.axd, które umożliwiają stronom po stronie klienta pobieranie zasobów osadzonych w zestawie. Aplikacja może działać wolniej, jeśli zostanie uruchomiona w trybie debugowania, ponieważ procedura obsługi pliku WebResources.axd nie jest buforowana.

## Bibliografia

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

