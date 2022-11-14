{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - File del linguaggio di definizione dei rapporti",
  "keywords" :[ "rdl", "report Definition Language", "XmlTextWriter", "XSD", "RDL element"],
  "description":"Informazioni sul formato di file RDL che è una rappresentazione XML di una definizione di report di SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Che cos'è un file RDL? ##

L'RDL (Report Definition Language) è un benchmark impostato da Microsoft per la definizione dei report. Un file RDL è costituito da uno o più elementi RDL. Considerando che un elemento RDL è costituito dal tipo di dati e dalla cardinalità. Un elemento può essere semplice o complesso. L'elemento semplice non ha alcun elemento figlio o attributo, mentre un elemento complesso ha figli e attributi facoltativi.

## Definizione dello schema XML RDL
Un file XML Schema Definition (XSD) convalida il file RDL. Lo schema definisce le regole in cui gli elementi RDL possono verificarsi in un file .rdl. Un elemento RDL può essere semplice o complesso. Un elemento semplice non ha elementi figlio o attributi e un elemento complesso ha figli e, facoltativamente, attributi.

## Creazione di RDL
Poiché RDL è di natura aperta ed estensibile, è possibile creare molte applicazioni e strumenti che generano file RDL basati sul suo schema XML. Uno dei modi più semplici per creare RDL da un'applicazione consiste nell'utilizzare le classi Microsoft .NET Framework dello spazio dei nomi **System.Xml** e dello spazio dei nomi System.Linq. In particolare, la classe **XmlTextWriter** può essere utilizzata per scrivere RDL. È possibile generare una definizione di report completa dall'inizio alla fine in qualsiasi applicazione .NET Framework utilizzando **XmlTextWriter**. Gli sviluppatori possono anche aggiungere elementi di report personalizzati con proprietà personalizzate per estendere l'RDL.

## Tipi RDL
La tabella seguente elenca i tipi e gli attributi utilizzati negli elementi RDL.

|Tipo|Descrizione|
---|---|
|Binary |Una proprietà con un valore binario codificato in base 64.|
|Booleano| Una proprietà con true o false come valore dell'oggetto. Se non diversamente specificato, il valore di un oggetto booleano facoltativo omesso è False.|
|Data |Una proprietà con una data completamente specificata o un valore data/ora specificato nel formato data ISO8601: AAAA-MM-GG[THH:MM[:SS[.S]]].|
|Enum |Una proprietà con un valore di testo stringa che deve essere uno di un elenco di valori designati.|
|Float |Una proprietà con un valore float. Un punto (.) viene utilizzato come separatore decimale facoltativo.|
|Intero |Una proprietà con un valore intero (int32).|
|Lingua |Una proprietà con un valore di testo che contiene un codice lingua e cultura, ad esempio "en-us" per l'inglese americano. Il valore deve essere una lingua specifica o una lingua neutra per la quale in Microsoft .NET Framework è definita una lingua predefinita.|
|Nome |Una proprietà con un valore di testo stringa. I nomi devono essere univoci all'interno dello spazio dei nomi dell'elemento. Se non specificato, lo spazio dei nomi per un elemento è l'oggetto contenitore più interno che ha un nome.|
|NormalizedString |Una proprietà con un valore di testo stringa che è stato normalizzato.|
|Size |Un elemento size deve contenere un numero (con un carattere punto utilizzato come separatore decimale opzionale). Il numero deve essere seguito da un designatore per un'unità di lunghezza CSS come cm, mm, in, pt o pc. Uno spazio tra il numero e il designatore è facoltativo. Per ulteriori informazioni sui designatori delle dimensioni, vedere Riferimento per valori e unità CSS. In RDL, il valore massimo per Size è 160 pollici. La dimensione minima è 0 pollici.|
|Stringa |Una proprietà con un valore di testo stringa.|
|UnsignedInt |Una proprietà con un valore intero senza segno (uint32).|
|Variante |Una proprietà con qualsiasi tipo XML semplice.|

## Tipi di dati RDL
In RDL, DataType Enumeration definisce il tipo di dati di un attributo, un'espressione o un parametro. La tabella seguente mostra come i tipi di dati CLR corrispondono ai tipi di dati RDL.

|Tipi CLR |Tipi di dati corrispondenti|
---|---|
|Booleano| booleano|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Intero|
|Singolo, Doppio |Flottante|
|Stringa, Char, GUID, Intervallo di tempo |Stringa|


## Riferimenti ##

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

