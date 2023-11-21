{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File AXD - Formato file del gestore Web ASP.NET",
  "description" :"Scopri cos'è un file AXD e le API che possono creare e aprire file AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Cos'è un file AXD?

Un file AXD è un file di impostazioni Web utilizzato per gestire e recuperare richieste di risorse incorporate in ASP.NET. Comprende istruzioni per recuperare risorse incorporate come immagini, file JavaScript ([.JS](/it/web/js/)) e file [.CSS](/it/web/css/). I file AXD vengono utilizzati per inserire risorse nelle pagine lato client. Ciò consente alle pagine client di accedere a queste risorse sul server in modo standard.

## Formato file AXD

I file AXD vengono archiviati come file binari sul lato server. Si riferisce a un file del gestore Web in ASP.NET che sono componenti che generano risposte a richieste specifiche a un server Web. I file AXD eseguono un'elaborazione personalizzata prima di generare la risposta in base alle richieste della pagina lato client. Questi vengono in genere salvati come file **WebResource.axd**.

### Cos'è il file WebResource.axd?

La maggior parte dei progetti ASP.NET salva file AXD come file WebResource.axd che consentono alle pagine sul lato client di scaricare risorse incorporate in un assembly. La tua applicazione potrebbe riscontrare prestazioni lente nel caso in cui la esegui in modalità debug poiché il gestore WebResources.axd non è memorizzato nella cache.

## Riferimenti

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

