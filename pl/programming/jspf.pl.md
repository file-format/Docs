{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - format pliku fragmentów JSP",
  "description":"Poznaj format pliku JSPF i interfejsy API, które mogą tworzyć i otwierać pliki JSPF.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Czym jest plik JSPF?
Plik z rozszerzeniem .jspf nazywa się fragmentem JSP; plik statyczny zawarty w innym pliku JSP. Pliki JSPF nie są kompilowane samodzielnie, ale są kompilowane wraz ze stroną, na której się znajdują. Jego składnia jest podobna do kodu Java Server Pages (JSP). Zawiera tylko fragment JSP; nie obejmuje całego dokumentu JSP.

## Format pliku JSPF
Zamiast tego używany jest termin „segment JSP”, ponieważ termin „fragment JSP” jest przeciążony w specyfikacji JSP 2.0. Fragmenty JSP mogą mieć rozszerzenia .jsp lub .jspf i powinny być umieszczone w **/WEB-INF/jspf** lub z resztą plików statycznych. Fragmenty JSP, które nie są kompletnymi stronami, muszą mieć rozszerzenie .jspf i muszą być umieszczone w **/WEB-INF/jspf**

### JSP lub Organizacja plików fragmentów JSP
Plik JSP zawiera następujące sekcje w kolejności, w jakiej są wymienione:

1. Otwieranie komentarzy
2. Dyrektywy strony JSP
3. Opcjonalne dyrektywy biblioteki znaczników
4. Opcjonalne deklaracje JSP
5. Kod HTML i JSP

Zarówno plik JSP, jak i JSPF rozpoczynają się od komentarza po stronie serwera, który nazywa się **Komentarz otwierający**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Ten komentarz może być widoczny tylko po stronie serwera, ponieważ jest usuwany podczas renderowania strony JSP.

## Kiedy używać pliku fragmentu JSP?
Gdy strona JSP wymaga określonej, ale złożonej struktury, którą można ponownie wykorzystać na innych stronach JSP, jednym ze sposobów radzenia sobie z tym jest podzielenie jej na części przy użyciu wzorca Composite View (sekcja Patterns w Java Blueprints). Na przykład strona JSP ma czasami następujący układ logiczny w swojej strukturze prezentacji:

{{< figure src="../jspf.png" alt="Format pliku JSPF" >}}

W tej sytuacji ta złożona strona JSP może zostać przekształcona w różne moduły, z których każdy będzie nazywany oddzielnym fragmentem JSP. Fragmenty JSP można następnie umieścić w odpowiednich miejscach na złożonej stronie JSP. Dlatego plik JSPF jest używany, gdy dyrektywy static include są używane do włączenia strony, która sama nie zostałaby wywołana, pliki z rozszerzeniem .jspf należy umieścić w katalogu /WEB-INF/jspf/ archiwum aplikacji WWW ( wojna).

## Przykład JSPF
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Bibliografia

* [Konwencje kodu dla stron JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

