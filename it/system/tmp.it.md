{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "estensione", "file", "formato", "sistema", "file TMP", "documenti TMP", "file TMP", "file temporaneo", "applicazione", "programmi" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Formato file temporaneo",
  "description":"Scopri il formato di file TMP e le API che possono creare e aprire file TMP.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Che cos'è un file TMP? ##

Un file TMP si riferisce a un backup transitorio, archiviazione o altro file system generato da un programma software. Occasionalmente viene creato come file invisibile e viene spesso distrutto quando si chiude il programma. I file TMP possono essere utilizzati anche per memorizzare temporaneamente informazioni durante la creazione di un nuovo file.

## Formato file TMP ##

Un file TMP è in genere costituito da dati grezzi che vengono utilizzati come fase nel processo di conversione del materiale da uno stile all'altro. Microsoft Word e Apple Safari sono due app in grado di produrre e utilizzare il formato file TMP.

I documenti TMP generati dovrebbero, in teoria, essere rimossi automaticamente alla chiusura del programma o allo spegnimento della macchina. In pratica, non è sempre così. Di conseguenza, mentre navighi tra i documenti del tuo programma, potresti imbatterti in file temporanei che non vengono utilizzati attivamente dal sistema o da qualsiasi altro software.

### Memoria ausiliaria ###

La memoria virtuale viene utilizzata nei sistemi operativi, tuttavia, i programmi che utilizzano enormi volumi di informazioni potrebbero dover creare documenti temporanei.

### Comunicazione tra processi ###

La maggior parte dei sistemi operativi fornisce primitive per il passaggio di dati tra programmi, come pipe, socket o memoria principale, ma il metodo più semplice consiste nel trasferire i file in un file temporaneo e avvisare l'applicazione ricevente della posizione del file temporaneo.


## Specifiche tecniche ##

L'ottenimento di nomi di documenti temporanei distintivi è solitamente fornito da sistemi operativi e programmi software.
I file temporanei possono essere generati in sicurezza su sistemi POSIX utilizzando le funzioni della libreria mkstemp o tmpfile. Alcuni sistemi includono la precedente applicazione mktemp POSIX (poiché scomparsa). Questi file si trovano solitamente nella normale directory temporanea sulle piattaforme Unix in /TMP, o %TEMP% (è specifico per il login) sui computer Windows.

Quando il programma si arresta o il documento viene chiuso, il file transitorio generato con tmpfile viene automaticamente rimosso. GetTempFileName (Windows) o tmpnam (POSIX) possono essere utilizzati per creare un nome di file temporaneo che durerà più a lungo del programma che lo ha creato.

## Riferimento ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
