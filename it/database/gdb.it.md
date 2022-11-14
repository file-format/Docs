{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file GDB - File geodatabase file ESRI",
  "description":"Scopri il formato di file GDB e le API che possono creare e aprire file GDB.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Che cos'è un file GDB?

Il file ESRI Geodatabase (FileGDB) è una raccolta di file in una cartella su disco che contengono dati geospaziali correlati come set di dati di funzionalità, classi di funzionalità e tabelle associate. Per funzionare, richiede che alcuni altri file siano conservati insieme al file .gdb nella stessa directory. Le query possono essere eseguite sul file .gdb per gestire dati spaziali e non spaziali.

## Formato file GDB - Ulteriori informazioni

I geodatabase di file sono costituiti da sette tabelle di sistema più i dati utente. I dati dell'utente possono essere memorizzati nei seguenti tipi di set di dati:

* Classe caratteristica
* Set di dati sulle funzionalità
* Set di dati Mosaico
* Catalogo raster
* Set di dati raster
* Set di dati schematico
* Tabella (non spaziale)
* Cassette degli attrezzi

I set di dati di funzionalità possono contenere classi di funzionalità nonché i seguenti tipi di set di dati:

* Allegati
* Annotazione collegata a funzionalità
* Reti geometriche
* Set di dati di rete
* Tessuti per pacchi
* Classi di relazione
* Terreni
* Topologie

La dimensione massima predefinita dei set di dati nei geodatabase di file è 1 TB. La dimensione massima può essere aumentata a 256 TB per set di dati di grandi dimensioni (solitamente raster). Questo è controllato da una parola chiave di configurazione. Per ulteriori informazioni, vedere Parole chiave di configurazione per i geodatabase di file.

I geodatabase di file possono anche contenere sottotipi e domini e partecipare alla replica di check-out/check-in e alle repliche unidirezionali.

Un geodatabase di file è accessibile contemporaneamente da più utenti. Se gli utenti stanno modificando, devono modificare set di dati diversi.

## Specifiche del formato file GDB ##

Il file GDB è un formato proprietario ESRI e le sue specifiche non sono disponibili pubblicamente. Per questo motivo, i dettagli del formato file per FIle GDB non possono essere documentati da nessuna parte se non da alcune fonti che lo hanno fatto [parzialmente](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) mediante reverse engineering .

## Riferimenti ##

* [Specifiche FGDB](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

