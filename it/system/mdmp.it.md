{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File MDMP - Formato file minidump di Windows",
  "description":"Scopri il formato di file MDMP e le API che possono creare e aprire file MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Che cos'è un file MDMP?

Un file MDMP è un dump della memoria di un'applicazione su Microsoft Windows creata quando l'applicazione si chiude in modo anomalo o si arresta in modo anomalo. Contiene informazioni e dump di dati che possono essere utilizzati per eseguire il debug della causa dell'arresto anomalo. I file MDMP sono applicabili su applicazioni create da qualsiasi piattaforma come Java, C++, .NET e altre. Oltre a MDMP,

Le applicazioni in grado di aprire file MDMP includono Microsoft Visual Studio Debugger.

## Formato file MDMP

I file MDMP vengono salvati come file binari su disco e possono essere aperti con il debugger di Microsoft Visual Studio. Contiene le seguenti informazioni per aiutare a identificare il motivo dell'arresto anomalo.

* Dettagli del messaggio Stop, i suoi parametri e altri dati
* Elenco dei driver caricati
* Contesto del processore (PRCB) per il processore che ha smesso di funzionare
* Informazioni sul processo e contesto del kernel (EPROCESS) per il processo interrotto
* Informazioni sul processo e contesto del kernel (ETHREAD) per il thread interrotto
* Stack di chiamate in modalità kernel per il thread interrotto

Queste informazioni aiutano a scoprire cosa è successo, risolvere il problema e impedire che si ripeta.

### Analizza Minidump

Windows richiede un file di paging nel volume di avvio per creare un file di dump della memoria. Il file di paging viene creato nel volume di avvio e deve avere una dimensione di almeno 2 megabyte (MB). Il file di dump viene creato quando un'applicazione si arresta in modo anomalo. In caso di un secondo problema, viene creato un secondo piccolo file di dump della memoria mentre viene mantenuto il precedente. Il nome del file di dump è distinto per evitare qualsiasi sovrascrittura.

Windows mantiene un elenco di tutti i file di dump della memoria nella cartella %SystemRoot%\Minidump. Puoi analizzare i file MDMP eseguendoli in Visual Studio Debugger come elencato nei passaggi seguenti.

## Come si apre un file MDMP in Visual Studio?

I passaggi seguenti possono essere usati per aprire un file MDMP in Visual Studio.

* In Visual Studio, dal menu File, scegliere Apri | Discarica d'urto.
* Passare al file di dump che si desidera aprire.
* Seleziona Apri.

## Riferimento

* [Come leggere il file di dump della memoria di piccole dimensioni creato da Windows in caso di arresto anomalo](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -file)

