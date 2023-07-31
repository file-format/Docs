{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - Formato file di raccolta TrueType",
  "description":"Un file TrueType Collection (TTC) combina più caratteri in un unico file. Sia Apple che Microsoft utilizzavano TTF su sistemi operativi Mac e Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Che cos'è un file TTC?
Il TTC è abbreviato come TrueType Collection è un'estensione del formato True Type. Un file TTC può combinare più file di font al suo interno. Questi file sono utili per combinare più font che condividono molti glifi in comune. Prima di Windows 2000, i file TTC venivano utilizzati nelle versioni di Windows in cinese, giapponese e coreano, ma in seguito il supporto era disponibile per tutte le regioni.


## La struttura del file di raccolta dei caratteri
Un file TTC è costituito da una tabella di intestazione TTC, directory di tabelle e più tabelle OpenType. L'intestazione TTC deve essere trovata all'inizio del file. Deve esistere una directory tabella completa per ogni tipo di carattere. Il formato TableDirectory dovrebbe essere simile a quello esistente in un file non di raccolta. I conteggi delle tabelle in tutte le directory all'interno di un file TTC vengono calcolati dall'inizio di un file TTC.
Le tabelle in un file TTC sono referenziate attraverso la directory delle tabelle dei rispettivi font. Alcune delle tabelle OpenType devono apparire più volte, una per ogni carattere aggiunto nel TTC. Considerando che le altre tabelle possono essere condivise da più caratteri nel file TTC.

### Intestazione TTC
Finora sono disponibili due versioni della tabella Header TTC:
- La versione 1.0 viene utilizzata per i file TTC senza firme digitali.
- La versione 2.0 può essere utilizzata per file TTC con o senza firme digitali.
Ecco le tabelle di intestazione TTC di entrambe le versioni:

**Versione intestazione TTC 1.0:**

|Tipo|Nome|Descrizione|
---|---|---|
|TAG|ttcTag|Stringa ID raccolta font: 'ttcf' (usata per caratteri con contorni CFF o CFF2 e con contorni TrueType)|
|uint16|majorVersion|Versione principale dell'intestazione TTC, = 1.|
|uint16|minorVersion|Versione secondaria dell'intestazione TTC, = 0.|
|uint32|numFonts|Numero di caratteri in TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Matrice di offset nella TableDirectory per ogni carattere dall'inizio del file|

**Versione intestazione TTC 2.0:**

|Tipo|Nome|Descrizione|
---|---|---|
|TAG|ttcTag |Stringa ID raccolta font: 'ttcf'|
|uint16| majorVersion |Versione principale dell'intestazione TTC, = 2.|
|uint16| minorVersion |Versione minore dell'intestazione TTC, = 0.|
|uint32| numFonts |Numero di caratteri in TTC|
|Offset32| tableDirectoryOffsets[numFonts] |Matrice di offset nella TableDirectory per ogni carattere dall'inizio del file|
|uint32| dsigTag |Tag che indica che esiste una tabella DSIG, 0x44534947 ('DSIG') (null se nessuna firma)|
|uint32| dsigLength |La lunghezza (in byte) della tabella DSIG (null se nessuna firma)|
|uint32| dsigOffset |L'offset (in byte) della tabella DSIG dall'inizio del file TTC (null se nessuna firma)|

## Riferimenti
* [Il file dei caratteri OpenType](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

