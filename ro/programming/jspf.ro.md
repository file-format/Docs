{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - Format de fișier fragment JSP",
  "description":"Aflați despre formatul de fișier JSPF și despre API-urile care pot crea și deschide fișiere JSPF.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Ce este un fișier JSPF?
Fișierul cu extensia .jspf se numește fragment JSP; un fișier static inclus într-un alt fișier JSP. Fișierele JSPF nu sunt compilate singure, cu toate acestea, ele sunt compilate alături de pagina în care au inclus. Sintaxa sa este similară cu codul Java Server Pages (JSP). Conține doar un fragment de JSP; nu a inclus întregul document JSP.

## Format de fișier JSPF
Termenul „segment JSP” este folosit în schimb, deoarece termenul „fragment JSP” este supraîncărcat în specificația JSP 2.0. Fragmentele JSP pot folosi fie extensii .jsp, fie .jspf și ar trebui plasate fie în **/WEB-INF/jspf**, fie cu restul fișierelor statice. Fragmentele JSP care nu sunt pagini complete trebuie să utilizeze extensia .jspf și trebuie să fie plasate în **/WEB-INF/jspf**

### JSP sau JSP Fragment File Organization
Un fișier JSP conține următoarele secțiuni în ordinea în care sunt listate:

1. Comentarii de deschidere
2. Directivele de pagină JSP
3. Directive opționale de bibliotecă de etichete
4. Declarații opționale JSP
5. Cod HTML și JSP

Un fișier JSP sau JSPF începe ambele cu un comentariu de stil pe partea serverului care se numește **Opening Comment**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Acest comentariu poate fi vizibil numai pe partea serverului, deoarece este eliminat în timpul redării paginii JSP.

## Când să utilizați fișierul JSP Fragment?
Atunci când o pagină JSP necesită o anumită structură, dar complexă, care poate fi reutilizată și în alte pagini JSP, o modalitate de a gestiona acest lucru este de a o împărți în bucăți, folosind modelul de vizualizare compusă (secțiunea Patterns din Java Blueprints). De exemplu, o pagină JSP are uneori următorul aspect logic în structura sa de prezentare:

{{< figure src="../jspf.png" alt="Format de fișier JSPF" >}}

În această situație, această pagină JSP compusă poate fi convertită în diverse module, fiecare va fi numit un fragment JSP separat. Fragmentele JSP pot fi apoi plasate în locații adecvate în pagina JSP compusă. Prin urmare, fișierul JSPF este folosit atunci când directivele de includere statice sunt folosite pentru a include o pagină care nu ar fi apelată de la sine, fișierele cu extensia .jspf ar trebui să fie plasate în directorul /WEB-INF/jspf/ al arhivei aplicației Web ( război).

## Exemplu JSPF
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

## Referințe

* [Convenții de cod pentru paginile JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

