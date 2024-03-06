{
  "date": "2020-11-11",
  "keywords": [
"DTSX",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par DTSX faila formātu un API, kas var izveidot un atvērt DTSX failus.",
  "title": "DTSX faila formāts — SQL servera DTS iestatījumu fails",
  "linktitle": "DTSX",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dts-lvx"
}
},
  "lastmod": "2020-08-12"
}

## Kas ir DTSX fails?

Fails ar paplašinājumu .dtsx (Data Transformation Services Package XML) ir datu pārveidošanas pakalpojumu (DTS) fails, ko Microsoft SQL izmanto, lai atsauktos uz datu migrācijas darbībām/noteikumiem datu pārsūtīšanai no vienas datu bāzes uz citu. Tas ietver transformācijas un jebkādas izvēles apstrādes darbības, kas var būt nepieciešamas datu pārsūtīšanas laikā starp sākuma un galamērķa punktu. SQL Server Integration Services (SSIS), Microsoft SQL Server komponents, izmanto DTSX failus, lai identificētu datu apstrādes darbības starp datu bāzes serveriem. DTSX failus var atvērt, izmantojot Microsoft SQL Server 2019.

## DTSX faila formāts

Datu pārvietošanai starp datu bāzes serveriem ir nepieciešami noteikumi un apstrādes darbības, lai nodrošinātu datu integritāti šīs darbības laikā. SSIS nodrošina, ka visas šīs darbības, lai pārvietotu un pielāgotu datus no dažādiem avotiem uzņēmumā, notiek ērti. Šeit nāk DTSX, kas nosaka struktūras, kas jāizmanto SSIS, lai noteiktu darbības, kurās datus var apstrādāt, kā tas izriet no šīm darbībām.

DTSX aprakstītā datu plūsma ir tāda, kā parādīts nākamajā attēlā.

{{< figure src="../DataFlowDTSX.png" alt="Datu plūsma DTSX" >}}

DTSX is [XML](/web/xml/)-based and is documented in [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). The enhanced refactoring of DTSX XML is DTSX 2.0 that includes new attributes to the structures, replacement of named properties as parent XML attributes, specifies defaults for most attribute values, and placement of repeated elements inside a parent element. DTSX structures are described using these [XML Schemas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) and the structural format is celar-text XML.

## Atsauces

 * [DTSX formāts — Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
 * [DTSX 2 formāts — Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

