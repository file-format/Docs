{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSP Fragment File Format",
  "description":"Další informace o formátu souborů JSPF a rozhraních API, která mohou vytvářet a otevírat soubory JSPF.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Co je soubor JSPF?
Soubor s příponou .jspf se nazývá fragment JSP; statický soubor zahrnutý v jiném souboru JSP. Soubory JSPF nejsou kompilovány samy o sobě, jsou však kompilovány vedle stránky, na které byly zahrnuty. Jeho syntaxe je podobná kódu Java Server Pages (JSP). Obsahuje pouze fragment JSP; nezahrnuje celý dokument JSP.

## Formát souboru JSPF
Místo toho se používá výraz „segment JSP“, protože výraz „fragment JSP“ je ve specifikaci JSP 2.0 přetížen. Fragmenty JSP mohou používat přípony .jsp nebo .jspf a měly by být umístěny buď v **/WEB-INF/jspf** nebo se zbytkem statických souborů. Fragmenty JSP, které nejsou úplnými stránkami, musí používat příponu .jspf a musí být umístěny v **/WEB-INF/jspf**

### Organizace souborů JSP nebo fragmentů JSP
Soubor JSP obsahuje následující sekce v pořadí, v jakém jsou uvedeny:

1. Otevírání komentářů
2. Direktivy stránky JSP
3. Volitelné direktivy knihovny značek
4. Nepovinné prohlášení JSP
5. HTML a JSP kód

Soubor JSP nebo JSPF začíná komentářem ve stylu na straně serveru, který se nazývá **Otevírací komentář**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Tento komentář může být viditelný pouze na straně serveru, protože je odstraněn během vykreslování stránky JSP.

## Kdy použít soubor fragmentu JSP?
Když stránka JSP vyžaduje určitou, ale složitou strukturu, kterou lze také znovu použít na jiných stránkách JSP, jedním ze způsobů, jak to vyřešit, je rozdělit ji na kousky pomocí vzoru Composite View (část Vzory v Java Blueprints). Například stránka JSP má někdy ve struktuře prezentace následující logické uspořádání:

{{< figure src="../jspf.png" alt="Formát souboru JSPF" >}}

V této situaci lze tuto složenou stránku JSP převést na různé moduly, z nichž každý bude nazýván samostatným fragmentem JSP. Fragmenty JSP lze poté umístit na vhodná místa na složené stránce JSP. Soubor JSPF se tedy používá, když se statické direktivy začlenění používají k zahrnutí stránky, která by se sama o sobě nevolala, soubory s příponou .jspf by měly být umístěny v adresáři /WEB-INF/jspf/ archivu webové aplikace ( válka).

## Příklad JSPF
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

## Reference

* [Konvence kódu pro stránky JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

