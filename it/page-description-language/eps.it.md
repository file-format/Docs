{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "file", "estensione", "formato file", "Layout di pagina", "PostScript incapsulato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file EPS e le API che possono creare e aprire file EPS.",
  "title" :"Formato file EPS - File PostScript incapsulato",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file EPS?

Un file .eps è un file immagine che viene salvato su disco in formato Encapsulated Postscript. Può contenere qualsiasi combinazione di testo, grafica e immagini. I file EPS possono anche includere un'immagine di anteprima bitmap incapsulata all'interno per la visualizzazione da parte di applicazioni in grado di aprire tali file.

## Breve storia del formato di file EPS

Una rapida occhiata al formato di file EPS dal punto di vista della cronologia rivela le seguenti informazioni:

* La prima versione di EPS è stata rilasciata da Adobe tra il 1985 e il 1988
* La versione 2.0 della specifica EPS è stata pubblicata nel gennaio 1989
* La specifica per la versione 3.0 di EPS è stata pubblicata come documento separato nel 1992; questa è l'ultima versione pubblicata.

EPS, in combinazione con il meccanismo di estensione Open Structuring Conventions descritto nella clausola 9 della specifica di Adobe PostScript Language Document Structuring Conventions, ha costituito la base delle prime versioni del formato di file Adobe Illustrator Artwork.

## Formato file EPS

EPS è un formato proprietario ma pubblicamente documentato e le specifiche del formato di file EPS sono disponibili pubblicamente per riferimento dello sviluppatore. EPS è un formato di file conforme alla [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) e aderisce a tutte le regole stabilite dalla DSC. Il DSC è un formato di file speciale per i documenti PostScript di Adobe. Qualsiasi applicazione che afferma di essere in grado di leggere file EPS deve essere conforme a DSC.

Un file EPS è costituito da due sezioni principali come spiegato di seguito.

### Anteprima immagine ###

Un tipico file EPS contiene un'immagine di anteprima in un formato concepito per un comodo utilizzo in un flusso di lavoro che coinvolge diversi sistemi o applicazioni. L'intento di un'anteprima è quello di avere un'immagine in un formato che la maggior parte delle applicazioni grafiche può renderizzare; un'anteprima è solitamente di risoluzione inferiore, in dimensioni in pixel e/o in profondità di bit. Il file di anteprima può essere in uno di numerosi formati. La specifica per EPS_3 elenca tre formati di anteprima "specifici del dispositivo":

* per Apple Macintosh, un'immagine PICT utilizzata dall'applicazione QuickDraw
* per i computer DOS, una bitmap TIFF
* Metafile di Windows.

PICT e Windows Metafile possono incorporare sia dati bitmap che grafica vettoriale. Inoltre, la specifica definisce una rappresentazione indipendente dal dispositivo molto semplice per un'immagine di anteprima bitmap incorporata. Questa rappresentazione è nota come Encapsulated PostScript Interchange Format (EPSI).

Un'anteprima EPSI è una bitmap rappresentata come esadecimale ASCII, racchiusa tra alcuni commenti PostScript per l'identificazione e pensata per essere semplice e facilmente trasportabile. Per distinguere i file EPS con i diversi formati di anteprima, nella specifica EPS sono state consigliate diverse estensioni di file DOS e tipi di file Macintosh.

### Codice PostScript

Come minimo, il formato del file EPS deve includere quanto segue:

* un commento sull'intestazione, %!PS-Adobe-3.0 EPSF-3.0
* e un commento del riquadro di delimitazione, %%BoundingBox: llx lly urx ury, che descrive i limiti dell'illustrazione. Questi quattro argomenti corrispondono agli angoli inferiore sinistro (llx, lly) e superiore destro (urx, ury) del riquadro di delimitazione.

Un file EPS non può utilizzare nessuno dei seguenti operatori:

* dispositivo a banda,
* cleardictstack
* copia pagina
* cancellazione
* server di uscita
* dispositivo frame
* grande tutto
* clip di avvio
* grafica iniziale
* matrice iniziale
* uscire
* bande di rendering
* globale
* dispositivo di impostazione della pagina
* set condiviso
* inizio lavoro.

## Conversione di EPS in altri formati di file

I file EPS possono essere convertiti in formati immagine standard come [JPG](/it/image/jpeg/), [PNG](/it/image/png/), [TIFF](/it/image/tiff/) e [PDF](/it/pdf /) utilizzando diverse applicazioni, ad es. Adobe Illustrator, Photoshop e PaintShop Pro.

A causa di una [vulnerabilità della sicurezza](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) nei file EPS, Office 2016, Office 2013, Office 2010 e Office 365 hanno disattivato la possibilità di inserire file EPS nei documenti di Office.

## Riferimenti

* [PostScript incapsulato - di Wikipedia](https://en.wikipedia.org/wiki/PostScript_incapsulato)

