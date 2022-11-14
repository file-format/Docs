{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "estensione", "file sav", "formato file sav", "Tipo file database", "Formato file database", "che cos'è un file sav"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file SAV e le API che possono creare e aprire file SAV.",
  "title" :"SAV - File di dati SPSS",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Che cos'è un file SAV?
Il file SAV è un file di dati creato dal Pacchetto statistico per le scienze sociali (SPSS), che è un'applicazione ampiamente utilizzata da ricercatori di mercato, ricercatori sanitari, società di sondaggi, governo, ricercatori dell'istruzione, organizzazioni di marketing, minatori di dati per l'analisi statistica. Il SAV salvato in un formato binario proprietario ed è costituito da un set di dati e da un dizionario che rappresentano il set di dati, salva i dati in righe e colonne.

## Formato file SAV
Il formato del file SAV è diventato relativamente stabile, ma non possiamo dirlo statico. La compatibilità con le versioni precedenti e successive è disponibile opzionalmente ove necessario, ma non viene mantenuta correttamente. I dati in un file SAV sono classificati nelle seguenti sezioni:

### Intestazione del file
Consiste di 176 byte. I primi 4 byte indicano la stringa **$FL2** o **$FL3** nella codifica dei caratteri utilizzata per il file. Gli ultimi tre byte rappresentano che i dati nel file vengono compressi utilizzando **ZLIB**. La successiva stringa di 60 byte inizia **@(#) SPSS DATA FILE** e determina anche il sistema operativo e la versione SPSS che ha creato il file. L'intestazione continua quindi con campi a sei cifre, contenenti il numero di variabili per osservazione e un codice cifra per la compressione, e termina con i dati dei caratteri che indicano la data e l'ora di creazione e un'etichetta del file.
### Record del descrittore di variabili
Il record contiene una sequenza fissa di campi, classificando il tipo e il nome della variabile insieme alle informazioni di formattazione utilizzate da SPSS. Ogni record di variabile può contenere facoltativamente un'etichetta di variabile fino a 120 caratteri e fino a tre specifiche di valori mancanti.
### Etichette di valore
Le etichette dei valori sono facoltative e memorizzate in coppie di record con tag interi 3 e 4. Il primo record che è il tag 3 ha una sequenza di coppie di campi, ciascuna coppia contenente un valore e l'etichetta del valore associata. Il secondo record che è il tag 4, rappresenta a quali variabili si applica l'insieme di valori/etichette.
### Documenti
Record singoli o multipli con tag intero 6. Documentazione opzionale. contiene righe di 80 caratteri.
### Record di estensioni
Record singoli o multipli con tag intero 7. I record di estensione forniscono informazioni che possono essere ignorate in modo sicuro, ma conservate, in molte situazioni, consente ai file scritti da software più recenti di preservare la compatibilità con le versioni precedenti. I record di estensione hanno tag di sottotipo interi.
### Terminatore del dizionario
Registra solo con tag intero 999. Separa il dizionario dalle osservazioni dei dati.
### Osservazioni dei dati
Viene considerato come i dati sono in ordine di osservazione, ad es. tutti i valori variabili per la prima osservazione, seguiti da tutti i valori per la seconda osservazione, ecc. Il formato del record di dati varia a seconda del codice di compressione nel record di intestazione del file. La parte di dati di un file .sav può essere decompressa:
- **codice 0**: compresso da bytecode
- **codice 1**: compresso utilizzando la compressione ZLIB
 







## Riferimenti ##

* [Famiglia di formati file di dati di sistema SPSS (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

