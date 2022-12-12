{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku PDF/X",
  "description":"Poznaj format plików PDF/X i API, które mogą tworzyć i otwierać pliki PDF/X.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Co to jest plik PDF/X? #

PDF/X to norma ISO 15930 opublikowana w 2001 roku z podzbiorem funkcji PDF. Norma została ustanowiona i opublikowana w oparciu o specyficzne wymagania branży poligraficznej i wydawniczej. Wszystkie wymagania dotyczące tego standardu zostały opracowane zgodnie z różnorodnymi potrzebami przemysłu poligraficznego i wydawniczego. PDF/X wymaga, aby zgodne pliki były kompletne, tj. samodzielne. Wymaga to, aby elementy takie jak czcionki używane na stronie były częścią dokumentu. Zawartość taka jak 3D lub wideo nie może być częścią dokumentu PDF/X. Informacje zawarte w dokumencie PDF/X wymagają, aby były dokładne.

## Standardy PDF/X i wersje ##

Rodzina standardów PDF/X składa się z kilku wersji, z których każda została zaprojektowana z myślą o specjalistycznym wyniku. Opracowanie tych standardów miało na celu zaspokojenie wielu różnorodnych potrzeb przemysłu poligraficznego i wydawniczego.

* `PDF/X-1a` — znany również jako pierwszy standard z rodziny PDF/X, PDF/X-1a wymaga, aby cała zawartość była częścią dokumentu PDF, aby mogła zostać wydrukowana. Elementy dokumentu, takie jak czcionki, formularze, ochrona hasłem i widoczne adnotacje, są niedozwolone. PDF/X-1a ma swoje specyficzne wymagania, jak również te dotyczące przezroczystości i dozwolone są warstwy. Wymagają one również, aby elementy druku używały tylko kolorów CMYK, skali szarości lub dodatkowych, co skutkuje brakiem użycia RGB lub przestrzeni kolorów niezależnych od urządzenia. dotyczy wymian, w których wszystkie pliki mają być dostarczone w CMYK (i/lub kolorach dodatkowych), bez danych RGB lub zarządzanych kolorami. PDF/X-1a jest również określany jako kompletna wymiana ze względu na kompletność informacji wymaganych przez
* `PDF/X-3` - został wprowadzony w 2002 roku i zniósł wiele ograniczeń PDF/X-1a. Umożliwiło to grafikom w formacie PDF/X-3 korzystanie z przestrzeni kolorów opartych na CMYK, grescale, RGB, Lab i ICC. W rzeczywistości jest oparty na standardach PDF 1.3 z [profilem ICC](https://en.wikipedia.org/wiki/ICC_Profile). Nazywany jest również zarządzaniem kolorami ze względu na elastyczność i zasady, jakie wprowadza w odniesieniu do kolorów zawartych w dokumencie PDF.
* `PDF/X-4` - obsługuje przezroczystości, więc PDF-X/4 zawiera wszystkie dane potrzebne do wydruku bez spłaszczania.
* `PDF/X-5` - jest oparty na PDF/X-4, dodając obsługę zewnętrznej grafiki poprzez referencyjne XObjects, jak również zewnętrzne profile n-colorant do celów renderowania. Użyj go do częściowej wymiany danych do druku za pomocą PDF w wersji 1.6

## Bibliografia ##

* [PDF/X – z Wikipedii](https://en.wikipedia.org/wiki/PDF/X)

