{
"data":"20/07/2023",
   "keywords":[
"BIDONE",
"File BIN",
"file",
"Estensione file BIN",
"estensione",
"file"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file BIN - File eseguibile Unix",
   "description":"Informazioni sul formato BIN e sulle API in grado di creare e aprire file BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
"parent" : "executable"
}
},
"lastmod":"20/07/2023"
}

## Cos'è un file BIN?

Un file BIN è un file eseguibile su sistemi operativi basati su Unix come Linux o FreeBSD. Contiene un programma compilato composto da codice binario derivato dal codice sorgente, rendendolo compatibile con l'architettura del sistema sottostante. I file BIN eseguibili Unix possono essere paragonati ai file .EXE di Windows e ai file .APP di macOS in termini di ruolo di formati eseguibili.

Nel campo dello sviluppo software per sistemi Unix, i file BIN vengono comunemente utilizzati dagli sviluppatori per confezionare e distribuire programmi. Offrono un mezzo conveniente per fornire software agli utenti, consentendo una facile installazione ed esecuzione. Oltre ai file BIN, esistono altri tipi di eseguibili Unix, tra cui [.ELF](/it/executable/elf/), .X86, [.RUN](/it/executable/run/) e .X86_64, ciascuno personalizzato per hardware specifico o requisiti di sistema.

Quando si tratta della struttura interna di un file BIN, è costituito da dati codificati che il sistema operativo Unix utilizza per identificare, leggere ed eseguire il programma allegato. Il sistema si basa su firme o intestazioni di file specifiche per riconoscere il file BIN come eseguibile, seguite dall'interpretazione ed esecuzione delle istruzioni binarie contenute al suo interno.

I file BIN vengono spesso forniti in bundle con un file **INSTALL.TXT** di accompagnamento, che fornisce istruzioni dettagliate su come installare e configurare correttamente il programma. Questa documentazione garantisce che gli utenti possano affrontare con successo il processo di installazione e iniziare a utilizzare il software senza complicazioni.

## Come aprire il file BIN?

I file BIN non sono progettati per essere aperti e visualizzati direttamente. Tuttavia è possibile eseguire i programmi o estrarre i dati in essi contenuti. Per accedere al contenuto di un file BIN, seguire questi passaggi sulla riga di comando, presupponendo che il nome del file BIN sia "sample.bin":

1. **Garantire le autorizzazioni eseguibili:**

Prima di eseguire il file BIN, assicurati che disponga delle autorizzazioni necessarie per essere eseguito come eseguibile. Utilizza il comando:

```
$ chmod +x sample.bin
```

Questo comando concede i privilegi di file eseguibile.

2. **Esegui il file BIN:**

Dopo aver impostato le autorizzazioni dell'eseguibile, è possibile eseguire il file BIN immettendo il seguente comando:

```
$ ./sample.bin
```

**Avvertimento**

_Prestare attenzione quando si ha a che fare con file BIN scaricati o inviati tramite posta elettronica, poiché possono essere potenzialmente utilizzati dai criminali informatici per distribuire malware. Esegui solo file BIN provenienti da fonti attendibili per mitigare il rischio di attacchi eseguibili dannosi._

## Altri file BIN

Di seguito sono riportati altri tipi di file che utilizzano l'estensione file **.bin**.

- [BIN - File codificato MacBinary](/it/compression/bin/)
- [BIN - File immagine disco binario](/it/disc-and-media/bin/)
- [BIN - File dei criteri IT BlackBerry](/it/settings/bin/)
- [BIN - ROM del gioco Sega Genesis](/it/gioco/bin/)
- [BIN - Immagine BIOS PlayStation PSX](/it/game/bin-pcsx/)

## Riferimenti

* [Come eseguire file binari in Linux](https://linuxhint.com/execute-binary-files-in-linux/)


