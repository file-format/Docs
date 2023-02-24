{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file XFDF - Che cos'è un file XFDF?",
  "description":"Scopri il file XFDF e le API che possono creare e aprire file XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file XFDF?

Un file con estensione .xfdf è un formato dati XML Forms generato con il software Adobe Acrobat. Come [FDF](/it/pdf/fdf/), XFDF contiene la descrizione degli elementi del modulo ei relativi valori in formato XML. Questo può includere i nomi e i valori dei campi di testo nel modulo PDF. XFDF vengono salvati in un formato leggibile dall'uomo e possono essere letti in modo programmatico utilizzando linguaggi di programmazione come C#.

## Formato file XFDF - Ulteriori informazioni

I file XFDF vengono salvati in formato file XML che è un formato universale utilizzato per l'importazione e l'esportazione di dati. Una struttura di file XFDF è costituita da un'intestazione, seguita da valori di campo e dati di elementi come mostrato di seguito.

|Elemento|Attributo|Contenuto|
---|---|---|
|\<XFDF> ||Elemento più in alto|
|\<fields> ||Tutti i valori dei campi per questo modello|
|<field (T)> |nome |Nome campo|
|<value (V)> |valore |Valore campo|

## Riferimenti

* [Supporto del formato FDF di Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Risorse per sviluppatori Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

