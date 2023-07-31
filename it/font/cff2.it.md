{
  "date" : "2020-08-20",
  "keywords" :[ "file cff2", "formato file cff2", "cos'è un file cff2", "file", "esempio cff2", "estensione file cff2", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Formato file font compatto versione 2",
  "description":"Scopri il formato file CFF2 e le API per creare e aprire file CFF2.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Che cos'è un file CFF2?

Il formato di file CFF2 è la versione 2.0 del formato di file CFF e consente l'archiviazione efficiente di contorni di glifi e metadati simili al formato di file CFF. CFF2 differisce da CFF in quanto è concepito per essere utilizzato nel contesto di un font OpenType come tabella 'sfnt' con il tag CFF2. Non può essere utilizzato come programma autonomo e dipende dai dati in altre tabelle OpenType.

## Formato file CFF2

Le [Specifiche del formato file CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) contengono dettagli sul layout dei dati interni, i tipi di dati, le tabelle e altre informazioni interne sul formato del file. Può essere fatto riferimento per riferimento allo sviluppatore. Alcuni dei dettagli su questi sono i seguenti.

### Disposizione dei dati

I dati binari del formato file CFF2 sono organizzati logicamente come un numero di strutture dati separate. Il layout all'interno dei dati binari è come mostrato nella tabella seguente.

|Inserimento |Commenti|
---|---|
|Intestazione |Posizione fissa|
|Top DICT| Posizione fissa|
|INDICE SOTTOSCRITTO Globale| Posizione fissa|
|Variante |Negozio|
|FDSelect |Presentato solo se è presente più di un Font DICT nel Font DICT INDEX.|
|INDICE DICT font ||
|Matrice di caratteri DICT| Incluso nel carattere DICT INDEX.|
|DICT privato| Uno per carattere DICT.|

Solo le prime tre strutture sono basate su postazioni fisse. I rimanenti vengono raggiunti tramite offset e il loro ordinamento può essere modificato.

### Tipi di dati

Il formato di file CFF2 utilizza i seguenti tipi di dati.

|Nome |Intervallo |Descrizione|
---|---|---|
|uint8 |da 0 a 255 |numero senza segno a 8 bit|
|uint16 |0 a 65535| Numero senza segno a 16 bit|
|uint32 |0 a 4294967295| Numero senza segno a 32 bit|
|Spostamento |varia| Offset di 1, 2, 3 o 4 byte (specificato dal campo OffSize in una tabella Indice)|
|OffSize |da 1 a 4| Il numero senza segno a 1 byte specifica la dimensione di uno o più campi Offset|

Memorizza tutti i dati numerici multibyte e i campi di offset in ordine di byte big-endian. Il formato CFF2 è privo di byte di riempimento in quanto non rispetta alcuna restrizione di allineamento.

### Dati DICT

I file CFF2 contengono i dati del dizionario dei caratteri come coppie chiave-valore in un formato tokenizzato compatto. Le chiavi del dizionario sono codificate come operatori a 1 o 2 byte ei valori del dizionario sono codificati come operandi numerici di dimensione variabile. Esistono tre strutture che utilizzano il formato dati DICT: `Top DICT`, `Font DICT` e `Private DICT`. Un certo numero di tipi di operandi interi di dimensioni variabili sono definiti e codificati come mostrato nella tabella seguente (il primo byte dell'operando è b0, il secondo è b1 e così via).

|Taglia |Intervallo b0 |Intervallo di valori |Calcolo del valore|
---|---|---|---|
|1 |da 32 a 246| da -107 a +107 |b0 - 139|
|2 |da 247 a 250| da +108 a +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |da 251 a 254| da -1131 a -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| da -32768 a +32767| b1 << 8 | b2|
|5 |29| -(2^31) a +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Intestazione

I dati binari iniziano con un'intestazione con il formato mostrato nella tabella seguente.

|Tipo |Nome |Descrizione|
---|---|---|
|uint8| majorVersion| Formatta la versione principale. Impostare su 2.|
|uint8| minorVersion| Formatta la versione minore. Impostare a zero.|
|uint8| headerSize| Dimensione dell'intestazione (byte).|
|uint16| topDictLength| Lunghezza della struttura DICT superiore in byte.|

## Riferimenti

* [Formato file CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

