{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik CON - Format pliku źródłowego aplikacji koncepcyjnej",
  "description" :"Dowiedz się, co to jest plik CON i interfejsy API, które mogą tworzyć i otwierać pliki CON.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Czym jest plik CON?

Plik CON to plik kodu źródłowego aplikacji opracowanej dla **Concept Application Server**. Służy do pisania aplikacji służących do wymiany danych pomiędzy serwerem a użytkownikiem. Pliki CON hostowane na serwerze są dostępne za pomocą przeglądarki internetowej, pod warunkiem, że Concept Client jest zainstalowany po stronie użytkownika. Serwer Concept Application to serwer WWW z językiem programowania na małą skalę, który może mieć silnik bazy danych podzbioru [SQL](/pl/database/sql/) (TinDB).

Pliki CON można otwierać / uruchamiać za pomocą RadGs Concept Application Server.

## Format pliku CON — więcej informacji

Pliki CON są hostowane na serwerze i są dostępne za pomocą przeglądarki internetowej na komputerze użytkownika. Koncepcja [Adresy URL](/pl/web/url/) różnią się od zwykłych adresów URL HTTP i zaczynają się od **concept://**.

### CON Przykład adresu URL pliku

Dostęp do pliku CON hostowanego na serwerze Concept Application Server można uzyskać za pośrednictwem przeglądarki internetowej przy użyciu adresów URL, takich jak:

```
concept://domain.server.com/web_application/main.con.
```
## Bibliografia

* [Serwer aplikacji koncepcyjnych](https://github.com/Devronium/ConceptApplicationServer)

