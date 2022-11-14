{
  "date" : "2021-07-12",
  "keywords" :[ "file cmd", "che cos'è un file cmd", "file", "esempio cmd", "estensione file cmd", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file CMD e le API che possono creare e aprire file CMD.",
  "title" :"CMD - Formato file di comando di Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Che cos'è un file CMD?
Un file CMD è costituito da uno script contenente uno o più comandi sotto forma di testo normale che vengono eseguiti per eseguire varie attività. È simile a un file [BAT](/it/executable/bat/), che viene generalmente utilizzato anche per memorizzare un batch di comandi eseguibili. I file CMD sono ampiamente utilizzati nel sistema operativo Microsoft Windows. Questi file sono stati introdotti quasi negli anni '90 ma sono ancora utilizzati nell'ultimo sistema operativo Windows. Questi file sono generalmente scritti per eseguire più di un comando in una sequenza.

## Formato file CMD
CMD è un formato di file utilizzato dai programmi eseguibili in stile CP/M. È generalmente paragonabile a [COM](/it/executable/com/) in CP/M-80 e [EXE](/it/executable/exe/) in DOS. Un file CMD contiene da 1 a 8 gruppi di codice o dati e un'intestazione di 128 byte. Ogni gruppo può avere una dimensione massima di 1 MB. I file CMD possono anche contenere informazioni sul trasferimento e le estensioni del sistema residente (RSX) nelle versioni successive. Il CMD è un nuovo arrivato rispetto al file [BAT](/it/executable/bat/); utilizzato per MS-DOS prima del rilascio di Windows In MS-DOS. Sebbene sia ancora possibile salvare i file con l'estensione .bat oggi, molte persone usano l'estensione .cmd per salvare i propri script eseguibili.

### Specifica del formato CMD

L'inizio dell'intestazione contiene l'elenco dei gruppi presenti nel file con le relative tipologie. Ciascun tipo può essere utilizzato al massimo una volta. Questi tipi sono:

- Codice
- Dati
- Extra
- Pila
- Utente 1
- Utente 2
- Utente 3
- Utente 4
- Codice condiviso

Allo stesso modo Program Segment Prefix in DOS, i primi 256 byte del gruppo di dati sono zero. Saranno popolati da CP/M-86 con la pagina zero. Se non è presente alcun gruppo di dati, verranno invece utilizzati i primi 256 byte del gruppo di codice.
## Esempio di file CMD
Di seguito è riportato un esempio di script CMD per mostrare le informazioni sui sistemi.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Riferimenti

* [Come scrivere uno script CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [File CMD (CP/M) - di Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

