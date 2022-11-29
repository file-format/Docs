{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSP Fragment File Format",
  "description":"Läs mer om JSPF-filformat och API:er som kan skapa och öppna JSPF-filer.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Vad är JSPF fil?
Filen med tillägget .jspf kallas JSP-fragment; en statisk fil som ingår i en annan JSP-fil. JSPF-filerna kompileras inte på egen hand, men de kompileras längs sidan där de ingår. Dess syntax liknar Java Server Pages (JSP)-koden. Den innehåller bara ett fragment av JSP; inkluderade inte hela JSP-dokumentet.

## JSPF filformat
Termen "JSP-segment" används istället eftersom termen "JSP-fragment" är överbelastad i JSP 2.0-specifikationen. JSP-fragmenten kan använda antingen .jsp- eller .jspf-tillägg och bör placeras antingen i **/WEB-INF/jspf** eller med resten av de statiska filerna. JSP-fragmenten som inte är kompletta sidor måste använda tillägget .jspf och måste placeras i **/WEB-INF/jspf**

### JSP eller JSP Fragment File Organization
En JSP-fil innehåller följande avsnitt i den ordning de är listade:

1. Öppningskommentarer
2. JSP-sidedirektiv(er)
3. Valfria direktiv(er) om taggbibliotek
4. Valfri JSP-deklaration(er)
5. HTML- och JSP-kod

En JSP- eller JSPF-fil börjar båda med en kommentar på serversidan som kallas **Öppningskommentar**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Den här kommentaren kan bara vara synlig på serversidan eftersom den tas bort under JSP-sidans rendering.

## När ska jag använda JSP Fragment-fil?
När en JSP-sida kräver en viss men komplex struktur som också kan återanvändas på andra JSP-sidor, är ett sätt att hantera detta att dela upp den i bitar, med hjälp av Composite View-mönstret (Patterns-sektionen i Java Blueprints). Till exempel har en JSP-sida ibland följande logiska layout i sin presentationsstruktur:

{{< figure src="../jspf.png" alt="JSPF filformat" >}}

I den här situationen kan denna sammansatta JSP-sida konverteras till olika moduler, var och en kommer att kallas ett separat JSP-fragment. JSP-fragmenten kan sedan placeras på lämpliga platser på den sammansatta JSP-sidan. Därför används JSPF-filen när statiska include-direktiv används för att inkludera en sida som inte skulle anropas av sig själv, filerna med .jspf-tillägget ska placeras i katalogen /WEB-INF/jspf/ i webbapplikationsarkivet ( krig).

## JSPF-exempel
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

## Referenser

* [Kodkonventioner för JavaServer-sidorna](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

