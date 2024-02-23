{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "File WOFF2: file in formato Web Open Font 2.0",
  "description": "Scopri cos'è un file WOFF2 e le API che possono creare e aprire il file WOFF2.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-it2"
}
},
  "lastmod": "2023-01-10"
}

## Cos'è un file WOFF2?

WOFF2 è un formato di file di font che è una versione più compressa del Web Open Font Format (WOFF). È stato sviluppato come un modo per ridurre la dimensione del file dei caratteri web, consentendo loro di caricarsi più velocemente e utilizzare meno larghezza di banda. WOFF2 utilizza un algoritmo di compressione chiamato Brotli per comprimere i dati dei caratteri, il che può comportare dimensioni di file significativamente inferiori rispetto ai caratteri [WOFF](/font/woff/) equivalenti. Questo formato è supportato dalla maggior parte dei browser Web moderni tra cui Chrome, Firefox, Safari, Opera ed Edge (versione 14 e successive).

## Formato file WOFF2: ulteriori informazioni

La struttura interna di un file di font WOFF2 è composta da diverse parti diverse, tra cui un'intestazione, metadati, una directory di tabelle e i dati del font stesso.

 1. L'intestazione contiene informazioni sul formato generale del file, incluso il numero di versione e il numero di tabelle presenti nel file.

 1. La sezione Metadati contiene informazioni come nome del carattere, copyright e altre informazioni relative ai caratteri.

 1. La directory della tabella contiene informazioni sulle diverse tabelle che compongono il carattere, inclusa la loro posizione nel file e la loro lunghezza.

 1. I dati del carattere stesso sono suddivisi in diverse tabelle, ciascuna delle quali contiene informazioni specifiche sul carattere, come i suoi caratteri e i glifi corrispondenti. Queste tabelle possono includere:

 * La tabella glyf contiene i contorni effettivi del carattere, inclusa la forma e la dimensione di ciascun carattere.
 * La tabella head contiene informazioni generali sul carattere, come il numero di versione, la dimensione del disegno e così via.
 * La tabella 'hmtx' contiene informazioni sulle metriche del carattere, comprese le larghezze e le posizioni dei caratteri.
 * Ogni tabella viene compressa e archiviata nel formato file WOFF2 dopo aver completato il processo di codifica.

La struttura complessiva è progettata per consentire l'analisi e la decodifica rapide, in modo che i browser Web possano caricare e visualizzare il carattere in modo rapido ed efficiente su un sito Web.

### Intestazione WOFF2
L'intestazione WOFF è composta da una firma identificativa che indica il tipo di dati inclusi nel file. L'intestazione WOFF insieme ai suoi campi è la seguente.

|Tipo|Nome campo|Descrizione|
---|---|---|
|UInt32|firma |0x774F4632 'wOF2' |
|UInt32| sapore |La versione sfnt del carattere di input.|
|UInt32| length |Dimensione totale del file WOFF.|
|UInt16| numTables |Numero di voci nella directory delle tabelle dei caratteri.|
|UInt16| riservato |Riservato; impostato a zero.|
|UInt32| totalSfntSize |Dimensione totale necessaria per i dati dei caratteri non compressi, inclusa l'intestazione sfnt, la directory e le tabelle dei caratteri (incluso il riempimento).|
|UInt32| totalCompressedSize Lunghezza totale del blocco dati compresso.|
|UInt16| majorVersion |Versione principale del file WOFF.|
|UInt16| minorVersion |Versione secondaria del file WOFF.|
|UInt32| metaOffset |Offset al blocco di metadati, dall'inizio del file WOFF.|
|UInt32| metaLength |Lunghezza del blocco di metadati compressi.|
|UInt32| metaOrigLength |Dimensione non compressa del blocco di metadati.|
|UInt32| privOffset |Offset al blocco dati privato, dall'inizio del file WOFF.|
|UInt32| privLength |Lunghezza del blocco dati privato.|


## Riferimenti
 * [Formato file w3 WOFF2](https://www.w3.org/TR/WOFF2/)

