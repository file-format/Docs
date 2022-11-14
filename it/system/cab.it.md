{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "estensione", "file", "formato", "sistema", "File CAB Windows", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - File dell'armadio di Windows",
  "description":"Scopri il formato di file CAB e le API che possono creare e aprire file CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Che cos'è un file CAB? ##

Un file con estensione .cab appartiene a un file CAB di Windows che appartiene alla categoria dei file di sistema. È un file che viene salvato nel formato file di archivio nelle versioni di Microsoft Windows che supportano algoritmi di dati compressi, come [LZX](/it/compression/lzx/), Quantum e [ZIP](/it/compression/zip/ ). Il file è di vitale importanza quando un utente o uno sviluppatore desidera contenere e condividere dati e file di installazione del software. Le caratteristiche della compressione dei dati senza perdita di dati e la certificazione digitale inclusa in questi file rendono questo file perfetto per archiviare e condividere tali file. Supporta diversi programmi di installazione Microsoft come Device Installer, Setup API e AdvPak.

## Breve storia ##

Il file CAB è un tipo di file di compressione dei dati sviluppato da Microsoft. Inizialmente era chiamato "Diamond", ma poi divenne popolarmente noto come CAB file, abbreviazione della parola "Cabinet"

## Specifiche tecniche ##

Un file CAB può in genere contenere fino a un massimo di 65535 cartelle, che a loro volta possono contenere un massimo di 65536 file ciascuna. Il meccanismo di archiviazione dei file CAB è efficiente in termini di tempo e spazio poiché salva ogni cartella come un blocco compresso invece di comprimere e archiviare ogni file separatamente. Le cartelle vuote non possono essere archiviate nelle cartelle di archivio CAB. Il file CAB è stato sviluppato per la prima volta da Microsoft e viene utilizzato in vari programmi di installazione, come InstallShield con un formato leggermente diverso. I file CAB sono comunemente collegati a programmi autoestraenti. I file Microsoft CAB sono facilmente riconoscibili grazie al loro indicatore univoco che aiuta a identificare il formato. L'indicatore univoco per tutti i file CAB di Microsoft è un prefisso di quattro parole, MSCF. Vedendo questo codice, un utente può facilmente distinguere un file CAB Microsoft da altri file e usarlo di conseguenza nei compressori o nelle versioni. I file possono essere compressi con più dati di installazione del software, oppure i dati presenti possono essere decompressi utilizzando il software giusto.


## Esempio di cabina ##

L'esempio seguente illustra la relazione tra file e cartelle in una struttura di file CAB:

{{< figure src="../cab.png" alt="Formato file CAB" >}}

## Riferimento ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
