{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File MASTER - Formato file di pagina master ASP.NET",
  "description" :"Ulteriori informazioni sul formato file MASTER e sulle API per creare e aprire file MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Cos'è un file MASTER?

Un file MASTER è un file modello di pagina Web principale creato con ASP.NET. Viene utilizzato come punto di partenza per creare più pagine con lo stesso layout e le stesse impostazioni del file MASTER. Il file MASTER del modello include impostazioni per intestazione, menu di navigazione, piè di pagina, carattere e informazioni sullo stile. L'utilizzo di un file MASTER aiuta a creare rapidamente più pagine Web.

Puoi aprire un file MASTER utilizzando Microsoft Visual Studio 2022 e versioni successive.

## Formato file MASTER - Ulteriori informazioni

Un file MASTER viene creato e salvato in formato file HTML ed è simile a qualsiasi altro file di pagina web. È suddiviso in sezioni modificabili e non modificabili. Le sezioni modificabili sono quelle che possono essere modificate per soddisfare le esigenze dell'utente. Le sezioni non modificabili vengono disattivate quando il file MASTER viene aperto in Microsoft Visual Studio.

Le pagine master sono costituite da due parti, ovvero la pagina master stessa e una o più pagine di contenuto.

### Pagina MASTER

La pagina master ha estensione .master ed è realizzata in ASP.NET. Ha un layout predefinito che comprende testo statico, tag HTML e controlli lato server. Nelle pagine .aspx ordinarie viene utilizzata la direttiva @ Page. In caso di file .master, questo viene sostituito dalla direttiva @Master.

### Pagine di contenuto

Una pagina di contenuto rappresenta il contenuto per i controlli segnaposto della pagina master. Si tratta di pagine .aspx che rappresentano effettivamente il code-behind della pagina master. Le pagine di contenuto vengono vincolate utilizzando la direttiva @ Page includendo un attributo MasterPageFile che punta alla pagina master da utilizzare come mostrato di seguito.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Riferimenti

* [Panoramica delle pagine Master ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

