{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "estensione", "file", "formato", "sistema", "Driver", "File di sistema", "programmi", "computer", "applicazione" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Formato file di sistema",
  "description":"Scopri il formato di file SYS e le API che possono creare e aprire file SYS.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Che cos'è un file SYS? ##

I file SYS sono "file di sistema" utilizzati nel sistema operativo Windows e nelle applicazioni MS-DOS. Questi file non possono essere aperti direttamente e sono costituiti dal driver e dalla configurazione del dispositivo. I file SYS sono responsabili del contenimento dei file delle funzioni principali del sistema operativo. Questi sono considerati file critici del driver del dispositivo e possono essere utilizzati anche quando è necessario risolvere qualsiasi problema del pilota. Questi sono responsabili del corretto funzionamento di un sistema informatico e i file .sys devono essere corretti e completi.


## Specifiche tecniche ##

I file .sys sono in realtà il sottoinsieme del formato [BMP](/it/image/bmp/) poiché consente solo combinazioni specifiche. Il formato normale di questi file è come LOGOS.SYS, LOGOW.SYS e LOGO.SYS. Tutti gli altri file non hanno questo formato.

Questi file vengono utilizzati principalmente all'interno della directory *C* di Windows al momento dell'installazione. La maggior parte dei problemi che ruotano attorno ai driver di dispositivo vengono risolti aggiornando il sistema operativo Windows. I dettagli e le informazioni di questi file possono essere visualizzati utilizzando i programmi integrati del sistema operativo Windows. Questi comprendono anche i riferimenti a diversi moduli in un sistema operativo.
Alcuni esempi di file di sistema sono:

* IO.SYS (questi memorizzano i driver di dispositivo del sistema operativo del disco)
* MSDOS.SYS (contengono il kernel o il codice principale del sistema operativo)
* CONFIG.SYS (contengono varie opzioni di configurazione)
* KEYBOARD.SYS (contengono informazioni relative al layout della tastiera)
* COUNTRY.SYS (queste informazioni relative a paese e codepage contengono)

## Formato file SYS ##

Microsoft ha sviluppato i file con estensione .sys. Le variabili e le funzioni sono incluse nei file SYS. Questi sono utilizzati principalmente dal sistema operativo Microsoft. Questi file si trovano principalmente nella directory principale del disco:

* C:\Windows\system32\driver
* C:\Windows\WinSxS

Alcuni avvisi comuni sui file SYS sono i seguenti:

* I nomi di questi file non devono essere modificati poiché questi file sono responsabili delle funzioni e delle variabili principali del sistema operativo
* Questi file non devono essere eliminati perché la loro assenza di questi file può causare errori
* I file .sys non devono essere scaricati da Internet finché non si è sicuri della legittimità della fonte
* Non si dovrebbero pasticciare con questi file poiché modificarli o pasticciare con questi provoca gravi errori di sistema
* Se questi file vengono danneggiati da virus o malware, è necessario reinstallarli

## Esempio SYS ##

Quello che segue è un esempio di un semplice file di configurazione del sistema SYS:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
