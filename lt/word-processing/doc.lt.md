{
  "date": "2019-12-03",
  "keywords": [
"doc",
"failą",
"pratęsimas",
"Dokumento formatas",
"Žodis",
"dokumentas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOC – „Microsoft Word“ dokumento failas",
  "description": "Sužinokite apie DOC failo formatą ir API, kurios gali kurti ir atidaryti DOC failus.",
  "linktitle": "DOC",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-do-ltc"
}
},
  "lastmod": "2019-12-03"
}

## Kas yra DOC failas?

Failai su plėtiniu .doc yra dokumentai, sukurti naudojant Microsoft Word arba kitus teksto apdorojimo dokumentus dvejetainiu failo formatu. Iš pradžių plėtinys buvo naudojamas paprasto teksto dokumentacijai keliose skirtingose operacinėse sistemose. Jame gali būti kelių skirtingų tipų duomenų, tokių kaip vaizdai, suformatuoti, taip pat paprastas tekstas, grafikai, diagramos, įterptieji objektai, nuorodos, puslapiai, puslapio formatavimas, spausdinimo nustatymai ir daug kitų. Šis formatas buvo populiarus visų rūšių dokumentacijai dėl daugybės galimybių, kurias jis siūlo vartotojams rašant vadovus, pasiūlymus, specifikacijas, gyvenimo aprašymus, straipsnius ar bet kokius panašius dokumentus. Atnaujinta DOC versija yra [DOCX](/word-processing/docx/), pagrįsta Office OpenXML, kurios specifikacijos yra atvirai prieinamos.

## Trumpa istorija ##

