{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ZST fails — Zstandarta saspiestā faila formāts",
  "description":"Uzziniet par ZST faila formātu un API, kas var izveidot un atvērt ZST failus.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-lv",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Kas ir ZST fails?

ZST fails ir saspiests fails, kas tiek ģenerēts ar Zstandarta (zstd) saspiešanas algoritmu. Tas ir saspiests fails, kas tiek izveidots ar bezzudumu saspiešanu, izmantojot algoritmu. ZST failus var izmantot, lai saspiestu dažāda veida failus, piemēram, datu bāzes, failu sistēmas, tīklus un spēles. Zstandartu regulē [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878), kas apraksta kopējo saspiešanas mehānismu, multivides veidu un satura kodējumu.

## ZST faila formāts

ZST faili tiek saglabāti diskā saspiestā faila formātā. Kompresijas mehānisms ir aprakstīts RFC 8878, kas noveco RFC 8478.

## ZST rāmji

ZST fails sastāv no viena vai vairākiem kadriem. Katrs rāmis var būt Zstandarta rāmis vai izlaižams rāmis. Zstandarta ietvarā ir saspiesti dati, savukārt izlaižamajā ietvarā ir pielāgoti lietotāja metadati.

### Zstandarta rāmis

Zstandarta rāmim ir šāda struktūra.

|Lauks|Izmērs baitos|
---|---|
|Maģiskais_skaitlis |4 baiti|
|Frame_Header |2–14 baiti|
|Datu_Block |n baiti|
|[Vairāk datu_bloku] ||
|[Content_Checksum] |4 baiti|

### Izlaižams rāmis

Izlaižams rāmis ļauj ievietot lietotāja definētus metadatus savienoto kadru plūsmā. Izlaižamā rāmja struktūra ir šāda.

|Maģiskais_skaitlis |Rāmja_izmērs |Lietotāja_dati|
---|---|---|
|4 baiti |4 baiti |n baiti|

## Atsauces Nr.

* [RFC 8878 Zstandard Compression](https://www.rfc-editor.org/rfc/rfc8878)


