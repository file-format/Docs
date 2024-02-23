{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File EAZ - Cos'è un file EAZ e come aprirlo?",
  "description":"Scopri il formato file EAZ e le API che possono creare e aprire file EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-itz"
}
},
  "lastmod" : "2023-12-23"
}

## Cos'è un file EAZ?

Il file EAZ è un file aggiuntivo utilizzato da ArcGIS Explorer, un'applicazione gratuita sviluppata da ESRI per l'esplorazione, la visualizzazione e la condivisione delle mappe. Contiene un archivio di file compressi che include un [XML file](/web/xml/), codice compilato e file di supporto necessari per il componente aggiuntivo. Questi file vengono utilizzati per espandere le funzionalità di base del software incorporando nuovi pulsanti, finestre agganciabili e altre estensioni.

## Formato file EAZ: ulteriori informazioni

I file EAZ vengono creati tramite l'utilizzo di ArcGIS Explorer SDK, un kit di sviluppo progettato per creare funzionalità personalizzate all'interno di ArcGIS Explorer. Questi file utilizzano la compressione [ZIP](/compression/zip/) per comprimere in modo efficiente i loro contenuti. Al centro dell'archivio, il file **Addins.xml** risiede nella directory principale e funge da componente vitale che delinea e descrive in dettaglio le varie personalizzazioni incorporate nel file EAZ.

Il file Addins.xml funge essenzialmente da tabella di marcia, offrendo approfondimenti su miglioramenti, modifiche ed estensioni specifici introdotti dal file EAZ in ArcGIS Explorer. Attraverso questa struttura completa, gli sviluppatori possono incapsulare e integrare perfettamente nuove funzionalità, pulsanti e finestre agganciabili, migliorando la funzionalità complessiva e l'esperienza utente dell'applicazione ArcGIS Explorer.

## Riferimenti

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