WordPerfect, a product of [Corel](https://www.corel.com/en/), used DOC as the extension of their proprietary format. In 1980s, WordPerfect remained the choice of usage on most of the computers due to its easy availability, conformance with most computer machines and Operating systems. However, WordPerfect saw its downfall on Windows OS when Microsoft introduced Microsoft Word as its product for documents file format and chose DOC extension for their proprietary format. As Microsoft Word became more and more popular, the DOC file format underwent several revisions from Microsoft Word 97 - 2003. Tai buvo 2007 m., kai numatytasis DOC failo formatas buvo pakeistas Office Open XML formatu (žinomu kaip DOCX), o naujosios Microsoft Word versijos dabar naudoja šį naują plėtinį kaip numatytąjį failo formatą.

## DOC failo formato specifikacijos – daugiau informacijos

Microsoft didn't release the DOC file format specifications for a long time until 2008. In Feb 2008, format specifications were released for .doc file format under the Microsoft Open Specification Promise. Though the specification does not describe all of the features used by the DOC format, it gives ample information about the knowledge required to work with this file format. Still, reverse engineering is required to make use of the available information. The specifications have been updated several times and the latest [revision](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) is 8.0 which was updated as of August 2018.

### Kai kurios pagrindinės sąvokos ###

Prieš pradedant bet kokią informaciją apie DOC failo formato specifikacijas, norint dirbti su šiuo failo formatu, reikia suprasti kai kurias pagrindines sąvokas.

**Failo informacijos bazė (Fib):** Fib struktūroje pateikiama informacija apie dokumentą ir nurodomos failo rodyklės į įvairias dokumentą sudarančias dalis.
Fib yra kintamo ilgio struktūra. Išskyrus bazinę dalį, kurios dydis yra fiksuotas, prieš kiekvieną skyrių pateikiamas skaičiavimo laukas, nurodantis kitos sekcijos dydį.

**Simbolio padėtis:** CP arba simbolio padėtis reiškia beženklį 32 bitų sveikąjį skaičių, kuris dokumento tekste naudojamas kaip nulinis simbolio indeksas. Kiekvieno simbolio vietos ir dydžio faile negalima gauti tiesiogiai, todėl juos reikia apskaičiuoti naudojant iš anksto nurodytą algoritmą. Veikėjai apima:

* Dokumento tekstas

* Objektų, tokių kaip išnašos ar teksto laukeliai, inkarai

* Valdymo simboliai, pvz., pastraipų ir lentelės langelių ženklai


**PLC:** PLC struktūra yra CP masyvas, po kurio seka duomenų elementų masyvas. Bet kurio PLC duomenų elementai turi būti tokio pat dydžio – nulis arba daugiau baitų, todėl CP skaičius turi būti vienu daugiau nei duomenų elementų skaičius. PLC struktūros yra skirtingų tipų, kur kiekvienas tipas nurodo, ar tam tipui leidžiami pasikartojantys CP, ar ne. PLC struktūrą sudaro:

* **aCP (kintamo ilgio):** CP elementų masyvas. Kiekvienas **PLC** struktūros tipas nurodo CP elementų reikšmę ir leistiną diapazoną.

* **aData (kintamo ilgio):** Kiekvienas **PLC** struktūros tipas nurodo duomenų elementų struktūrą ir reikšmę, bet kokius duomenų elementų skaičiaus ir juose esančių duomenų apribojimus. Taip pat nurodomas ryšys tarp duomenų elementų ir atitinkamų CP.


**Tinkamas pasirinkimas:** .DOC failo konstrukcijos daugiausia apibūdinamos įvairiais CP. Microsoft nurodo keletą [rules](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx), kurių reikia laikytis tokiu atveju.

**STTB:** STTB yra eilučių lentelė, sudaryta iš antraštės, po kurios seka elementų masyvas. **cData** reikšmė nurodo elementų, esančių masyve, skaičių.

**Nuosavybės saugykla:** Word faile gali būti įvairių elementų, tokių kaip tekstas, pastraipos, lentelės, paveikslėliai ir skyriai, kur kiekvienas gali turėti savo ypatybes. Jų savybės yra saugomos Word faile kaip skirtumai nuo numatytosios. Tokius skirtumus nurodo PRl, susidedantis iš vieno ypatybės modifikatoriaus (Sprm) ir jo operando. Programa gali nustatyti galutinį savybių rinkinį taikydama **Prl** sąrašus.

**Apsauga slaptažodžiu:** Word failai taip pat gali būti apsaugoti slaptažodžiu, kuriam galima naudoti vieną iš šių mechanizmų.

* XOR užtemimas

* Biuro dvejetainių dokumentų RC4 šifravimas

* Office dvejetainis dokumentas RC4 CryptoAPI šifravimas


Jei FibBase.fEncrypted ir FibBase.fObfuscation yra 1, failas užtemdytas naudojant XOR užmaskavimą.

Jei FibBase.fEncrypted yra 1, o FibBase.fObfuscation yra 0, failas užšifruojamas naudojant Office Binary Document RC4 Encryption arba Office Binary Document RC4 CryptoAPI šifravimą, o EncryptionHeader saugomas pirmajame T FibBase.lKey sraute. EncryptionHeader.EncryptionVersionInfo nurodo, kuris šifravimo mechanizmas buvo naudojamas failui užšifruoti.

### Failo struktūra ###

Dvejetainis Word failas savo originalumu yra OLE sudėtinis failas, kurį sudaro kelios saugyklos ir srautai. Šios saugyklos ir srautai turi savo struktūrą ir dydžius, kurie nurodo rašymo ir skaitymo parametrus. Šitie yra:

#### WordDocument Stream ####

This stream contains the document text and other information referenced from other parts of the file. The stream has no predefined structure other than the FIB at the beginning which is mandatory and should be at offset 0. Šis srautas neturi būti didesnis nei 2147 MB.

#### 1TableStream arba 0TableStream ####

Dvejetainiame Word faile gali būti lentelės srautų, žinomų kaip 1 lentelės srautas arba 0 lentelės srautas. Dokumente turi būti bent vienas iš jų. Tačiau jei dokumente yra ir 1Table, ir 0Table srautai, naudojamas tik base.fWhichTblStm nurodytas srautas. Nenurodytas srautas PRIVALO būti ignoruojamas.
Lentelės srautas NETURI būti didesnis nei 2147 MB.

#### Duomenų srautas ####

Duomenų srautas neturi iš anksto nustatytos struktūros. Jame yra duomenys, nurodyti iš FIB arba iš kitų failo dalių. Šis srautas nebūtinai turi būti, jei į jį nėra nuorodų. Duomenų srautas NETURI būti didesnis nei 2147 MB.

#### Objektų baseino saugykla ####

Objektų telkinio saugykloje yra įterptųjų OLE objektų saugyklos. Šios saugyklos nebūtina, jei dokumente nėra įterptų OLE objektų.

#### Tinkinta XML duomenų saugykla ####

Pasirinktinė XML duomenų saugykla yra pasirenkama saugykla, kurios pavadinimas TURI būti MsoDataStore.

#### Suvestinės informacijos srautas ####

Suvestinės informacijos srautas yra pasirenkamas srautas, kurio pavadinimas PRIVALO būti \005SummaryInformation, kur \005 yra simbolis, kurio vertė yra 0x0005, o ne eilutės raidė \005.

#### Dokumento suvestinės informacijos srautas ####

Dokumento suvestinės informacijos srautas yra pasirenkamas srautas, kurio pavadinimas PRIVALO būti \005DocumentSummaryInformation, kur \005 yra simbolis, kurio vertė yra 0x0005, o ne eilutės raidė \005.

#### Šifravimo srautas

Šifravimo srautas yra pasirenkamas srautas, kurio pavadinimas PRIVALO būti šifravimas. Šis srautas NETURI būti, nebent tenkinamos abi toliau nurodytos sąlygos:

* Dokumentas užšifruotas naudojant Office Binary Document RC4 CryptoAPI šifravimą.

* „fDocProps“ reikšmė nustatoma EncryptionHeader.Flags.


#### Makrokomandų saugykla

Makrokomandų saugykla yra pasirenkama saugykla, kurioje yra failo makrokomandos. Jei yra, tai TURI būti projekto šakninė saugykla.

#### XML parašų saugykla

XML parašų saugykla yra pasirenkama saugykla, kurios pavadinimas PRIVALO būti \_xmlsignatures.

#### Parašų srautas

Parašų srautas yra pasirenkamas srautas, kurio pavadinimas PRIVALO būti \_signatures. Šiame sraute yra skaitmeninių parašų.

#### Informacijos teisių valdymas Duomenų erdvės saugykla

Informacijos teisių valdymo duomenų erdvės saugykla yra pasirenkama saugykla, kurios pavadinimas PRIVALO būti \006DataSpaces, kur \006 yra simbolis, kurio reikšmė yra 0x0006, o ne eilutės raidė \006. Jei ši saugykla yra, saugomo turinio srautas taip pat PRIVALO būti.
Jei ši saugykla yra, visi nurodyti srautai ir saugyklos, išskyrus šią saugyklą ir apsaugoto turinio srautą, TURI būti nuskaitomi iš saugomo turinio srauto, kaip nurodyta [MS-OFFCRYPTO] ir jei kuris nors iš tų srautų ir saugyklų yra už saugomo turinio ribų. Srautas, jie TURI būti ignoruojami.

#### Apsaugotas turinio srautas

Apsaugoto turinio srautas yra pasirenkamas srautas, kurio pavadinimas PRIVALO būti \009DRMContent, kur \009 yra simbolis, kurio vertė yra 0x0009, o ne eilutės raidė \009.
Jei šis srautas yra, PRIVALO būti ir informacijos teisių valdymo duomenų erdvės saugykla.

## Nuorodos Nr.

* [MS-DOC failų formavimo specifikacijos](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)

* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))


