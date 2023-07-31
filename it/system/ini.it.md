{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "estensione", "file", "formato", "sistema", "Iniziazione", "estensione directory", "programmi", "computer", "applicazione" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Formato file di avvio",
  "description":"Scopri il formato di file INI e le API che possono creare e aprire file INI.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Che cos'è un file INI? ##

Un file INI è un documento di configurazione dei messaggi per programmi per computer che contengono chiavi pubbliche per caratteristiche e sezioni che organizzano gli attributi in un framework e una grammatica. Questi documenti di configurazione del formato file di sistema prendono il nome dall'estensione di directory INI del sistema operativo MS-DOS, che sta per iniziazione. Ha reso popolare questa forma di configurazione del software. Molti programmi su altre applicazioni software utilizzano varie aggiunte di nomi di file, come CONF e [CFG](/it/system/cfg/), sebbene il formato abbia stabilito uno standard non ufficiale in molte situazioni di configurazione.

## Breve storia dei file INI##

Inizialmente, la principale tecnica di configurazione del programma di Windows era un formato di file di testo che consisteva in righe di testo con una coppia cruciale per riga, suddivise in sezioni. I driver di dispositivo, i caratteri tipografici e i lanciatori di avvio sono stati tutti archiviati in questo formato. Anche le singole impostazioni venivano comunemente archiviate nei file INI dalle app.
Fino a Windows 3.1x, il formato era supportato su piattaforme Microsoft Windows a 16 bit. A partire da Windows 95, Microsoft ha iniziato a incoraggiare gli sviluppatori a utilizzare il registro di Windows anziché i file INI per la configurazione.

## File INI - Specifiche del formato file

### Chiavi/Proprietà ###

La chiave/proprietà è l'elemento più basilare di un file INI. Un simbolo di uguale (=) separa il nome e il valore di ciascuna chiave. A sinistra del segno di uguale è dove viene visualizzato il nome. Il simbolo uguale e il punto e virgola sono lettere discrete nel sistema Windows, quindi non possono essere utilizzati nella chiave. Qualsiasi carattere può essere utilizzato nel valore.

```
name=value
```

### Sezioni ###

Il commento della sezione viene visualizzato tra parentesi quadre ([]) sulla propria riga. Dopo la definizione della sezione, tutte le chiavi sono collegate a quella sezione. Le sezioni terminano alla designazione della sezione successiva o alla fine del documento; non esiste un separatore di "fine sezione" specifico. Le sezioni non possono essere impilate; possono essere nominati solo una volta e non è necessario che siano collegati.

```
[section]
a=a
b=b
```

### Modifica delle funzionalità ###

Il formato del file INI non ha una definizione accettata a livello globale. Molte applicazioni per computer includono funzioni in aggiunta a quelle già menzionate. L'elenco seguente include alcune caratteristiche comuni che possono essere incluse o meno in ogni singolo programma.

* Commenti
* Caratteri di escape
* Nomi duplicati


## Esempio INI ##

Il file INI di esempio ha il seguente aspetto:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Riferimento ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

