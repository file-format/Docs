{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File HDMP - Formato file di dump dell'heap di Windows",
  "description":"Scopri il formato di file HDMP e le API che possono creare e aprire file HDMP.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Che cos'è un file HDMP?

Il file HDMP è un dump della memoria non compresso quando un'applicazione o un programma si arresta in modo anomalo a causa di un errore. Viene creato solo da Windows XP/Vista e contiene un dump dello stato dell'applicazione al momento dell'arresto anomalo. Essendo non compressi, i file HDMP occupano più spazio sul disco rispetto ai file Minidump [MDMP](/it/system/mdmp/) compressi a scopo di reporting.

Le applicazioni che possono essere utilizzate per **aprire** o analizzare file HDMP includono Microsoft Visual Studio con strumenti di debug per Windows.

## Formato file HDMP

I file HDMP vengono archiviati su disco come file binari e non offrono alcun vantaggio se aperti senza le applicazioni appropriate. Questi contengono dati di sistema rilevanti registrati quando si è verificato l'errore.

### Differenza tra i formati di file HDMP e MDMP

Gli HDMP sono file di dump della memoria non compressi. Al contrario, MDMP sono file mini dump che vengono compressi per la riduzione delle dimensioni del file e inviati a Microsoft per segnalare il problema.

## Riferimento ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

