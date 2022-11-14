{
  "date" : "2021-08-11",
  "keywords" :["file wim", "formato file wim", "cos'è un file wim", "file", "esempio wim", "estensione file wim","estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri il formato di file WIM e le API che possono creare e aprire file WIM.",
  "title" :"WIM - File formato immagine Windows",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Che cos'è un file WIM?
I file con estensione .wim sono stati visti per la prima volta in Windows Vista. Il WIM appartiene a un formato di imaging basato su file che è stato tipicamente introdotto in Microsoft Windows Vista. Consente di distribuire una singola immagine disco su diverse piattaforme di computer. I file WIM vengono utilizzati per gestire file come aggiornamenti, driver e componenti senza riavviare l'immagine del sistema operativo. Il file AQ WIM contiene un set di file e metadati associati che è molto simile ad altri formati di file su disco.

## Formati di file WIM
Il formato di file WIM non è come i formati basati su settori come VHD o IS, infatti è un file-based, il che significa che l'unità fondamentale di informazioni in un WIM è un file. Il vantaggio di base dell'essere basato su file è che una singola istanza di archiviazione di un file referenziato più volte nell'albero del filesystem e l'indipendenza dall'hardware. Riduce il sovraccarico di apertura e chiusura di vari file singolarmente, perché i file sono archiviati all'interno di un unico WIM file. I file WIM possono memorizzare più immagini del disco, a cui viene fatto riferimento dal loro nome univoco o dal loro indice numerico.
### Supporto per algoritmi di compressione
WIM supporta le seguenti famiglie di algoritmi di compressione in velocità decrescente e rapporto crescente:
- XPRESS
- LZX
- LZMS
- Compressione solida.
Le prime tre famiglie sono basate su LZ77 mentre la compressione Solid è stata introdotta insieme a LZMS in WIMGAPI Windows 8 e DISM Windows 8.1.
### Strumenti per il formato file WIM
I seguenti strumenti di solito supportano il formato di file WIM:

- **ImageX**: uno strumento da riga di comando utilizzato per modificare, creare e distribuire immagini disco di Windows in Windows Imaging Format. Insieme alla relativa WIMGAPI, viene distribuito come parte del kit gratuito di installazione automatizzata di Windows. A partire da Windows Vista, Installazione di Windows utilizza l'API WAIK per installare Windows.
- **DISM**: uno strumento introdotto in Windows 7 e Windows Server 2008 R2 in grado di eseguire attività relative al servizio su un'immagine di installazione di Windows, sia essa un'immagine online o un'immagine offline all'interno di una cartella o di un file WIM. questo strumento era in grado di montare e smontare immagini, aggiungere un driver di dispositivo a un'immagine offline e interrogare i driver di dispositivo installati in un'immagine offline.
 




## Riferimenti


* [Formato di imaging di Windows - di Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


