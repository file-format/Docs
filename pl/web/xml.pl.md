{
  "date" : "2019-10-11",
  "keywords" :["xml", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "rozszerzalny język znaczników"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku XML",
  "description":"Poznaj format pliku XML i interfejsy API, które mogą tworzyć i otwierać pliki XML.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik XML?

XML oznacza Extensible Markup Language, który jest podobny do **[HTML](/pl/web/html/)**, ale różni się używaniem tagów do definiowania obiektów. Cała idea stworzenia formatu plików XML polegała na przechowywaniu i przesyłaniu danych bez uzależnienia od oprogramowania lub narzędzi sprzętowych. Jego popularność wynika z tego, że jest czytelny zarówno dla ludzi, jak i dla maszyn. Umożliwia to tworzenie wspólnych protokołów danych w postaci obiektów, które mają być przechowywane i udostępniane w sieci, takiej jak World Wide Web (WWW). „X” w XML oznacza rozszerzalny, co oznacza, że język można rozszerzyć do dowolnej liczby symboli, zgodnie z wymaganiami użytkownika. To właśnie dla tych funkcji wykorzystuje go wiele standardowych formatów plików, takich jak Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/pl/web/xhtml/)** i **[SVG](/pl/page-description-language /svg/)**.

## Format pliku XML

Format pliku XML jest oparty na XML Document Object Model (DOM), który jest programistycznym interfejsem API dla dokumentów HTML i XML. XML DOM definiuje standardową metodę uzyskiwania dostępu do elementów dokumentu XML i manipulowania nimi. Tworzy widok struktury drzewa dokumentu XML, którego można użyć do uzyskania dostępu do wszystkich elementów poprzez drzewo DOM. Istniejące elementy można modyfikować/usuwać, a także tworzyć nowe elementy w drzewie XML. Każdy element dokumentu XML jest nazywany węzłem. XML DOM jest pokazany na poniższej ilustracji.

{{< figure src="../XML DOM.png" alt="DOM XML" >}}

### Uniwersalne podejście XML

Potęga XML sprawia, że jest to uniwersalny język komunikacji danych w sieci, upraszczając transport danych i zmiany platformy. Zapewnia to również możliwość wymiany danych między niekompatybilnymi systemami dzięki przechowywaniu danych w formacie zwykłego tekstu. HTML służy do reprezentacji danych w Internecie, podczas gdy XML służy do wymiany danych. Pary tagów znaczników używane w XML definiują kluczowe elementy struktury, które mają być wykorzystywane przez aplikacje czytające.

## Przykład XMLa

Poniżej przedstawiono uproszczony przykład katalogu płyt CD, w którym każdy rekord zawiera informacje o płytach CD, takie jak wykonawca, kraj, firma, cena i rok produkcji.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Bibliografia

* [XML – z Wikipedii](https://en.wikipedia.org/wiki/XML)

