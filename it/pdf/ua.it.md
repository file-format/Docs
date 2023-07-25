{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file PDF/UA",
  "description":"Scopri il formato di file PDF/UA e le API che possono creare e aprire file PDF/UA.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Che cos'è il file PDF/UA? #

PDF/UA è stato pubblicato come [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) nell'agosto 2012 ed è di gran lunga la prima definizione completa di una serie di requisiti per documenti PDF universalmente accessibili. Il termine "universalmente accessibile" si riferisce alla comprensione che le informazioni contenute in un documento [PDF](/it/pdf/) dovrebbero essere ugualmente e indipendentemente accessibili a tutti in generale e alle persone con disabilità in particolare. L'introduzione dello standard PDF/UA può essere considerata un passo importante per la creazione di strumenti e applicazioni al fine di creare e leggere il contenuto PDF.

## Requisiti del formato del file ##

Il PDF/UA ha alcuni requisiti definiti alla base che fungono da essenza di questo standard. Essenzialmente, si basano sull'assegnazione di tag ai PDF, il che significa che tutti i documenti PDF/UA devono essere taggati correttamente. Richiede inoltre che i tag siano semanticamente appropriati e in ordine logico. Ciò garantisce che il documento finale creato con le specifiche PDF/UA sia più affidabile e accessibile. Ciò potrebbe portare gli autori di PDF a chiedersi se hanno bisogno di sapere tutto su tutti questi requisiti? Fortunatamente, non è così perché gli strumenti di conformità PDF/UA si assumono la responsabilità di aggiungere e preservare l'accessibilità del PDF.

I requisiti del formato file per PDF/UA sono i seguenti.

* Il contenuto è classificato in due modi: contenuto significativo e artefatti come elementi decorativi della pagina. Tutti i contenuti significativi devono essere contrassegnati e integrati nella struttura ad albero di tutti i tag all'interno di un documento. I manufatti, d'altra parte, devono solo essere contrassegnati come tali.
* I contenuti significativi devono essere contrassegnati con tag e, insieme agli altri tag nel documento, creare una struttura ad albero completa.
* I contenuti significativi devono essere contrassegnati con i tag semantici appropriati.
* L'albero della struttura creato dai tag del documento deve riflettere l'ordine di lettura logico del documento.
* Possono essere utilizzati solo i tag standard definiti in PDF 1.7; se vengono utilizzati altri tag, una voce di assegnazione di ruolo deve registrare quale tag standard rappresenta ciascuno di essi.
* Le informazioni non possono essere trasmesse utilizzando solo mezzi visivi (ad es. contrasto, colore o posizione sulla pagina).
* Non sono consentiti contenuti sfarfallio, lampeggiante o lampeggiante, sia come effetti controllati da JavaScript sia come parte di qualsiasi video incorporato nel PDF.
* È necessario fornire un titolo del documento e il documento deve essere impostato in modo che il titolo (anziché il nome del file) appaia nel titolo della finestra.
* La lingua di tutti i contenuti deve essere annotata e le modifiche alla lingua devono essere esplicitamente contrassegnate come tali.

## Conformità PDF/UA ##

Lo standard PDF/UA definisce le specifiche per contenuto, lettori e tecnologia assistiva. Questi tre aspetti sono collegati tra loro in base ai contenuti del documento. I requisiti di conformità per ciascuno di questi sono indicati di seguito.

## File conformi ##

I file conformi allo standard PDF/UA devono contenere funzionalità valide secondo le [specifiche PDF 1.7](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). Tuttavia, le funzionalità vietate da PDF/UA in particolare dovrebbero essere escluse.

## Lettori conformi ##

Un lettore conforme deve obbedire alle regole scritte dalle specifiche PDF 1.7. Nello specifico dovrebbe supportare:

* tutti i tag, attributi e valori chiave specificati per l'accessibilità. Dovrebbe anche avere la capacità di elaborare e rappresentare firme digitali, annotazioni e Contenuti facoltativi.
* elaborare e rappresentare firme digitali, annotazioni e contenuti opzionali
* navigare nel documento con una varietà di mezzi

## Tecnologia assistiva conforme ##

Una tecnologia assistiva conforme è destinata a supportare le funzionalità PDF/UA. Questi includono, ad esempio, le caratteristiche del contenuto e del lettore e dovrebbero consentire la navigazione per etichette di pagina, struttura del documento o struttura. Dovrebbe anche consentire all'utente di ignorare lo zoom di navigazione predefinito.

## Riferimenti ##

* [PDF/UA - Di Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA in breve](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

