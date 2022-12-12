{
  "date" : "2021-06-24",
  "keywords" :["RSS", "częściowe", "rozszerzenie", "plik", "format", "sieć", "Really Simple Syndication", "Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Naprawdę prosta dystrybucja",
  "description":"Poznaj format plików RSS i interfejsy API, które mogą tworzyć i otwierać pliki RSS.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Co to jest plik RSS? ##

Plik z rozszerzeniem .rss jest znany jako Really Simple Syndication. RSS to plik XML, który jest łatwo lub łatwo odczytywany przez komputer. Te pliki XML są automatycznie aktualizowane o wszelkie zmiany danych lub aktualizacje witryny lub strony internetowej. Zaktualizowane informacje wraz z metadanymi (nazwisko autora, nazwa wydawcy, data publikacji itp.) oraz inne treści internetowe serwisu są pobierane przez pliki RSS użytkownika i prezentowane w łatwym do odczytania formacie. Najlepszą cechą tych plików RSS jest to, że działają w czasie rzeczywistym, a aktualizacje, wiadomości, publikacje, czyli najnowsze, są wyświetlane na górze pliku. Korzystając z pliku RSS, możesz łatwo utworzyć plik zawierający najnowsze aktualizacje dowolnego interesującego Cię tematu, pobierając odpowiednią zawartość z Internetu i czytając ją za pomocą pliku RSS.

## Krótka historia ##

W rzeczywistości plik RSS został po raz pierwszy stworzony przez firmę Netscape, która wynalazła pierwszą wersję pliku RSS, ale potem porzuciła ten pomysł i nie kontynuowała prac nad nowszymi wersjami. Wtedy to **Userland Software** pracowało nad formatem plików RSS i kontynuowało wprowadzanie do niego innowacji w nowszej wersji, tak właśnie wszedł na rynek RSS v2. Jednak wynalezienie RSS można powiązać z Resource Description Framework, autorstwa Ramanathana V w 1997 roku. Działanie tych dwóch plików jest dość podobne i można bezpiecznie założyć, że koncepcja RSS powstała w oparciu o działanie RDF, czytnik plików, który był używany do zbierania metadanych.

## Specyfikacja techniczna ##

Plik RSS jest typem pliku XML i wszystkie pliki RSS muszą być zgodne ze standardami XML 1.0. Istnieją różne wersje różnych plików RSS, między innymi 0.91, 0.92, 2.0. Plik każdej wersji jest zgodny ze specyfikacjami i standardami tej konkretnej wersji.

## RSS Przykład ##

Poniżej znajduje się uproszczony przykład RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## Odniesienie ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
