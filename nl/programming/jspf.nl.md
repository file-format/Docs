{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSP-fragmentbestandsindeling",
  "description":"Meer informatie over JSPF-bestandsindeling en API's die JSPF-bestanden kunnen maken en openen.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Wat is een JSPF-bestand?
Het bestand met de extensie .jspf wordt JSP-fragment genoemd; een statisch bestand dat is opgenomen in een ander JSP-bestand. De JSPF-bestanden worden niet op zichzelf gecompileerd, maar worden naast de pagina gecompileerd waarin ze zijn opgenomen. De syntaxis is vergelijkbaar met de Java Server Pages-code (JSP). Het bevat slechts een fragment van JSP; niet het hele JSP-document bevatte.

## JSPF-bestandsindeling
In plaats daarvan wordt de term "JSP-segment" gebruikt omdat de term "JSP-fragment" overbelast is in de JSP 2.0-specificatie. De JSP-fragmenten kunnen de extensie .jsp of .jspf gebruiken en moeten in **/WEB-INF/jspf** of bij de rest van de statische bestanden worden geplaatst. De JSP-fragmenten die geen volledige pagina's zijn, moeten de .jspf-extensie gebruiken en moeten worden geplaatst in **/WEB-INF/jspf**

### JSP- of JSP-fragmentbestandsorganisatie
Een JSP-bestand bevat de volgende secties in de volgorde waarin ze worden vermeld:

1. Opmerkingen openen
2. JSP-paginarichtlijn(en)
3. Optionele tagbibliotheekrichtlijn(en)
4. Optionele JSP-aangifte(n)
5. HTML- en JSP-code

Een JSP- of JSPF-bestand begint beide met een opmerking in serverstijl die **Openingcommentaar** wordt genoemd:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Deze opmerking is alleen zichtbaar aan de serverzijde omdat deze wordt verwijderd tijdens het renderen van JSP-pagina's.

## Wanneer JSP-fragmentbestand gebruiken?
Wanneer een JSP-pagina een bepaalde maar complexe structuur vereist die ook in andere JSP-pagina's kan worden hergebruikt, is een manier om dit aan te pakken deze in stukken op te splitsen met behulp van het Composite View-patroon (de sectie Patronen van Java Blueprints). Zo heeft een JSP-pagina soms de volgende logische indeling in de presentatiestructuur:

{{< figure src="../jspf.png" alt="JSPF-bestandsindeling" >}}

In deze situatie kan deze samengestelde JSP-pagina worden omgezet in verschillende modules, die elk een apart JSP-fragment worden genoemd. De JSP-fragmenten kunnen vervolgens op de juiste locaties op de samengestelde JSP-pagina worden geplaatst. Daarom wordt het JSPF-bestand gebruikt wanneer statische include-richtlijnen worden gebruikt om een pagina op te nemen die op zichzelf niet zou worden aangeroepen. De bestanden met de extensie .jspf moeten in de directory /WEB-INF/jspf/ van het webtoepassingsarchief worden geplaatst ( oorlog).

## JSPF-voorbeeld
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

## Referenties

* [Codeconventies voor de JavaServer-pagina's](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

