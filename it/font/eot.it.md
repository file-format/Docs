{
  "date" : "2020-08-20",
  "keywords" :[ "file eot", "formato file eot", "cos'è un file eot", "file", "esempio eot", "estensione file eot", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - Formato file font TrueType",
  "description":"Scopri il formato file EOT e le API per creare e aprire file EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Che cos'è un file EOT?

Un file con estensione .eot è un font OpenType incorporato in un documento. Questi sono utilizzati principalmente nei file Web come una pagina Web. È stato creato da Microsoft ed è supportato dai prodotti Microsoft, incluso il file di presentazione PowerPoint [.pps](/it/presentation/pps/). Il file non è di uso primario ed è una sorta di documento di accompagnamento con il documento principale o la pagina web. Simile ai caratteri OTF, EOT supporta sia i contorni Postscript che TrueType per i glifi. I file EOT sono di dimensioni inferiori per il motivo che vengono compressi utilizzando la compressione LZ. EOT utilizza uno strumento Microsoft per creare un font da font TTF/OTF esistenti.

## Breve storia

Il font EOT è stato presentato al W3C nel 2007 come parte di CSS3 ma a causa dei suoi requisiti per essere installato permanentemente su un sistema remoto è diventato il motivo del suo rifiuto. È stato ripresentato nel marzo 2008, ma alla fine il W3C ha scelto [Web Font Format](/it/font/woff/) (WOFF) che è stato poi standardizzato.

## Formato file EOT

I dettagli sul formato del file EOT sono disponibili nella [pagina di invio W3](https://www.w3.org/Submission/EOT/#FileFormat) ed elabora la struttura utilizzata da questo formato di carattere. L'EOT consiste in un'unica struttura EMBEDDEDFONT che fornisce informazioni di base sufficienti sul nome del font e sui caratteri supportati. L'imballaggio di queste informazioni consente agli User Agent di evitare di decomprimere, decomprimere o installare il font se è già presente sulla macchina.

### EMBEDDEDFONT Struttura
La struttura EMBEDDEDFONT ha subito tre revisioni, con l'aggiunta di dati aggiuntivi alla fine della struttura ad ogni revisione. L'ultima revisione della struttura EMBEDDEDFONT è illustrata di seguito.

|Tipo di dati|Nome voce|Descrizione|
---|---|---|
|unsigned long|EOTSize|Lunghezza totale della struttura in byte (inclusi dati di stringhe e caratteri)|
|unsigned long|FontDataSize|Lunghezza del carattere OpenType (FontData) in byte|
|unsigned long|Versione|Numero di versione di questo formato - 0x00020002|
|unsigned long|Flags|Flag di elaborazione|
|byte[10]|FontPANOSE|Il valore PANOSE per questo carattere - Vedi https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|In Windows deriva da TEXTMETRIC.tmCharSet. Questo valore specifica il set di caratteri del font. DEFAULT_CHARSET (0x01) non indica alcuna preferenza. - Vedere https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Corsivo|Se il bit per ITALIC è impostato in OS/2.fsSelection, il valore sarà 0x01 - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Peso|Il valore di peso per questo font - Vedi https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Digitare i flag che forniscono informazioni sulle autorizzazioni di incorporamento - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|Numero magico per file EOT - 0x504C. Utilizzato per verificare la corruzione dei dati.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bit 0-31) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bit 32-63) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bit 64-95) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bit 96-127) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bit 0-31) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bit 32-63) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Riservato1|Riservato - deve essere 0|
|unsigned long|Riservato2|Riservato - deve essere 0|
|unsigned long|Riservato3|Riservato - deve essere 0|
|unsigned long|Riservato4|Riservato - deve essere 0|
|unsigned short|Padding1|Padding per mantenere l'allineamento lungo. Il valore di riempimento deve essere sempre impostato su 0x0000.|
|unsigned short|FamilyNameSize|Numero di byte utilizzati dall'array FamilyName|
|byte|NomeFamiglia[DimensioneNomeFamiglia]|Matrice di caratteri UTF-16 della lunghezza di byte DimensioneNomeFamiglia. Questa è la stringa della famiglia di caratteri in lingua inglese trovata nella tabella dei nomi del carattere (ID nome = 1) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Il valore di riempimento deve essere sempre impostato su 0x0000.|
|unsigned short|StyleNameSize|Numero di byte utilizzati da StyleName|
|byte|StyleName[StyleNameSize]|Matrice di caratteri UTF-16 la lunghezza dei byte StyleNameSize. Questa è la stringa della sottofamiglia di caratteri in lingua inglese trovata nella tabella dei nomi del carattere (ID nome = 2) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Il valore di riempimento deve essere sempre impostato su 0x0000.|
|unsigned short|VersionNameSize|Numero di byte utilizzati da VersionName|
|bytes|VersionName[VersionNameSize]|Matrice di caratteri UTF-16 della lunghezza dei byte VersionNameSize. Questa è la stringa della versione in lingua inglese trovata nella tabella dei nomi del carattere (ID nome = 5) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Il valore di riempimento deve essere sempre impostato su 0x0000.|
|unsigned short|FullNameSize|Numero di byte utilizzati da FullName|
|byte|FullName[FullNameSize]|Matrice di caratteri UTF-16 della lunghezza dei byte FullNameSize. Questa è la stringa del nome completo in lingua inglese trovata nella tabella dei nomi del carattere (ID nome = 4) - Vedere https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Il valore di riempimento deve essere sempre impostato su 0x0000.|
|unsigned short|RootStringSize|Numero di byte utilizzati dall'array RootString|
|byte|RootString[RootStringSize]|Matrice di caratteri UTF-16 la lunghezza dei byte RootStringSize.|
|unsigned long|RootStringCheckSum|Valore CheckSum RootString. Vedere l'algoritmo per elaborare RootStringChecksum di seguito.|
|unsigned long|EUDCCodePage|Valore codepage necessario per il supporto dei caratteri EUDC.|
|unsigned short|Padding6|Il valore di riempimento deve essere sempre impostato su 0x0000.|
|unsigned short|SignatureSize|Numero di byte utilizzati dall'array Signature. Attualmente riservato e dovrebbe essere impostato su 0x0000.|
|byte|Firma[SignatureSize]|Attualmente riservato. Se SignatureSize è 0x0000 non c'è lunghezza per questa matrice.|
|unsigned long|EUDCFlags|Elaborazione flag per il font EUDC. I valori tipici potrebbero essere TTEMBED_XORENCRYPTDATA e TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Numero di byte utilizzati dall'array Signature.|
|byte|EUDCFontData[EUDCFontSize]|Numero di byte utilizzati per i dati del carattere EUDC. Se EUDCFontSize è 0x00000000 non c'è lunghezza per questa matrice. |
|byte|FontData[FontDataSize]|I dati del carattere per questo file EOT. I dati possono essere compressi o criptati XOR come indicato dai flag di elaborazione.|

## Riferimenti

* [Formato file EOT](https://www.w3.org/Submission/EOT/)
* [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Incorporamento font](https://en.wikipedia.org/wiki/Font_embedding)

