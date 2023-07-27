{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","file ascx", "formato file ascx", "tipo di file ascx", "file", "tipo", "cos'è un file ascx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file ASCX",
  "description" :"Scopri cos'è un file ASCX e le API che possono creare e aprire file ASCX.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Che cos'è un file ASCX?

Un file con estensione .ascx è un controllo utente utilizzato come componente riutilizzabile nelle pagine Web. Viene referenziato in qualsiasi sito Web ASP trascinandolo dalla casella di controllo alla pagina. I controlli degli utenti ASCX vengono aggiunti al progetto come fonte centrale, con il risultato che qualsiasi modifica nel controllo utente si riflette sull'intero sito web. A differenza dei file ASMX che definiscono un meccanismo per comunicare all'interno di 2 oggetti su Internet, i file ASCX sono controlli utente per l'incorporamento in pagine o siti Web.

## Formato file ASCX

I file ASCX vengono scritti in formato di testo normale e possono utilizzare il codice dietro funzionalità come le pagine Web che terminano con .ascx.cs. Il codice di markup dei controlli utente inizia con la direttiva @Control, come mostrato nell'esempio seguente.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Questo controllo utente Web può essere riutilizzato su molte pagine come piè di pagina, intestazione o qualche tipo di navigazione del sito. I controlli utente Web hanno proprietà, metodi ed eventi come qualsiasi altro controllo che li rende utili per impostare il loro comportamento visivo.

### Esempio di registrazione dei controlli utente in web.config

Per utilizzare un unico controllo utente su più pagine, il controllo web può essere registrato in web.config. Ciò consente di utilizzare il controllo su tutto il sito Web invece di registrarsi su ciascuna pagina individualmente. Il codice di esempio seguente definisce come registrare un controllo Web in web.config da visualizzare come piè di pagina sull'intero sito Web.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Riferimenti

* [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [Controllo utente ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

