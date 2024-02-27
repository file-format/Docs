{
  "date": "2021-04-20",
  "keywords": [
"JSPF fil",
"jspf",
"JSPF eksempel",
"udvidelse",
"format",
"jspf tutorial",
"jsp fragment",
"JSPF filformat"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSPF - JSP Fragment File Format",
  "description": "Lær om JSPF-filformat og API'er, der kan oprette og åbne JSPF-filer.",
  "linktitle": "JSPF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jsp-daf"
}
},
  "lastmod": "2021-04-21"
}

## Hvad er en JSPF fil?
Filen med filtypenavnet .jspf kaldes JSP-fragment; en statisk fil inkluderet i en anden JSP-fil. JSPF-filerne kompileres ikke på egen hånd, men de kompileres langs siden, hvor de inkluderede. Dens syntaks ligner Java Server Pages (JSP)-koden. Den indeholder kun et fragment af JSP; ikke inkluderet hele JSP-dokumentet.

## JSPF filformat
Udtrykket JSP-segment bruges i stedet, da udtrykket JSP-fragment er overbelastet i JSP 2.0-specifikationen. JSP-fragmenterne kan bruge enten .jsp- eller .jspf-udvidelser og bør placeres enten i **/WEB-INF/jspf** eller med resten af de statiske filer. JSP-fragmenterne, der ikke er komplette sider, skal bruge .jspf-udvidelsen og skal placeres i **/WEB-INF/jspf**

### JSP eller JSP Fragment File Organization
En JSP-fil indeholder følgende sektioner i den rækkefølge, de er anført:

1. Åbningskommentarer
2. JSP-sidedirektiv(er)
3. Valgfri tagbiblioteksdirektiv(er)
4. Valgfri JSP-erklæring(er)
5. HTML og JSP kode

En JSP- eller JSPF-fil begynder begge med en kommentar på serversiden, som kaldes **Åbningskommentar**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Denne kommentar kan kun være synlig på serversiden, fordi den fjernes under gengivelse af JSP-side.

## Hvornår skal man bruge JSP Fragment-fil?
Når en JSP-side kræver en bestemt, men kompleks struktur, som også kan genbruges på andre JSP-sider, er en måde at håndtere dette på at dele den op i stykker ved at bruge Composite View-mønsteret (Patterns-sektionen i Java Blueprints). For eksempel har en JSP-side nogle gange følgende logiske layout i sin præsentationsstruktur:

{{< figure src="../jspf.png" alt="JSPF filformat" >}}

I denne situation kan denne sammensatte JSP-side konverteres til forskellige moduler, hver vil blive kaldt et separat JSP-fragment. JSP-fragmenterne kan derefter placeres på passende steder på den sammensatte JSP-side. Derfor bruges JSPF-filen, når statiske include-direktiver bruges til at inkludere en side, der ikke ville blive kaldt af sig selv, filerne med .jspf-udvidelsen skal placeres i mappen /WEB-INF/jspf/ i webapplikationsarkivet ( krig).

## JSPF eksempel
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

## Referencer

 * [Kodekonventioner for JavaServer-siderne](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

