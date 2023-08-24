{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - plik języka znaczników ColdFusion",
  "description" :"Dowiedz się, co to jest plik CFML i interfejsy API, które mogą tworzyć i otwierać pliki CFML.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Czym jest plik CFML?

Plik z rozszerzeniem .cfml to plik języka ColdFusion Markup Language, który służy do tworzenia strony internetowej. Odnosi się do zestawu reguł używanych do określenia, w jaki sposób aplikacja ColdFusion będzie rozwijana przez programistę. ColdFusion to język programowania używany do szybkiego tworzenia aplikacji internetowych po stronie serwera i przy użyciu mniej niż inne technologie, takie jak [ASP](/pl/web/asp/), [PHP](/pl/programming/php/) itp. Niektóre z aplikacji, które mogą otwierać pliki CML, to Adobe ColdFusion 2018, Adobe ColdFusion Builder i Adobe Dreamweaver.

## Format pliku CFML — więcej informacji

Pliki CFML są plikami znaczników i zawierają elementy sieciowe w postaci tagów. Są to pliki tekstowe, które można otwierać i edytować w dowolnym edytorze tekstu. Pliki CFML składają się z kilku tagów, które są podobne do [HTML](/pl/web/html/) i zwykle składają się z tagu otwierającego i zamykającego. Te znaczniki mogą również zawierać jeden lub więcej atrybutów.

### Składnia znaczników

Poniżej przedstawiono ogólną składnię znaczników CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Większość tagów akceptuje atrybuty i jest zdefiniowana w następujący sposób.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Niektóre z tych tagów akceptują również wiele atrybutów z następującą składnią.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Przykład kodu CFML

Oto przykład użycia rzeczywistego tagu CFML — tagu `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Bibliografia

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

