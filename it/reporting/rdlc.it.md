{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Report Definition Language lato client",
  "keywords" :[ "rdlc", "report Definition Language", "formato mkv", "XSD", "Report Definition Language lato client"],
  "description":"Informazioni sul formato di file RDLC che è una rappresentazione XML di una definizione di report di SQL Server Reporting Services.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Che cos'è un file RDLC? ##

RDLC sta per Report Definition Language lato client. In realtà è un'estensione del file di report creato utilizzando la tecnologia di reporting di Microsoft. Per creare questi file viene utilizzata la versione SQL Server 2005 di Progettazione report. Il controllo **ReportViewer** sul lato client può eseguire direttamente i report RDLC.

## File RDL VS RDLC
|File .rdl |File .rdlc|
---|---|
|I file RDL vengono creati dalla versione SQL Server 2005 di Report Designer|I file RDLC vengono creati dalla versione Visual Studio 2005 di Report Designer|
|Viene utilizzato in SQL Server Reporting Services|Viene utilizzato in Visual Studio|
|E' un report remoto|E' un report locale|
|È necessaria un'istanza di Reporting Services per eseguirla|Non è necessaria un'istanza di Reporting Services|

## Creazione di file di definizione report client (.rdlc).
Il controllo ReportViewer viene utilizzato per eseguire i file di definizione dei report client (.rdlc) utilizzando la funzionalità di elaborazione incorporata del controllo. I report client eseguiti in modalità di elaborazione locale possono essere facilmente creati nel progetto dell'applicazione. Di seguito sono riportati gli approcci per la creazione del report:

- Utilizzare la **Procedura guidata report** per creare una nuova definizione di report client (.rdlc).

- Creare un nuovo file di definizione del report client (.rdlc) usando Visual Studio.

- Genera una definizione di report a livello di codice.


È possibile visualizzare in anteprima un report solo eseguendolo in un controllo **ReportViewer**. Tieni presente che puoi aprire e modificare la definizione del rapporto in qualsiasi momento, quindi creare o distribuire l'applicazione per verificare i risultati.

## Riferimenti ##

- [Creazione di file di definizione report client (.rdlc)](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

