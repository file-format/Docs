{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik APPCACHE - format pliku manifestu pamięci podręcznej HTML5",
  "description" :"Dowiedz się, czym jest plik APPCACHE i interfejsy API, które mogą tworzyć i otwierać pliki APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Czym jest plik APPCACHE?

Plik APPCACHE to plik tekstowy zawierający listę zasobów, które mają być buforowane przez przeglądarki w celu uzyskania dostępu offline do aplikacji internetowych. Jest to przydatne, gdy nie ma połączenia z Internetem. W takiej sytuacji przeglądarka korzysta z zasobów pamięci podręcznej offline w celu zapewnienia dostępu do zawartości sieci. Plik APPCACHE zawiera zasoby internetowe, takie jak obrazy (na przykład **[PNG](/pl/image/png/)**, **[WEBP](/pl/image/webp/)** itd.), arkusze stylów **([ CSS])(/pl/web/css/)** i pliki skryptów (takie jak pliki Javascript **[JS](/pl/web/js/)**).

Aplikacje, które mogą **otwierać pliki APPCACHE**, obejmują przeglądarki internetowe, takie jak Google Chrome, Safari i Firefox.

## Format pliku APPCACHE — więcej informacji

Pliki APPCACHE to proste pliki tekstowe, zapewniające dostęp offline do stron internetowych do uruchamiania bez połączenia z Internetem. Obecność APPCACHE oznacza, że strona jest dostępna w trybie offline.

### Jak odwołać się do pliku APPCACHE?

Na Twojej stronie HTML plik APPCACHE ma następujące odniesienie.

```
<html manifest="example.appcache">
  ...
</html>
```

## Struktura pliku manifestu APPCACHE

Prosty plik manifestu APPCACHE wygląda następująco.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Jest to najprostszy przykład i mogą występować również bardziej złożone struktury.

## Zalety manifestu APPCACHE

Zastosowanie interfejsu pamięci podręcznej daje aplikacjom internetowym następujące korzyści.

1. Przeglądanie w trybie offline — interfejs pamięci podręcznej umożliwia użytkownikom końcowym przeglądanie całej witryny w trybie offline
1. Szybkość — pamięć podręczna umożliwia szybki dostęp do treści offline bezpośrednio z dysku
1. Dostępność przez cały czas — w przypadku awarii witryny użytkownicy nadal będą mieli dostęp do treści internetowych i będą mogli korzystać z trybu offline

## Bibliografia

* [Przewodnik po manifestie AppCache dla początkujących](https://web.dev/appcache-beginner/)

