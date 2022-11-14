{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - Formato file frammento JSP",
  "description":"Scopri il formato di file JSPF e le API che possono creare e aprire file JSPF.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Che cos'è un file JSPF?
Il file con estensione .jspf è chiamato frammento JSP; un file statico incluso in un altro file JSP. I file JSPF non vengono compilati da soli, tuttavia, vengono compilati accanto alla pagina in cui sono inclusi. La sua sintassi è simile al codice JSP (Java Server Pages). Contiene solo un frammento di JSP; non incluso tutto l'intero documento JSP.

## Formato file JSPF
Il termine "segmento JSP" viene invece utilizzato poiché il termine "frammento JSP" è sovraccaricato nella specifica JSP 2.0. I frammenti JSP possono utilizzare le estensioni .jsp o .jspf e devono essere inseriti in **/WEB-INF/jspf** o con il resto dei file statici. I frammenti JSP che non sono pagine complete devono utilizzare l'estensione .jspf e devono essere inseriti in **/WEB-INF/jspf**

### Organizzazione del file di frammenti JSP o JSP
Un file JSP contiene le seguenti sezioni nell'ordine in cui sono elencate:

1. Commenti di apertura
2. Direttive della pagina JSP
3. Direttive facoltative della libreria di tag
4. Dichiarazioni JSP facoltative
5. Codice HTML e JSP

Un file JSP o JSPF inizia entrambi con un commento di stile lato server chiamato **Commento di apertura**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Questo commento può essere visibile solo sul lato server perché viene rimosso durante il rendering della pagina JSP.

## Quando utilizzare il file Frammento JSP?
Quando una pagina JSP richiede una struttura certa ma complessa che può essere riutilizzata anche in altre pagine JSP, un modo per gestirla è suddividerla in pezzi, utilizzando il pattern Composite View (la sezione Patterns di Java Blueprints). Ad esempio, una pagina JSP a volte ha il seguente layout logico nella sua struttura di presentazione:

{{< figure src="../jspf.png" alt="Formato file JSPF" >}}

In questa situazione, questa pagina JSP composita può essere convertita in vari moduli, ciascuno sarà chiamato un frammento JSP separato. I frammenti JSP possono quindi essere collocati in posizioni appropriate nella pagina JSP composita. Pertanto, il file JSPF viene utilizzato quando le direttive include statiche vengono utilizzate per includere una pagina che non verrebbe chiamata da sola, i file con estensione .jspf devono essere inseriti nella directory /WEB-INF/jspf/ dell'archivio dell'applicazione Web ( guerra).

## Esempio JSPF
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

## Riferimenti

* [Convenzioni sul codice per le pagine JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

