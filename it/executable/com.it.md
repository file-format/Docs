{
  "date" : "2021-06-29",
  "keywords" :[ "file com", "che cos'è un file com", "file", "esempio com", "estensione file com", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file COM e le API che possono creare e aprire file COM.",
  "title" :"COM - Formato file di comando DOS",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Che cos'è un file COM?
I file COM vengono utilizzati semplicemente per eseguire una serie di comandi o istruzioni. Un file COM è costituito da un programma eseguibile che può essere eseguito da Windows o MS-DOS. Allo stesso modo un file EXE, anche il file COM viene salvato in formato binario ma è diverso dal file EXE perché non ha intestazione o metadati e inoltre ha una dimensione massima di 64 KB circa. Quando il file COM viene eseguito per la prima volta su un sistema a 32 bit, viene richiesto di installare il componente NT Virtual DOS Machine (NTVDM). Il file COM può essere eseguito nella versione a 64 bit di Microsoft Windows con una macchina virtuale che supporta l'ambiente MS-DOS.

## Formato file COM
Il formato di file COM è un formato eseguibile binario utilizzato in Microsoft Windows o MS-DOS. La sua struttura consiste solo in un insieme di istruzioni; non ha intestazione e non contiene metadati standard. Memorizza tutti i suoi dati e codice in un solo segmento e il suo binario ha una dimensione massima di 64 KB. Questo formato di file non si sposta da solo quando si tenta di rieseguirlo. Quindi il sistema operativo lo carica a un indirizzo preimpostato. Inoltre, è possibile creare un file COM da eseguire con entrambi i sistemi operativi sotto forma di **fat binary**. Non c'è alcuna compatibilità effettiva a livello di istruzione. Le istruzioni al punto di ingresso sono selezionate per essere uguali in termini di funzionalità ma diverse in entrambi i sistemi operativi e fanno in modo che il programma sia in esecuzione, saltano alla sezione del sistema operativo in uso. Si tratta sostanzialmente di due programmi diversi con la stessa procedura in un unico file, preceduti dal codice che seleziona quello da utilizzare.
### Esempio di file COM
Quando si esegue un file COM, le istruzioni vengono lette dal primo byte e seguite consecutivamente fino a trovare le ultime istruzioni. Ecco un esempio di codice ASM:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Riferimenti

* [File COM - di Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

