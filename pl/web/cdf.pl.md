{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Format definicji kanału",
  "description" :"Dowiedz się, czym jest plik CDF i interfejsy API, które mogą tworzyć i otwierać pliki CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Czym jest plik CDF?

Plik z rozszerzeniem .cdf to format pliku dystrybucji informacji oparty na XLM, który był używany do publikowania częstych aktualizacji jako „kanały”. Informacje są publikowane z dowolnego serwera WWW i są automatycznie dostarczane do komputerów z kompatybilnymi programami odbiorczymi, takimi jak przeglądarki internetowe. Użytkownicy subskrybują aktywne kanały i mają zaplanowane aktualizacje dostarczane na ich komputery stacjonarne.
Pliki CDF były wcześniej używane w połączeniu z technologiami Microsoft Active Channel, Active Desktop i Smart Offline Favorites.

## Format pliku CDF

Pliki CDF są zapisywane jako pliki XML, które są ogólnym formatem plików internetowych do wymiany informacji. Format pliku CDF jest już starym formatem i nigdy nie był powszechnie stosowany. W porównaniu z tym RSS Netscape był bardziej znany i powszechnie używany.

### Przykład formatu pliku CDF

Poniżej znajduje się ogólny przykład formatu pliku CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domena/folder/"
LASTMOD="1998-11-05T22:12"
PRECACHE="TAK"
POZIOM="0">
<TITLE>Tytuł kanału</TITLE>
<ABSTRACT>Streszczenie zawartości kanału.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="TAK"
POZIOM="1">
<TITLE>Tytuł strony drugiej</TITLE>
<ABSTRACT>Streszczenie zawartości strony drugiej.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Bibliografia

* [Format definicji kanału – według Wikipedii](https://en.wikipedia.org/wiki/Channel_Definition_Format)

