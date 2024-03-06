{
  "date": "2019-12-03",
  "keywords": [
"doc",
"failu",
"pagarinājumu",
"faila formātā",
"Vārds",
"Dokuments"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOC — Microsoft Word dokumentu fails",
  "description": "Uzziniet par DOC faila formātu un API, kas var izveidot un atvērt DOC failus.",
  "linktitle": "DOC",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-do-lvc"
}
},
  "lastmod": "2019-12-03"
}

## Kas ir DOC fails?

Faili ar paplašinājumu .doc ir Microsoft Word vai citu tekstapstrādes dokumentu ģenerēti dokumenti binārā faila formātā. Sākotnēji paplašinājums tika izmantots vienkārša teksta dokumentācijai vairākās dažādās operētājsistēmās. Tas var saturēt dažādu veidu datus, piemēram, attēlus, formatētus, kā arī vienkāršu tekstu, grafikus, diagrammas, iegultos objektus, saites, lapas, lappušu formatējumu, drukas iestatījumus un daudz ko citu. Formāts bija populārs visu veidu dokumentācijai, jo tas lietotājiem piedāvā rokasgrāmatu, priekšlikumu, specifikāciju, CV, rakstu vai citu līdzīgu dokumentu rakstīšanas iespējas. Atjauninātā DOC versija ir [DOCX](/word-processing/docx/), kuras pamatā ir Office OpenXML, kuras specifikācijas ir atklāti pieejamas.

## Īsa vēsture ##

