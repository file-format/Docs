{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file TPSR - File di rapporto della sessione pilota di TeamViewer",
  "description":"Scopri il formato di file TPSR e le API che possono creare e aprire file TPSR.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## Che cos'è un file TPSR?

Un TPSR è un file di protocollo di connessione utilizzato da TeamViewer Assist AR (precedentemente noto come TeamViewer Pilot). Le informazioni memorizzate in un file TPSR vengono archiviate nel formato di file compresso [ZIP](/it/compression/zip/). TPSR contiene la cronologia dettagliata della connessione di TeamViewer tra un esperto e un tecnico per la risoluzione dei problemi e la revisione. Le informazioni contenute in un file TPSR includono tipo di dispositivo, nome, ID Assist AR, ID esperto, data e ora e durata della connessione. Questi dati vengono archiviati in un file [JSON](/it/web/json/) all'interno dell'archivio TPSR compresso.

## Formato file TPSR

Un file TPSR viene archiviato su disco in formato di file di archivio ZIP in cui i contenuti sono archiviati all'interno di un file JSON. Viene generato automaticamente dopo il completamento della connessione Assist AR, a condizione che l'opzione Report connessione sia abilitata in TeamViewer.

TeamViewer Assist AR consente agli esperti di connettersi ai tecnici per ottenere feed LIVE dell'estremità remota tramite la videocamera mobile. Possono assistere i tecnici per risolvere il problema al telefono.

## Apri file TPSR

È possibile aprire i file TPSR utilizzando la versione desktop del software TeamViewer. Se installato sul computer, facendo doppio clic sul file TPSR lo si aprirà nel software TeamViewer. I file TPSR possono essere esportati anche in file [PDF](/it/pdf/) o possono essere stampati per avere una copia stampata del file di protocollo.

## Riferimenti ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

