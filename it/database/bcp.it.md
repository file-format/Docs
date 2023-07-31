{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file BCP e le API che possono creare e aprire file BCP.",
  "title" :"BCP - Formato file di copia in blocco di SQL Server",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Che cos'è un file BCP?

BCP (Bulk Copy Format) è il formato dei dati tecnici di Microsoft SQL Server che definisce le strutture dei dati per archiviare diversi valori del tipo di dati del database per l'importazione/esportazione. Il formato definisce completamente l'interpretazione di ciascuna colonna di dati in modo che l'insieme di valori specificato nel file di dati possa essere letto. L'utilità [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) utilizza il formato file BCP per leggere dati da tale file e identificarlo.


## Formato file BCP

Il file in formato BCP è un documento XML che definisce l'ordine delle colonne, il nome e il tipo di dati. Consente agli utenti di importare/esportare grandi quantità di dati dal file di dati specificando questi campi. Ciò è utile nell'importazione in blocco di valori di dati da file di dati. Il numero e l'ordine dei campi di dati nel file di dati possono essere diversi da quelli nelle colonne della tabella di destinazione. Questo è quando il file di formato dati BCP viene in aiuto specificando l'ordine e il tipo di colonne per l'importazione dei dati.

La struttura del file di formato è rappresentata nel formato seguente.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### Tipi di dati BCP

|Tipo di dati|Intervallo|Rappresentazione|
---|---|---|
|BigInt|-263 (-9.223.372.036.854.775.808) fino a 263-1 (9.223.372.036.854.775.807)|`BigInt = ["-"]1*19DIGIT`|
|Binario|Da 1 a 8000 byte|Formato di stringa Unicode con codifica esadecimale `Binario = 32000OCTET`|
|Bit|0 o 1|stringa Unicode semplice Bit = "0" / "1"|
|Char|da 1 a 8000|Formato stringa Unicode, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET con n = 4 x (2,147,483,647)|
|Data|0001-01-01 fino a 9999-12-31|Formato stringa AAAA-MM-GG|
|DataOra|1753-01-01 00:00:00.000 fino a 9999-12-31 23:59:59.997| Unicode AAAA-MM-GG hh:mm:ss[.nnn] formato stringa|
|DataOra2|0001-01-01 00:00:00.0000000 fino a 9999-12-31 23:59:59.9999999.| Unicode AAAA-MM-GG hh:mm:ss[.nnnnnnn] formato stringa|
|DateTimeOffset|0001-01-01 da 00:00:00.0000000 a 9999-12-31 23:59:59.9999999 nel fuso orario UTC (Coordinated Universal Time)| Unicode AAAA-MM-GG hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] formato stringa|
|Decimale|-1038 + 1 fino a 1038 – 1|Formato stringa Unicode `Decimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Mobile|-1.79E+308 fino a -2.23E-308; 0; da 2.23E-308 a 1.79E+308|Formato stringa Unicode|
|Immagine|sequenza di byte che vanno da 0 a 231 – 1 (2.147.483.647)|formato di stringa Unicode con codifica esadecimale|
|Int|-231 (-2,147,483,648) fino a 231 – 1 (2,147,483,647)|Formato stringa Unicode|

## Riferimenti

* [Formato BCP - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

