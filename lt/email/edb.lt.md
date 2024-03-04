{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EDB failo formatas – „Exchange Mail“ duomenų bazės failas",
  "description": "Sužinokite apie EDB failo formatą ir API, kurios gali kurti ir atidaryti EDB failus.",
  "linktitle": "EDB",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ed-ltb"
}
},
  "lastmod": "2020-09-16"
}

## Kas yra EDB failas?

Failas su .edb plėtiniu yra pašto dėžutės duomenų bazė, sukurta Microsoft Exchange Server, skirta su paštu susijusiems duomenims saugoti. EDB, Exchange duomenų bazė, saugo pranešimus, kurie yra apdorojami ir ne SMTP. EDB taip pat žinomas kaip Extensible Storage Engine (ESE) duomenų bazės failai ir saugo failus naudojant b-tree struktūrą. Kaip saugyklos failus, EDB failus galima konvertuoti į kitus pašto saugojimo failų formatus, tokius kaip [PST](/email/pst/) ir [OST](/email/ost/).

## EDB failo formatas

Nėra oficialių / atvirų EDB failo formato specifikacijų, kurias būtų galima nurodyti. Padaryta tam tikra pažanga kuriant failo formato atvirkštinę inžineriją, todėl buvo iššifruotos dalinės specifikacijos. Remiantis šiais duomenimis, EDB failą sudaro:
 * Failo antraštė – yra duomenų bazės failo antraštės informacija
 * Fiksuoto dydžio puslapiai – yra duomenų bazė, kurią sudaro lentelės ir indeksai

### Duomenų bazės failo antraštė
Duomenų bazės failo antraštė yra pirmajame duomenų bazės puslapyje ir yra mažiausiai 668 baitai. Failo antraštėje, be kitų laukų, yra Failo formato versija ir Failo tipas.

#### Failų tipai
|Tipas|Aprašymas
---|---|
|0| Duomenų bazė|
|1| Srautinis |

Pastaba: šių tipų identifikatoriai nežinomi.

#### Failo formato versija
Pradinis EDB formatas prasidėjo 1997 m. balandžio mėn. ir vėliau buvo keičiamas.

|Revsion Date|Version|Revision|description
---|---|---|---|
|1997 m. balandis| 0x00000620|0x00000000| Originalus operacinės sistemos Beta formatas.|
|1997 m. gegužės mėn. |0x00000620|0x00000001| Pridėkite prie katalogo stulpelių sąlyginiam indeksavimui ir OLD.|
|1997 m. birželis|0x00000620|0x00000002|Pridėkite IDB vėliavėlę fLocalizedText.|
|1997 m. spalis|0x00000620|0x00000003|Pridėkite SPLIT_BUFFER prie tarpo medžio šaknų puslapių.|
|1998 m. sausio mėn.|0x00000620|0x00000002|Grąžinti peržiūrą, kad ESE97 išliktų suderinamas.|
||0x00000620|0x00000003|Pridėkite naujų pažymėtų stulpelių prie katalogo (CallbackData ir CallbackDependencies).|
|1998 m. gegužės mėn.|0x00000620|0x00000004|Super Long Value (SLV) palaikymas: signSLV, fSLVYra duomenų antraštėje.|
|1998 m. gegužės mėn.|0x00000620|0x00000005|Naujas SLV erdvės medis.|
|1998 m. spalio mėn.|0x00000620|0x00000006|SLV erdvės žemėlapis.|
|1998 m. gruodžio mėn.|0x00000620|0x00000007|4 baitų IDXSEG.|
|1999 m. sausis|0x00000620|0x00000008|Naujas šablono stulpelio formatas.|
|1999 m. birželis|0x00000620|0x00000009|Surūšiuoti šablono stulpeliai. Naudojama Windows XP SP3|
||0x00000620|0x0000000b|Yra puslapio antraštė su ECC kontroline sumaUsed in Exchange|
||0x00000620|0x0000000c|Naudojama sistemoje Windows Vista (SP0)|
||0x00000620|0x00000011|Palaiko 2 KiB, 16 KiB ir 32 KiB puslapius.Išplėstinė puslapio antraštė su papildomomis ECC kontrolinėmis sumomis.Stulpelių suspaudimas.Užuomina apie erdvę.Naudojama Windows 7 (SP0)|
|1999 m. gegužės mėn.|0x00000623|0x00000000|Naujas erdvės vadovas.|

### Duomenų bazės failai

EDB duomenų bazės faile yra visų duomenų bazėje esančių lentelių schema. Be to, joje taip pat yra visų duomenų bazės lentelių įrašai ir lentelių indeksai. Jo vieta nustatoma pagal šiuos identifikatorius.

* JetCreateDatabase

* JetCreateDatabase2

* JetAttachDatabase

* JetAttachDatabase2


Remiantis jais, duomenų bazės būklę galima įvertinti taip.

|Vertė|Identifier|Aprašymas
---|---|---|
|1|JET_dbstateJustCreated|Duomenų bazė ką tik sukurta.|
|2|JET_dbstateDirtyShutdown|Kad duomenų bazėje būtų galima naudoti arba kilnoti, reikia atlikti standųjį arba minkštąjį atkūrimą. Tokios būsenos duomenų bazių nereikėtų bandyti perkelti.|
|3|JET_dbstateCleanShutdown|Duomenų bazės būsena yra švari. Duomenų bazė gali būti pridėta be jokių žurnalo failų.|
|4|JET_dbstateBeingConverted|Duomenų bazė atnaujinama.|
|5|JET_dbstateForceDetachInternal|Ši reikšmė įdiegta sistemoje WindowsXP|
 
## Nuorodos
 * [Extensible Storage Engine (ESE) duomenų bazės failo (EDB) specifikacijos](https://github.com/libyal/libesedb/tree/main/documentation)

