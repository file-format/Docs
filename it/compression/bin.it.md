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
"title": "Formato file BIN - File codificato MacBinary",
   "description":"Informazioni sul formato BIN e sulle API in grado di creare e aprire file BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
"parent" : "compression"
}
},
"lastmod":"20/07/2023"
}

## Cos'è un file BIN?

Un file BIN, nel contesto dei computer Macintosh, può fare riferimento a un file salvato nel formato MacBinary. MacBinary è un formato di file progettato specificamente per il trasferimento di file Macintosh su Internet, e-mail, FTP o supporti portatili. Lo scopo di MacBinary è preservare la struttura completa dei file e gli attributi dei file Macintosh, inclusi sia il fork dei dati che il fork delle risorse, all'interno di un singolo file.

Il formato MacBinary ottiene questo risultato incapsulando il fork delle risorse e il fork dei dati del Macintosh Hierarchical File System (HFS) in un file compresso. Include anche un'intestazione del Finder che contiene metadati importanti sul file. Combinando tutti questi componenti in un unico file, MacBinary garantisce che il file mantenga la sua integrità e possa essere facilmente trasferito e condiviso su diverse piattaforme.

Con i progressi nei file system e nei protocolli di trasferimento file di Apple, l'uso dei file BIN e del formato MacBinary è diventato meno comune. L'introduzione di formati di file come ZIP e il passaggio a file system più moderni, come HFS+ e APFS, hanno ridotto la necessità di file codificati con MacBinary. Questi file system più recenti forniscono modi più efficienti di gestire attributi di file, fork di risorse e fork di dati, rendendo il formato MacBinary meno necessario nel panorama informatico odierno.

## Formato file BIN: ulteriori informazioni

Agli albori dei computer Macintosh, i file venivano archiviati in due "fork" separati a causa delle limitazioni dei dati. Il "fork delle risorse" conteneva dati strutturati, mentre il "fork dei dati" conteneva dati non strutturati. Mentre il sistema operativo Mac classico trattava questi fork come un singolo file, il trasferimento di file su sistemi non Mac comportava una perdita di dati perché non riconoscevano i fork come una singola entità. Per risolvere questo problema, il formato MacBinary è stato creato da individui come Dennis Brothers, Harry Chesley e Yves Lempereur. MacBinary ha compresso e combinato i fork in un unico file, noto come file BIN, per il trasferimento su sistemi non Mac. Al ritorno al sistema operativo Mac, le forcelle verrebbero nuovamente separate. Con l'abbandono dell'HFS basato su fork negli anni 2000, l'uso del formato MacBinary è diminuito in modo significativo. Oggi, incontrare un file BIN con codifica MacBinary è raro a meno che non ti imbatti in un vecchio file su un sistema non Mac o ne scarichi uno da Internet.

Il formato MacBinary ha attraversato diverse versioni nel tempo per adattarsi ai cambiamenti nei sistemi Macintosh e nella gestione dei file. Ecco alcune delle diverse versioni del formato MacBinary:

- **MacBinary I:** la versione iniziale di MacBinary, introdotta alla fine degli anni '80. Combinava il fork delle risorse e il fork dei dati in un unico file binario, consentendo il trasferimento multipiattaforma di file Macintosh.

- **MacBinary II:** questa versione, rilasciata all'inizio degli anni '90, ha migliorato il formato MacBinary originale aggiungendo ulteriori informazioni, come il tipo di file e i codici dell'autore, all'intestazione del file binario. Questi codici hanno contribuito a mantenere l'integrità e l'identificazione dei file Macintosh durante il trasferimento.

- **MacBinary III:** il formato MacBinary III, introdotto a metà degli anni '90, ha ulteriormente migliorato le versioni precedenti includendo metadati aggiuntivi, come il nome del file e le date di creazione e modifica del file, nell'intestazione del file binario. Ciò ha consentito una conservazione più completa degli attributi dei file Macintosh durante il trasferimento.

- **MacBinary IV:** MacBinary IV è stato sviluppato per risolvere problemi di compatibilità con il sistema operativo emergente Mac OS X nei primi anni 2000. Incorporava modifiche per adattarsi alla nuova struttura e agli attributi del file system introdotti in Mac OS X.

## Come aprire un file BIN?

I file BIN codificati MacBinary possono essere aperti utilizzando varie utilità di compressione. Per gli utenti macOS, l'**Apple Archive Utility** è un'opzione adatta. Gli utenti Windows possono utilizzare software come **Smith Micro StuffIt Deluxe** per estrarre il contenuto di un file BIN codificato MacBinary. Un'altra opzione per gli utenti macOS è **The Unarchiver**, uno strumento versatile in grado di gestire più formati di file, incluso MacBinary.

È importante notare che l'estensione del file .bin viene utilizzata da vari formati di file, non solo da MacBinary. Pertanto, se trovi un file BIN che non può essere aperto con le utilità sopra menzionate, potrebbe essere salvato in un formato diverso. In questi casi, potrebbe essere necessario identificare il formato file specifico e utilizzare il software o l'utilità appropriata progettata per quel formato per accedere ai contenuti del file.

## Altri file BIN

Di seguito sono riportati altri tipi di file che utilizzano l'estensione file **.bin**.

- [BIN - File immagine disco binario](/it/disc-and-media/bin/)
- [BIN - File eseguibile Unix](/it/executable/bin/)
- [BIN - File dei criteri IT BlackBerry](/it/settings/bin/)
- [BIN - ROM del gioco Sega Genesis](/it/game/bin/)
- [BIN - Immagine BIOS PlayStation PSX](/it/game/bin-pcsx/)

## Riferimenti

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

