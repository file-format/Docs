
{
  "date": "2021-12-14",
  "keywords": [
".abc failu",
"pagarinājumu",
"formātā",
"ActionScript baitu koda fails",
"kā atvērt .abc failu",
"abc faila formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ABC — ActionScript baitu koda fails",
  "description": "Uzziniet par ABC faila formātu, izmantojot piemēru un API, kas var izveidot un atvērt ABC failus.",
  "linktitle": "ABC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ab-lvc"
}
},
  "lastmod": "2021-12-14"
}

## Kas ir ABC fails?

Fails ar paplašinājumu .abc ir ActionScript baitu koda fails, ko Flash kompilators izveidojis ActionScript skriptu failu kompilēšanas rezultātā. ABC failā ietverto baitu kodu izpilda ActionScript virtuālā mašīna (AVM un AVM2). Baitu kods sastāv no nemainīgiem datiem, instrukcijām no AVM2 instrukciju kopas un dažāda veida metadatiem. Kad ABC fails tiek ielādēts AVM vai AVM2, tas tiek pārbaudīts. Ja tas neatbilst AVM2 pārskatam, tas tiek noraidīts. ABC failus var atvērt Adobe Flash Player, kas jau sen ir pārtraukts.

## ABC faila formāts — vairāk informācijas

ABC faili tiek saglabāti diskā binārā faila formātā, ko var lasīt AVM vai AVM2 virtuālajās mašīnās. Tā iekšējā faila struktūra attēlo izpildāmā koda bloku ar visiem tā pastāvīgajiem datiem, tipu deskriptoriem, kodu un metadatiem.

## ABC failu struktūra

ABC faila struktūra ir tāda, kā parādīts zemāk.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC failu lauki

|Lauka nosaukums|Apraksts|
---|---|
|minor_version, major_version|Major_version un minor_version vērtības ir abcFile formāta galveno un mazāko versiju numuri.|
|constant_pool|Constant_pool ir mainīga garuma struktūra, kas sastāv no veseliem skaitļiem, dubultniekiem, virknēm, nosaukumvietām, nosaukumvietu kopām un vairākiem nosaukumiem.|
|method_count, method|Metodes_skaita vērtība ir ierakstu skaits metodes masīvā. Katrs ieraksts metožu masīvā ir mainīga garuma method_info struktūra.|
|metadata_count, metadata|Metadata_count vērtība ir ierakstu skaits metadatu masīvā. Katrs metadatu ieraksts ir metadata_infostruktūra, kas saista nosaukumu ar virknes vērtību kopu. |
|class_count, instance, class|Class_count vērtība ir ierakstu skaits instances un klases masīvos. |
|script_count, script|Skriptu_skaita vērtība ir ierakstu skaits skriptu masīvā. Katrs skripta ieraksts ir script_info struktūra, kas nosaka viena skripta raksturlielumus šajā failā. |
|method_body_count, method_body|Metodes_body_count vērtība ir ierakstu skaits masīvā method_body. Katrs method_bodyentry sastāv no mainīga garuma method_body_info struktūras, kurā ir norādījumi par atsevišķu metodi vai funkciju.|

## Atsauces

 * [Robust ABC (ActionScript Bytecode) [Dis-]Assembler — Github](https://github.com/CyberShadow/RABCDAsm)

