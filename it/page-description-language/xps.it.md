{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Specifiche carta XML", "File", "Estensione", "Formato file", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Formato file layout di pagina",
  "description":"Scopri il formato di file XPS e le API che possono creare e aprire file XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Che cos'è un file XPS? ##

Un file XPS rappresenta i file di layout di pagina basati sulle specifiche della carta XML create da Microsoft. È stato sviluppato in sostituzione del formato di file EMF ed è simile al formato di file [PDF](/it/pdf/), ma utilizza XML nel layout, nell'aspetto e nelle informazioni di stampa di un documento. In effetti, è più giustificato affermare che XPS è un tentativo su PDF, ma non è riuscito a ottenere abbastanza popolarità in quanto di proprietà di PDF per molte ragioni. Microsoft fornisce XPS Document Writer per impostazione predefinita da Windows 7 in poi per la creazione di file XPS. I file XPS possono essere generati selezionando "Microsoft XPS Document Writer" come stampante durante la stampa del documento.

I visualizzatori XPS sono integrati come parte di Windows Vista, Windows 7, Windows 8 e Internet Explorer 6 o versioni successive. I file XPS diventano di sola lettura una volta generati. Ciò aumenta la fiducia dell'utente nei documenti ricevuti inviati come XPS per l'autenticità del documento. Un documento XPS può contenere una o più pagine convertite dal documento originale.

## Breve storia ##

Microsoft ha presentato la specifica XPS a Ecma International. Nel giugno 2007, l'Ecma Technical Committee 46 (TC46) è stato istituito per sviluppare uno standard basato sulle specifiche della carta OpenXPS. Ecma International ha approvato lo Standard Ecma (ECMA-388) [Specifiche XPS](http://www.ecma-international.org/publications/standards/Ecma-388.htm) nel giugno 2009 alla 97a Assemblea Generale.

## Formato file XPS ##

Il formato XPS è costituito da markup XML che definisce la composizione di un documento e l'aspetto visivo di ogni pagina insieme alle regole di rendering per la visualizzazione o la stampa del documento. Conserva tutte le informazioni per ricreare un documento su qualsiasi sistema che lo renda indipendente dalle risorse disponibili su quel sistema. Il formato è essenzialmente un archivio ZIP e se rinomini l'estensione del file in ZIP, vedrai i file costitutivi che contengono i dati del documento. Questi documenti includono:

* file di pagina del documento (.fpage) - Contiene il contenuto del documento e le impostazioni del formato del documento. Ogni pagina nel documento XPS ha un file FPAGE.
* file delle impostazioni del documento (.fdoc) - Memorizza le impostazioni incluse nell'archivio XPS.
* file frammento di documento (.frag) - Definisce le impostazioni per il file XPS effettivo e ogni pagina del documento ha il proprio file .frag.

{{< figure src="../XPS-1.png" alt="Formato file XPS" >}}

Questi file conservano il contenuto del documento in modo tale che se, ad esempio, qualcuno non ha gli stessi caratteri installati sul proprio computer, il visualizzatore XPS riprodurrà comunque quei caratteri originali. Ciò implica l'inclusione di un file di markup XML per ciascuno:

* Pagina
* Testo
* Caratteri incorporati
* Immagini raster
* Grafica vettoriale 2D
* Gestione dei diritti digitali

Il formato del documento XPS include un insieme ben definito di parti e relazioni, ognuna delle quali soddisfa uno scopo particolare nel documento. Il formato estende anche le funzionalità del pacchetto, comprese le firme digitali, le miniature e l'interleaving.

Un tipico documento XPS ha il seguente aspetto e può essere analizzato alla luce del formato file XPS [specifiche](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="Formato file XPS" >}}


## Riferimenti ##

* [Specifiche del formato file XPS](http://www.ecma-international.org/publications/standards/Ecma-388.htm)
* [XPS - Di Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

