{
  "date" : "2021-06-30",
  "keywords" :[ "file exe", "formato file exe", "cos'è un file exe", "file", "esempio exe", "estensione file exe", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Un file .exe è un file eseguibile Microsoft eseguito su sistema operativo Windows. Ulteriori informazioni sul formato di file EXE.",
  "title" :"Cos'è un file EXE eseguibile?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Che cos'è un file EXE?

La parola EXE è l'abbreviazione di **eseguibile**. Un file .exe è un programma che può essere eseguito sul sistema operativo Microsoft Windows. Gli sviluppatori di applicazioni pubblicano principalmente i loro programmi per il sistema operativo Windows in formato eseguibile come file exe. È il formato di file standard per eseguire applicazioni su Windows. **Setup.exe**, **Install.exe** e **cmd.exe** sono alcuni nomi comuni e familiari di file EXE.

## Formato file EXE

I compilatori MS-DOS sono stati introdotti con i modelli di memoria con il limite di memoria di 64 KB. Il concetto generale è quello di impostare diversi registri di segmento nella CPU x86 (CS, DS, ES, SS) in modo che puntino a segmenti diversi o uguali, consentendo quindi vari gradi di accesso alla memoria. Alcuni modelli di memoria specifici erano:

- **Tiny**: tutti gli accessi alla memoria sono a 16 bit (registri di segmento invariati). Produce un file .COM invece di un file .EXE.
- **Piccolo**: tutti gli accessi alla memoria sono a 16 bit (registri di segmento invariati).
- **Compatto**: gli indirizzi dati includono sia il segmento che l'offset, ricaricando i registri DS o ES all'accesso e consentendo fino a 1M di dati. Gli accessi al codice non modificano il registro CS, consentendo 64K di codice.
- **Medio**: gli indirizzi di codice includono l'indirizzo del segmento, ricaricando CS all'accesso e consentendo fino a 1M di codice. Gli accessi ai dati non modificano i registri DS ed ES, consentendo 64K di dati.
- **Grande**: sia il codice che gli indirizzi dati sono coppie (segmento, offset), ricaricando sempre gli indirizzi del segmento. L'intero spazio di memoria di 1M byte è disponibile sia per il codice che per i dati.
- **Enorme**: come il modello grande, con aritmetica aggiuntiva generata dal compilatore per consentire l'accesso a matrici di dimensioni superiori a 64 KB.

Gli sviluppatori devono decidere quale modello deve essere selezionato durante la creazione di un file exe.

### Formato file EXE portatile

Il formato di file eseguibile portatile (PE) contiene una serie di intestazioni informative, di seguito è riportato l'elenco delle intestazioni:

- **intestazione DOS**: l'intestazione MS-DOS garantisce la compatibilità con le versioni precedenti o il declino regolare di nuovi tipi di file.
- **PE Header**: All'offset 60 (0x3C) dall'inizio dell'intestazione DOS c'è un puntatore all'intestazione del file PE
- **COFF Header**: l'intestazione COFF contiene alcune informazioni utili per un eseguibile e alcune informazioni che sono più utili per un file oggetto.
- **Intestazione opzionale PE**: l'intestazione opzionale PE si trova direttamente dopo l'intestazione COFF e alcune fonti mostrano addirittura che le due intestazioni fanno parte della stessa struttura.
- **Tabella delle sezioni**: subito dopo l'intestazione opzionale PE troviamo una tabella delle sezioni. La tabella delle sezioni è costituita da un array di strutture IMAGE_SECTION_HEADER.
- **Sezioni mappabili**: consente di risparmiare spazio in memoria mappando il codice di una libreria in più di un processo.

## Puoi eseguire un file EXE su un Mac?

I file exe non vengono utilizzati come eseguibili su Mac OS. Tuttavia, se desideri eseguire un file exe su Mac OS, è possibile utilizzare i seguenti metodi.

1. **Wine** - Wine è la soluzione perfetta per le persone che desiderano utilizzare le proprie applicazioni per PC su sistemi Mac. È un acronimo che sta per "Wine Is Not A Emulator", che significa. Wine crea lo stesso ambiente di directory utilizzato da Microsoft in modo da poter eseguire la tua applicazione Windows utilizzandolo.
2. **Macchine virtuali**: crea una macchina virtuale Windows utilizzando Parallel Desktop o VM Virtual Box ed esegui l'applicazione all'interno della macchina virtuale.
3. **Boot Camp**: l'installazione e la configurazione di Windows Boot Camp su Mac OS ti consente di eseguire il sistema operativo Windows su computer Mac.

## Riferimenti

* [.exe- di Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [Disassembly x86/File eseguibili di Windows](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

