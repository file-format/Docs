{
  "date" : "2021-06-24",
  "keywords" :[ "file bat", "che cos'è un file bat", "file", "esempio di file bat", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file BAT e le API che possono creare e aprire file BAT.",
  "title" :"BAT - Formato file batch",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Che cos'è un file BAT?
Un file BAT è noto come file batch viene eseguito con DOS e tutte le versioni di Windows, in cmd.exe. Consiste in una serie di comandi di riga in testo normale che devono essere eseguiti dall'interprete della riga di comando per eseguire diverse attività, come l'esecuzione di utilità di manutenzione all'interno di Windows o l'avvio di programmi tipici. Un file batch può includere qualsiasi comando che può essere accettato dall'interprete in modo interattivo e utilizzare la struttura del codice che abilita il branching condizionale e il loop come scritto all'interno del file batch.
## Formato file BAT
Un formato di file BAT è semplicemente uno script incorporato per automatizzare sequenze di comandi che sono di natura ripetitive. Il termine "batch" viene utilizzato per l'elaborazione batch, può essere considerato come "esecuzione non interattiva". Pertanto un file batch potrebbe non elaborare un batch di più dati. Nel vecchio sistema operativo su disco (DOS), il file batch veniva eseguito sotto l'interfaccia della riga di comando digitando il nome del file e l'estensione .bat. Il precedente sistema operativo basato sull'interfaccia grafica Microsoft come Microsoft Windows dipendeva da DOS. Gli utenti dovevano utilizzare DOS per eseguire operazioni tipiche come riparare, ottimizzare o reinstallare Windows. Successivamente Microsoft ha introdotto Windows NT che non dipendeva dal sistema operativo DOS. Pertanto, i file batch possono essere eseguiti utilizzando il prompt dei comandi o **cmd.exe** nei moderni sistemi operativi Microsoft.
### Parametri del file batch
Il prompt dei comandi supporta una serie di variabili speciali come **%0, da %1 a %9** per fare riferimento al nome e al percorso del lavoro batch e ai nove parametri chiamanti dall'interno del lavoro batch. I parametri inesistenti vengono sostituiti da una stringa di lunghezza zero. Tuttavia, possono essere utilizzati in modo simile alle variabili di ambiente, ma non vengono salvati nell'ambiente. Microsoft e IBM si riferiscono a queste variabili come parametri di sostituzione, mentre Novell, Digital Research e Caldera hanno introdotto per esse il termine variabili di sostituzione.

Ecco alcuni utili comandi per i file batch:
| Comando | Descrizione |
------|------------|
| VER | Questo comando batch mostra la versione di MS-DOS in uso. |
|ASSOC| Questo è un comando batch che associa un'estensione a un tipo di file (FTYPE), visualizza le associazioni esistenti o elimina un'associazione. |
|CD| Questo comando batch aiuta ad apportare modifiche a una directory diversa o visualizza la directory corrente. |
|CLS| Questo comando batch cancella lo schermo. |
|COPIA| Questo comando batch viene utilizzato per copiare i file da una posizione all'altra. |
|CANC| Questo comando batch elimina i file e non le directory. |
|DIR| Questo comando batch elenca il contenuto di una directory. |
|DATA| Questo comando batch aiuta a trovare la data di sistema. |
|ECO| Questo comando batch visualizza i messaggi o attiva o disattiva l'eco dei comandi. |
|ESCI| Questo comando batch esce dalla console DOS. |
|MD| Questo comando batch crea una nuova directory nella posizione corrente. |
|SPOSTA| Questo comando batch sposta file o directory tra directory. |
|PERCORSO| Questo comando batch visualizza o imposta la variabile di percorso. |
|PAUSA| Questo comando batch richiede all'utente e attende l'immissione di una riga di input. |
|RICHIESTA| Questo comando batch può essere utilizzato per modificare o reimpostare il prompt di cmd.exe. |
|RD| Questo comando batch rimuove le directory, ma le directory devono essere vuote prima di poter essere rimosse. |
|REN| Rinomina file e directory |
|REM| Questo comando batch viene utilizzato per i commenti nei file batch, impedendo l'esecuzione del contenuto del commento. |
|INIZIO| Questo comando batch avvia un programma in una nuova finestra o apre un documento. |
|TEMPO| Questo comando batch imposta o visualizza l'ora. |
|TIPO| Questo comando batch stampa il contenuto di uno o più file nell'output. |
|VOL| Questo comando batch visualizza le etichette del volume. |
|ATTRIB| Visualizza o imposta gli attributi dei file nella directory curret |
|CHKDSK| Questo comando batch controlla il disco per eventuali problemi. |
|SCELTA| Questo comando batch fornisce un elenco di opzioni all'utente. |
|CMD| Questo comando batch richiama un'altra istanza del prompt dei comandi. |
|COMP| Questo comando batch confronta 2 file in base alla dimensione del file. |
|CONVERTI| Questo comando batch converte un volume dal file system FAT16 o FAT32 al file system NTFS. |
|QUERY DRIVER| Questo comando batch mostra tutti i driver di dispositivo installati e le relative proprietà. |
|Espandi| Questo comando batch estrae i file dai file CAB compressi. |
|TROVA| Questo comando batch cerca una stringa nei file o nell'input, generando righe corrispondenti. |
|FORMATO| Questo comando batch formatta un disco per utilizzare il file system supportato da Windows come FAT, FAT32 o NTFS, sovrascrivendo così il contenuto precedente del disco. |
|AIUTO| Questo comando batch mostra l'elenco dei comandi forniti da Windows. |
|CONFIG.IP| Questo comando batch visualizza la configurazione IP di Windows. Mostra la configurazione per connessione e il nome di quella connessione. |
|ETICHETTA| Questo comando batch aggiunge, imposta o rimuove un'etichetta del disco. |
|ALTRO| Questo comando batch visualizza il contenuto di uno o più file, una schermata alla volta. |
|RETE| Fornisce vari servizi di rete, a seconda del comando utilizzato. |
|PING| Questo comando batch invia pacchetti ICMP/IP "eco" sulla rete all'indirizzo designato. |
|SPEGNIMENTO| Questo comando batch spegne un computer o disconnette l'utente corrente. |
|ORDINA| Questo comando batch prende l'input da un file sorgente e ne ordina il contenuto in ordine alfabetico, dalla A alla Z o dalla Z alla A. Stampa l'output sulla console. |
|SUBST| Questo comando batch assegna una lettera di unità a una cartella locale, visualizza le assegnazioni correnti o rimuove un'assegnazione. |
|SISTEMA| Questo comando batch mostra la configurazione di un computer e del relativo sistema operativo. |
|TASKKILL| Questo comando batch termina una o più attività. |
|ELENCO ATTIVITA'| Questo comando batch elenca le attività, inclusi il nome dell'attività e l'ID processo (PID). |
|XCOPIA| Questo comando batch copia file e directory in un modo più avanzato. |
|ALBERO| Questo comando batch visualizza un albero di tutte le sottodirectory della directory corrente a qualsiasi livello di ricorsione o profondità. |
|FC |Questo comando batch elenca le differenze effettive tra due file. |
|DISKPART |Questo comando batch mostra e configura le proprietà delle partizioni del disco. |
|TITLE |Questo comando batch imposta il titolo visualizzato nella finestra della console. |
|IMPOSTA | Visualizza l'elenco delle variabili di ambiente nel sistema corrente. |

## Esempio di file BAT
Gli script batch vengono generalmente salvati come semplici file di testo; contenente comandi che vengono eseguiti in una sequenza. Questi file vengono salvati con estensione .bat; riconosciuto ed eseguito utilizzando il software **Command Interpreter**. Questo software è nativamente disponibile in Microsoft Windows con il nome **cmd.exe**.

Ecco uno script batch di esempio che elimina tutti i file nella directory corrente:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Riferimenti

* [Script batch - Guida rapida](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [File batch - di Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

