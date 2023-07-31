{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","file asmx", "formato file asmx", "tipo di file asmx", "file", "tipo", "cos'è un file asmx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - File del servizio Web ASP.NET",
  "description" :"Scopri cos'è un file ASMX e le API che possono creare e aprire file ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Che cos'è un file ASMX?

Un file con estensione .asmx è un file del servizio Web ASP.NET che fornisce la comunicazione tra due oggetti su Internet utilizzando il Simple Object Access Protocol (SOAP). Viene distribuito come servizio sul server Web basato su Windows per elaborare la richiesta in arrivo e restituire la risposta. A differenza dei file [ASPX](/it/web/aspx/) che contengono il codice per la visualizzazione visiva delle pagine Web ASP.NET, i file ASMX vengono eseguiti sul server in background ed eseguono diverse attività come la connessione al database, il recupero dei dati e la restituzione in un formato in cui è stata presentata la richiesta. Questi sono usati specificamente per i servizi web XML.

## Formato file ASMX

I file ASMX sono in formato testo normale e possono essere aperti o modificati in applicazioni come Microsoft Visual Studio o editor di testo. È un formato di file proprietario di Microsoft e ha una sintassi ben definita per la creazione di servizi web. Una risposta di un file ASMX sotto forma di SOAP XML ha i seguenti elementi.

* `Envelop` - Un elemento radice che identifica il documento XML come messaggio SOAP.
* `Header` - Un elemento facoltativo che contiene informazioni specifiche dell'applicazione come i dati di autenticazione. Se l'elemento Header è presente, deve essere il primo elemento figlio dell'elemento Envelope.
* `Body` - Contiene il messaggio SOAP destinato al destinatario.
* `Fault` - Un elemento opzionale utilizzato per indicare i messaggi di errore. Se l'elemento Fault è presente, deve essere un elemento figlio dell'elemento Body.

I file ASMX possono essere scritti in linguaggi .NET come [C#](/it/programming/cs/), [Visual Basic](/it/programming/vb/) o JScript.

## In che modo ASMX è diverso da ASPX e ASCX?

I file ASMX sono diversi dai file ASPX e ASCX.

* ASPX, Active Server Pages, i file sono file di programmazione generati utilizzando il framework Microsoft ASP.NET in esecuzione su server Web. Questi vengono visualizzati nel browser Web del client quando l'utente richiede di accedere a tale pagina.
* ASCX, Active Server User Control, definisce i controlli utente utilizzati per definire i controlli riutilizzabili nelle pagine Web ASP.NET o nell'intero sito Web.

## Riferimenti

* [Utilizzo del servizio ASMX](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Controllo utente ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

