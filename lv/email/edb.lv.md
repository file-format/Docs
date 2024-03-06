{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EDB faila formāts — Exchange pasta datu bāzes fails",
  "description": "Uzziniet par EDB failu formātu un API, kas var izveidot un atvērt EDB failus.",
  "linktitle": "EDB",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ed-lvb"
}
},
  "lastmod": "2020-09-16"
}

## Kas ir EDB fails?

Fails ar .edb faila paplašinājumu ir pastkastes datu bāze, ko izveido Microsoft Exchange Server, lai saglabātu ar pastu saistītus datus. EDB, Exchange datu bāze, saglabā ziņojumus, kas ir procesā un nav SMTP. EDB ir pazīstami arī kā Extensible Storage Engine (ESE) datu bāzes faili un glabā failus, izmantojot b-tree struktūru. Kā krātuves failus, EDB failus var pārvērst citos pasta krātuves failu formātos, piemēram, [PST](/email/pst/) un [OST](/email/ost/).

## EDB faila formāts

Nav pieejamas oficiālas/atvērtas EDB faila formāta specifikācijas, uz kurām varētu atsaukties. Ir panākts zināms progress faila formāta reversās inženierijas jomā, kā rezultātā ir veikta daļēja specifikāciju dekodēšana. Saskaņā ar šiem datiem EDB fails sastāv no:
 * Faila galvene — satur datu bāzes faila galvenes informāciju
 * Fiksēta izmēra lapas — satur datu bāzi, kurā ir tabulas un indeksi

### Datu bāzes faila galvene
Datu bāzes faila galvene atrodas pirmajā datu bāzes lapā un ir vismaz 668 baiti. Faila galvenē papildus citiem laukiem ir Faila formāta versija” un Faila tips”.

#### Failu veidi
|Tips|Apraksts
---|---|
|0| Datu bāze|
|1| Straumēšana|

Piezīme. Šo veidu identifikatori nav zināmi.

#### Faila formāta versija
Sākotnējais EDB formāts sākās 1997. gada aprīlī un turpināja attīstīties, lai pēc tam mainītos.

|Revsion Date|Version|Revision|description
---|---|---|---|
|1997. gada aprīlis| 0x00000620|0x00000000| Sākotnējā operētājsistēmas Beta formāts.|
|1997. gada maijs |0x00000620|0x00000001| Pievienojiet katalogā kolonnas nosacījuma indeksācijai un OLD.|
|Jūnijs 1997|0x00000620|0x00000002|Pievienojiet fLocalizedText karogu IDB.|
|1997. gada oktobris|0x00000620|0x00000003|Pievienojiet SPLIT_BUFFER kosmosa koka sakņu lapām.|
|1998. gada janvāris|0x00000620|0x00000002|Atsauciet pārskatīšanu, lai ESE97 joprojām būtu saderīga.|
||0x00000620|0x00000003|Pievienot katalogam jaunas slejas ar atzīmi (CallbackData un CallbackDependencies).|
|1998. gada maijs|0x00000620|0x00000004|Īpaši garas vērtības (SLV) atbalsts: signSLV, fSLVPastāv DB galvenē.|
|1998. gada maijs|0x00000620|0x00000005|Jauns SLV kosmosa koks.|
|1998. gada oktobris|0x00000620|0x00000006|SLV kosmosa karte.|
|1998. gada decembris|0x00000620|0x00000007|4 baitu IDXSEG.|
|1999. gada janvāris|0x00000620|0x00000008|Jauns veidnes kolonnas formāts.|
|1999. gada jūnijs|0x00000620|0x00000009|Sakārtotas veidņu kolonnas. Izmanto operētājsistēmā Windows XP SP3|
||0x00000620|0x0000000b|Satur lapas galveni ar ECC kontrolsummuUsed in Exchange|
||0x00000620|0x0000000c|Izmantota operētājsistēmā Windows Vista (SP0)|
||0x00000620|0x00000011|Atbalsts 2 KiB, 16 KiB un 32 KiB lapām.Paplašināta lapas galvene ar papildu ECC kontrolsummām.Sleju saspiešana.Atstarpes padomi.Izmanto operētājsistēmā Windows 7 (SP0)|
|1999. gada maijs|0x00000623|0x00000000|Jauns telpas pārvaldnieks.|

### Datu bāzes faili

EDB datu bāzes failā ir visu datu bāzes tabulu shēma. Turklāt tajā ir iekļauti arī visu datu bāzes tabulu ieraksti un tabulu indeksi. Tās atrašanās vietu nosaka šādi identifikatori.

* JetCreateDatabase

* JetCreateDatabase2

* JetAttachDatabase

* JetAttachDatabase2


Pamatojoties uz tiem, datu bāzes stāvokli var novērtēt šādi.

|Vērtība|Identifier|Apraksts
---|---|---|
|1|JET_dbstateJustCreated|Datubāze tikko tika izveidota.|
|2|JET_dbstateDirtyShutdown|Lai datu bāze būtu lietojama vai pārvietojama, ir jāpalaiž cietā vai mīkstā atkopšana. Nevajadzētu mēģināt pārvietot datu bāzes šādā stāvoklī.|
|3|JET_dbstateCleanShutdown|Datu bāze ir tīrā stāvoklī. Datu bāzi var pievienot bez žurnālfailiem.|
|4|JET_dbstateBeingConverted|Datubāze tiek jaunināta.|
|5|JET_dbstateForceDetachInternal|Šī vērtība ir ieviesta operētājsistēmā WindowsXP|
 
## Atsauces
 * [Extensible Storage Engine (ESE) datu bāzes faila (EDB) specifikācijas](https://github.com/libyal/libesedb/tree/main/documentation)

