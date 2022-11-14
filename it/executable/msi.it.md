{
  "date" : "2021-06-30",
  "keywords" :[ "file msi", "formato file MSI", "cos'è un file msi", "file", "esempio msi", "estensione file msi", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file MSI e le API che possono creare e aprire file MSI.",
  "title" :"MSI - File del pacchetto di Windows Installer",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Che cos'è un file MSI?
Un file MSI utilizzato per installare e avviare programmi Windows; un pacchetto completo per Microsoft Windows che contiene le informazioni sull'installazione di un tipico programma software, inclusi i file essenziali da installare e le informazioni sul percorso di installazione. I file MSI possono contenere anche il pacchetto per gli aggiornamenti software. I file MSI sono simili a [EXE](/it/executable/exe/), ma a volte EXE potrebbe non includere le informazioni sul programma di installazione e il programma software potrebbe essere eseguito direttamente quando si esegue il file EXE.

## Formato file MSI
Windows Installer è in realtà un'API (Application Programming Interface) e un componente software di Microsoft Windows utilizzato per l'installazione, la rimozione e la manutenzione di un programma software. Le informazioni sull'installazione ei file facoltativi sono impacchettati come pacchetti di installazione e database liberamente relazionali strutturati come COM Structured Storage; noto come **file MSI**, con estensione di file .msi. I pacchetti con estensione di file **.mst** contengono **Transformation Scripts** di Windows Installer, i file con estensione **.msm** contengono **Unisci moduli** e l'estensione di file **.pcp** viene utilizzato per **Proprietà di creazione patch**. Windows Installer diventa più avanzato dopo aver apportato modifiche significative rispetto alle versioni precedenti, l'API di installazione. Un framework GUI e la generazione automatica della sequenza di disinstallazione sono le nuove funzionalità di Windows Installer. È stato considerato ora come un'alternativa ai framework di installazione eseguibili autonomi.

### Struttura logica dei pacchetti MSI
Un pacchetto indica l'installazione di uno o più prodotti completi ed è generalmente identificato da un **GUID**. Un prodotto è costituito da uno o più componenti e raggruppato in varie funzioni. Windows Installer non gestisce le dipendenze tra vari prodotti contemporaneamente. La struttura logica dei pacchetti è composta dai seguenti elementi:

- **Prodotti**: un singolo programma di lavoro installato o un insieme di più programmi combinati insieme costituisce un prodotto. Un prodotto è identificato da un GUID univoco.
- **Caratteristiche**: può contenere un numero qualsiasi di componenti e altre sottocaratteristiche. I pacchetti più piccoli possono essere costituiti da una singola funzionalità.
- **Componenti**: il componente viene trattato da Windows Installer come un'unità; può contenere file di programma, cartelle, chiavi di registro, componenti COM e collegamenti.
- **Percorsi chiave**: un percorso chiave è un file specifico, un'origine dati ODBC o una chiave di registro che l'autore del pacchetto specifica come critico per un determinato componente.

## Riferimenti

* [Windows Installer - di Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