WordPerfect, a product of [Corel](https://www.corel.com/en/), used DOC as the extension of their proprietary format. In 1980s, WordPerfect remained the choice of usage on most of the computers due to its easy availability, conformance with most computer machines and Operating systems. However, WordPerfect saw its downfall on Windows OS when Microsoft introduced Microsoft Word as its product for documents file format and chose DOC extension for their proprietary format. As Microsoft Word became more and more popular, the DOC file format underwent several revisions from Microsoft Word 97 - 2003. Tas bija 2007. gads, kad noklusējuma DOC faila formāts tika aizstāts ar Office Open XML formātu (pazīstams kā DOCX), un jaunajās Microsoft Word versijās šis jaunais paplašinājums tagad tiek izmantots kā noklusējuma faila formāts.

## DOC faila formāta specifikācijas — vairāk informācijas

Microsoft didn't release the DOC file format specifications for a long time until 2008. In Feb 2008, format specifications were released for .doc file format under the Microsoft Open Specification Promise. Though the specification does not describe all of the features used by the DOC format, it gives ample information about the knowledge required to work with this file format. Still, reverse engineering is required to make use of the available information. The specifications have been updated several times and the latest [revision](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) is 8.0 which was updated as of August 2018.

### Daži pamatjēdzieni ###

Pirms mēs iedziļināmies detaļās par DOC faila formāta specifikācijām, ir jāsaprot daži pamatjēdzieni, lai strādātu ar šo faila formātu.

**Faila informācijas bāze (Fib):** Fib struktūra satur informāciju par dokumentu un norāda faila norādes uz dažādām daļām, kas veido dokumentu.
Fib ir mainīga garuma struktūra. Izņemot pamata daļu, kuras izmērs ir fiksēts, katras sadaļas priekšā ir skaitīšanas lauks, kas norāda nākamās sadaļas lielumu.

**Rakstzīmju pozīcija:** CP vai rakstzīmju pozīcija ir neparakstīts 32 bitu vesels skaitlis, kas dokumenta tekstā kalpo kā rakstzīmes indekss, kura pamatā ir nulles vērtība. Katras rakstzīmes atrašanās vietu un lielumu failā nevar izgūt tieši, un tas ir jāaprēķina, izmantojot iepriekš noteiktu algoritmu. Rakstzīmes ietver:

* Dokumenta teksts

* Objektu enkuri, piemēram, zemsvītras piezīmes vai tekstlodziņi

* Vadības rakstzīmes, piemēram, rindkopu atzīmes un tabulas šūnu atzīmes


**PLC:** PLC struktūra ir CP masīvs, kam seko datu elementu masīvs. Jebkura PLC datu elementiem ir jābūt vienādam ar nulli vai vairāk baitiem, un šī iemesla dēļ CP skaitam ir jābūt par vienu vairāk nekā datu elementu skaitam. PLC struktūras ir dažāda veida, kur katrs tips norāda, vai šim tipam ir atļauts dublēt CP. PLC struktūra sastāv no:

* **aCP (mainīgs garums):** CP elementu masīvs. Katrs **PLC** struktūras veids nosaka CP elementu nozīmi un atļauto diapazonu.

* **aData (mainīgs garums):** Katrs **PLC** struktūras veids nosaka datu elementu struktūru un nozīmi, visus datu elementu skaita ierobežojumus un visus tajos ietverto datu ierobežojumus. Tas arī norāda attiecības starp datu elementiem un atbilstošajiem CP.


**Derīga atlase:** .DOC failu konstrukcijas galvenokārt apraksta CP diapazons. Microsoft ir norādījis vairākus [rules](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx), kas šādā gadījumā jāievēro.

**STTB:** STTB ir virkņu tabula, kas sastāv no galvenes, kurai seko elementu masīvs. Vērtība **cData** norāda masīvā ietverto elementu skaitu.

**Īpašuma krātuve:** Word failā var būt dažādi elementi, piemēram, teksts, rindkopas, tabulas, attēli un sadaļas, kur katram var būt savi rekvizīti. To rekvizīti tiek saglabāti Word failā kā atšķirības no noklusējuma. Šādas atšķirības nosaka PRl, kas sastāv no viena īpašuma modifikatora (Sprm) un tā operanda. Lietojumprogramma var noteikt galīgo rekvizītu kopu, izmantojot **Prl** sarakstus.

**Aizsardzība ar paroli:** Word failus var aizsargāt arī ar paroli, kam var izmantot kādu no šiem mehānismiem.

* XOR apmulsināšana

* Biroja bināro dokumentu RC4 šifrēšana

* Office bināro dokumentu RC4 CryptoAPI šifrēšana


Ja gan FibBase.fEncrypted, gan FibBase.fObfuscation ir 1, fails tiek aizēnots, izmantojot XOR obfuscation.

Ja FibBase.fEncrypted ir 1 un FibBase.fObfuscation ir 0, fails tiek šifrēts, izmantojot Office Binary Document RC4 šifrēšanu vai Office Binary Document RC4 CryptoAPI šifrēšanu, un EncryptionHeader tiek glabāts pirmajā FibBase.lKey straumes Tablet baitos. EncryptionHeader.EncryptionVersionInfo norāda, kurš šifrēšanas mehānisms tika izmantots faila šifrēšanai.

### Faila struktūra ###

Binārais Word fails savā oriģinalitātē ir OLE salikts fails, kas sastāv no vairākām krātuvēm un straumēm. Šīm krātuvēm un straumēm ir sava struktūra un izmēri, kas nosaka rakstīšanas un lasīšanas parametrus. Šie ir:

#### WordDocument Stream ####

This stream contains the document text and other information referenced from other parts of the file. The stream has no predefined structure other than the FIB at the beginning which is mandatory and should be at offset 0. Šī straume nedrīkst būt lielāka par 2147 MB.

#### 1TableStream vai 0TableStream ####

Binārais Word fails var saturēt tabulas straumes, kas pazīstamas kā 1 tabulas straume vai 0 tabulas straume. Vismaz vienam no tiem jābūt dokumentā. Tomēr, ja dokumentā ir gan straumes 1Table, gan 0Table, tiek izmantota tikai straume, uz kuru atsaucas base.fWhichTblStm. Straume bez atsauces ir OBLIGĀTI jāignorē.
Tabulas straume NEDRĪKST būt lielāka par 2147 MB.

#### Datu straume ####

Datu straumei nav iepriekš noteiktas struktūras. Tajā ir dati, uz kuriem ir atsauces no FIB vai citām faila daļām. Šai straumei nav jābūt klāt, ja uz to nav atsauces. Datu straume NEDRĪKST būt lielāka par 2147 MB.

#### Objektu baseina krātuve ####

Objektu pūla krātuvē ir iegulto OLE objektu krātuves. Šai krātuvei nav jābūt, ja dokumentā nav iegultu OLE objektu.

#### Pielāgota XML datu krātuve ####

Pielāgotā XML datu krātuve ir izvēles krātuve, kuras nosaukumam OBLIGĀTI ir jābūt MsoDataStore.

#### Kopsavilkuma informācijas straume ####

Kopsavilkuma informācijas straume ir neobligāta straume, kuras nosaukumam OBLIGĀTI ir jābūt \005SummaryInformation, kur \005 ir rakstzīme ar vērtību 0x0005, nevis virknes burts \005.

#### Dokumentu kopsavilkuma informācijas straume ####

Dokumenta kopsavilkuma informācijas straume ir neobligāta straume, kuras nosaukumam OBLIGĀTI ir jābūt \005DocumentSummaryInformation, kur \005 ir rakstzīme ar vērtību 0x0005, nevis virknes burts \005.

#### Šifrēšanas straume

Šifrēšanas straume ir izvēles straume, kuras nosaukumam OBLIGĀTI ir jābūt šifrēšana. Šī straume NEDRĪKST būt, ja nav izpildīti abi tālāk minētie nosacījumi.

* Dokuments ir šifrēts ar Office Binary Document RC4 CryptoAPI šifrēšanu.

* fDocProps vērtība ir iestatīta mapē EncryptionHeader.Flags.


#### Makro krātuve

Makro krātuve ir izvēles krātuve, kurā ir faila makro. Ja tāda ir, tai OBLIGĀTI ir jābūt projekta saknes krātuvei.

#### XML parakstu glabāšana

XML parakstu krātuve ir izvēles krātuve, kuras nosaukumam OBLIGĀTI ir \_xmlsignatures.

#### Parakstu straume

Parakstu straume ir neobligāta straume, kuras nosaukumam OBLIGĀTI ir \_signatures. Šajā straumē ir ciparparaksti.

#### Informācijas tiesību pārvaldība Datu telpas glabāšana

Informācijas tiesību pārvaldības datu telpas krātuve ir izvēles krātuve, kuras nosaukumam OBLIGĀTI ir \006DataSpaces, kur \006 ir rakstzīme ar vērtību 0x0006, nevis virknes burts \006. Ja šī krātuve ir pieejama, OBLIGĀTI ir jābūt arī aizsargātā satura straumei.
Ja šī krātuve ir pieejama, visas norādītās straumes un krātuves, izņemot šo krātuvi un aizsargātā satura straumi, JĀLASA no aizsargātā satura straumes, kā norādīts [MS-OFFCRYPTO], un ja kāda no šīm straumēm un krātuvēm pastāv ārpus aizsargātā satura. Straumējiet, tie būtu jāignorē.

#### Aizsargāta satura straume

Aizsargātā satura straume ir neobligāta straume, kuras nosaukumam OBLIGĀTI ir jābūt \009DRMContent, kur \009 ir rakstzīme ar vērtību 0x0009, nevis virknes burts \009.
Ja šī straume ir pieejama, OBLIGĀTI ir jābūt arī informācijas tiesību pārvaldības datu telpas krātuvei.

## Atsauces Nr.

* [MS-DOC failu veidošanas specifikācijas](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)

* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))


