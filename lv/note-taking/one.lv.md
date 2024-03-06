{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONE — Microsoft OneNote faila formāts",
  "description": "Uzziniet par VIENU faila formātu un API, kas var izveidot un atvērt VIENU failu.",
  "linktitle": "ONE",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-on-lve"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir .ONE fails? ##

Failus, kas apzīmēti ar paplašinājumu .ONE, izveido lietojumprogramma Microsoft OneNote. OneNote ļauj apkopot informāciju, izmantojot lietojumprogrammu, it kā jūs izmantotu melnrakstu bloknotu piezīmju veikšanai. OneNote faili var saturēt dažādus elementus, kurus var novietot nefiksētās vietās dokumentu lapās. Šajos elementos var būt teksts, digitalizēts rokraksts un objekti, kas kopēti no citām lietojumprogrammām, tostarp attēli, zīmējumi un multivides (audio/video) klipi. Microsoft tagad piedāvā OneNote tiešsaistes versiju kā daļu no Office365, kur piezīmes var koplietot ar citiem OneNote lietotājiem internetā.

## .ONE faila formāta specifikācijas ##

OneNote faila formāts nodrošina efektīvu veidu, kā attēlot digitālās piezīmes kā hierarhiskas sadaļu un lapu kopas. Katrā lapā ir lietotāja definēts saturs īpašā struktūrā, kas tiek attēlots ar faila formātu Document Object Model (DOM). Šī formāta datu modelis ir tāds, kā parādīts tālāk.

### Struktūras pārskats ###

Kā parādīts OneNote faila formāta datu modelī, OneNote dokuments sastāv no dažādiem elementiem.

#### Sadaļa ####

Sadaļa ir OneNote faila augstākais konteiners, kurā ir arī dažādi elementi, piemēram:

* Lapas

* Metadati

* Īpašības


Metadati un rekvizīti ietver sadaļas nosaukumu, sadaļā ietverto lapu identifikāciju un secību, kādā šīs lapas parādās. Termins sadaļa attiecas uz visām lapām, kas atrodas sadaļā, un šo datu attēlojumu OneNote® versiju krātuves failā, kuram ir .one faila nosaukuma paplašinājums.

#### Lappuse ####

Lietotāja definēts saturs OneNote dokumentā ir ietverts lapā. Lapas informācija ietver tekstu, sarakstus, tabulas, lappušu nosaukumus, attēlus un piezīmju atzīmes. Lapa sastāv no kontūru objektiem, kuriem tiek pievienota lielākā daļa ietverto objektu. Katrai lapai var piešķirt nosaukumu jēgpilnam attēlojumam, kā arī objektus var pievienot tieši lapām. Lapā var būt arī apakšlapas hierarhiskā sistēmā.

#### Rekvizīti un rekvizītu kopas ####

OneNote saturs sastāv no rekvizītiem, rekvizītu kopām un failu datu objektiem. Rekvizītu kopa ir rekvizītu kolekcija, kas atspoguļo noteikta veida saturu. Faila datu objekts ir bināro datu bloks, kas satur attēlus, iegultos failus vai audio/video saturu.

#### OneNote piezīmju grāmatiņa ####

Piezīmju grāmatiņa ir sadaļu failu kolekcija, kas tiek glabāta vienā direktorijā. Rekvizītu kolekcija tiek izmantota, lai norādītu iestatījumus, piemēram, piezīmju grāmatiņas sadaļu secību un piezīmju grāmatiņas krāsu.

### Faila struktūra ###

Versiju krātuves failam OBLIGĀTI jāsākas ar struktūru **Galvene**. Pārējā faila daļa ir sadalīta baitu blokos, kur katra bloka lielums un struktūra tiek norādīta laukā, kas uz to atsaucas. Bloks ir sasniedzams, ja uz to atsaucas struktūra **Header** vai ja uz to atsaucas lauks citā sasniedzamā blokā. Dati, kas atrodas ārpus **Galvenes** struktūras, un visi sasniedzamie bloki OBLIGĀTI ir jāignorē.

Visas struktūras ir izlīdzinātas uz 1 baita robežām. Visi veseli skaitļi ir parakstīti, ja vien nav norādīts citādi. Visi lauki ir [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), ja vien nav norādīts citādi.

#### Virsraksts ####

ONE faila galvene sastāv no daļām, kurās ir dažādi unikāli ID un lauki faila informācijas attēlošanai, kā norādīts tālāk.

`guidFileType (16 baiti): GUID, kas norāda versiju krātuves faila veidu. OBLIGĀTI ir jābūt vienai no vērtībām no tālāk esošās tabulas.


|Faila formāts|Vērtība
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 baiti): GUID, kas norāda šī versiju krātuves faila identitāti. JĀBŪT globāli unikālam.

`guidLegacyFileVersion (16 baiti):` OBLIGĀTI ir {00000000-0000-0000-0000-000000000000} un OBLIGĀTI jāignorē.

`guidFileFormat (16 baiti): GUID, kas norāda, ka fails ir versiju krātuves fails. JĀBŪT {109ADD3F-911B-49F5-A5D0-1791EDC8AED8}”.

`ffvLastCodeThatWroteToThisFile (4 baiti): vesels skaitlis bez paraksta. Atkarībā no faila veida OBLIGĀTI ir jābūt vienai no vērtībām šajā tabulā.

|Faila formāts|Vērtība
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 baiti): neparakstīts vesels skaitlis. OBLIGĀTI ir jābūt vienai no vērtībām šajā tabulā atkarībā no šī faila faila formāta.


|Faila formāts|Vērtība
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 baiti): neparakstīts vesels skaitlis. OBLIGĀTI ir jābūt vienai no vērtībām šajā tabulā atkarībā no šī faila faila formāta.

|Faila formāts|Vērtība
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

ffvOldestCodeThatMayReadThisFile (4 baiti): Neparakstīts vesels skaitlis. OBLIGĀTI ir jābūt vienai no vērtībām šajā tabulā atkarībā no šī faila faila formāta.

|Faila formāts|Vērtība
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 baiti): **FileChunkReference32** struktūra, kuras vērtībai OBLIGĀTI jābūt fcrZero”.

`fcrLegacyTransactionLog (8 baiti): **FileChunkReference32** struktūra, kurai OBLIGĀTI ir jābūt fcrNil”.

`cTransactionsInLog (4 baiti): neparakstīts vesels skaitlis, kas norāda darījumu skaitu darījumu žurnālā. NEDRĪKST būt nulle.

`cbLegacyExpectedFileLength (4 baiti): neparakstīts vesels skaitlis, kam OBLIGĀTI ir jābūt nullei un OBLIGĀTI jāignorē.

rgbPlaceholder (8 baiti): neparakstīts vesels skaitlis, kam OBLIGĀTI ir jābūt nullei un OBLIGĀTI jāignorē.

`fcrLegacyFileNodeListRoot (8 baiti): **FileChunkReference32** struktūra, kurai OBLIGĀTI ir jābūt fcrNil.

`cbLegacyFreeSpaceInFreeChunkList (4 baiti): neparakstīts vesels skaitlis, kam OBLIGĀTI ir jābūt nullei un OBLIGĀTI jāignorē.

`fNeedsDefrag (1 baits):' OBLIGĀTI jāignorē.

`fRepairedFile (1 baits): OBLIGĀTI ir jāignorē.

`fNeedsGarbageCollect (1 baits): OBLIGĀTI ir jāignorē.

`fHasNoEmbeddedFileObjects (1 baits): neparakstīts vesels skaitlis, kam OBLIGĀTI ir jābūt nullei un OBLIGĀTI jāignorē.

`guidAncestor (16 baiti): GUID, kas norāda satura rādītāja faila lauku **Header.guidFile**, kas norādīts šajā tabulā:


|Satura rādītāja faila formāts|Satura rādītāja faila atrašanās vieta
--- | --- |
|Sadaļas fails - .One|Satura rādītāja fails atrodas tajā pašā direktorijā, kur šis fails.
|Satura rādītāja fails — .onetoc2|Satura rādītāja fails atrodas šī faila vecākdirektorijā.

Ja GUID ir 00000000-0000-0000-0000-000000000000}, šajā laukā nav atsauces uz satura rādītāja failu.

`crcName (4 baiti): neparakstīts vesels skaitlis, kas norāda šī versiju krātuves faila nosaukuma CRC vērtību. Nosaukums ir faila nosaukuma unikoda attēlojums ar paplašinājumu un papildu nulles rakstzīmi beigās. Šis CRC vienmēr tiek aprēķināts, izmantojot CRC algoritmu .one failam neatkarīgi no šī versiju krātuves faila formāta.

`fcrHashedChunkList (12 baiti): **FileChunkReference64x32** struktūra, kas norāda atsauci uz pirmo **FileNodeListFragment** jauktā gabalu sarakstā. Ja struktūras **FileChunkReference64x32** vērtība ir fcrZero vai fcrNil, jauktais gabalu saraksts nepastāv.

`fcrTransactionLog (12 baiti): **FileChunkReference64x32** struktūra, kas norāda atsauci uz pirmo **TransactionLogFragment** struktūru darījumu žurnālā. Lauka **fcrTransactionLog** vērtība NEDRĪKST būt fcrZero un NEDRĪKST būt fcrNil.

`fcrFileNodeListRoot (12 baiti): **FileChunkReference64x32** struktūra, kas norāda atsauci uz saknes faila mezglu sarakstu. Lauka **fcrFileNodeListRoot** vērtība NEDRĪKST būt fcrZero un NEDRĪKST būt fcrNil.

`fcrFreeChunkList (12 baiti): **FileChunkReference64x32** struktūra, kas norāda atsauci uz pirmo **FreeChunkListFragment** struktūru. Ja struktūras **FileChunkReference64x32** vērtība ir fcrZero vai fcrNil, tad bezmaksas gabalu saraksts nepastāv.

`cbExpectedFileLength (8 baiti): neparakstīts vesels skaitlis, kas norāda šī versiju krātuves faila lielumu baitos.

`cbFreeSpaceInFreeChunkList (8 baiti): neparakstīts vesels skaitlis, kam BŪTU jānorāda brīvās vietas lielums, kas norādīts brīvo daļu sarakstā.

`guidFileVersion (16 baiti): GUID. Ja tiek mainīta lauka **cTransactionsInLog** vai **guidDenyReadFileVersion** vērtība, **guidFileVersion** OBLIGĀTI jāmaina uz jaunu GUID.

`nFileVersionGeneration (8 baiti): neparakstīts vesels skaitlis, kas norāda, cik reižu fails ir mainīts. OBLIGĀTI jāpalielina, mainoties laukam **guidFileVersion**.

`guidDenyReadFileVersion (16 baiti): GUID. Kad tiek mainīts esošais faila saturs, izņemot faila **Header** struktūru un neizmantotos krātuves blokus, **guidDenyReadFileVersion** OBLIGĀTI jāmaina uz jaunu GUID.

`grfDebugLogFlags (4 baiti): OBLIGĀTI ir nulle. OBLIGĀTI jāignorē.

`fcrDebugLog (12 baiti): **FileChunkReference64x32** struktūra, kurai OBLIGĀTI ir jābūt vērtībai fcrZero. OBLIGĀTI jāignorē.

`fcrAllocVerificationFreeChunkList (12 baiti): **FileChunkReference64x32** struktūra, kurai OBLIGĀTI ir jābūt fcrZero. OBLIGĀTI jāignorē.

`bnCreated (4 baiti): neparakstīts vesels skaitlis, kas norāda lietojumprogrammas būvējuma numuru, kas izveidoja šo versiju krātuves failu. IR jāignorē.

bnLastWroteToThisFile (4 baiti): neparakstīts vesels skaitlis, kas norāda lietojumprogrammas būvējuma numuru, kas pēdējo reizi ierakstīja šajā versiju krātuves failā. IR jāignorē.

bnOldestWritten (4 baiti): neparakstīts vesels skaitlis, kas norāda vecākās lietojumprogrammas būvējuma numuru, kas ierakstīja šajā versiju krātuves failā. IR jāignorē.

bnNewestWritten (4 baiti): neparakstīts vesels skaitlis, kas norāda jaunākās lietojumprogrammas būvējuma numuru, kas ierakstīja šajā versiju krātuves failā. IR jāignorē.

rgbReserved (728 baiti): OBLIGĀTI ir jābūt nullei. OBLIGĀTI jāignorē.

## Atsauces Nr.

* [[MS-ONESTORE] — OneNote faila formāts](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote — Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


