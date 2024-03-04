{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONE – „Microsoft OneNote“ failo formatas",
  "description": "Sužinokite apie VIENO failo formatą ir API, kurios gali sukurti ir atidaryti VIENĄ failus.",
  "linktitle": "ONE",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-on-lte"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra .ONE failas? ##

Failai, atstovaujami .ONE plėtiniu, sukurti naudojant Microsoft OneNote programą. OneNote leidžia rinkti informaciją naudojant programą taip, lyg naudodami juodraščio bloknotą užrašams darytumėte. OneNote failuose gali būti įvairių elementų, kuriuos galima įdėti į nefiksuotas dokumentų puslapių vietas. Šiuose elementuose gali būti teksto, suskaitmeninto rašysenos ir objektų, nukopijuotų iš kitų programų, įskaitant vaizdus, brėžinius ir daugialypės terpės (garso / vaizdo) klipus. Microsoft dabar siūlo internetinę OneNote versiją kaip Office365 dalį, kur pastabas galima bendrinti su kitais OneNote vartotojais internetu.

## .ONE failo formato specifikacijos ##

OneNote failo formatas yra efektyvus būdas pateikti skaitmeninius užrašus kaip hierarchinius sekcijų ir puslapių rinkinius. Kiekviename puslapyje yra vartotojo apibrėžtas turinys konkrečioje struktūroje, kad jis būtų vaizduojamas failo formato dokumento objekto modeliu (DOM). Šio formato duomenų modelis yra toks, kaip parodyta toliau.

### Struktūros apžvalga ###

Kaip parodyta OneNote failo formato duomenų modelyje, OneNote dokumentą sudaro skirtingi elementai.

#### Skyrius ####

Skyrius yra aukščiausias OneNote failo konteineris, kuriame dar yra įvairių elementų, pavyzdžiui:

* Puslapiai

* Metaduomenys

* Savybės


Metaduomenys ir ypatybės apima sekcijos pavadinimą, skiltyje esančių puslapių identifikaciją ir tų puslapių rodymo tvarką. Sąvoka sekcija reiškia visus puslapius, esančius skyriuje, ir tų duomenų atvaizdavimą OneNote® versijų saugyklos faile, kurio failo pavadinimo plėtinys yra .one.

#### Puslapis ####

Vartotojo nustatytas turinys OneNote dokumente yra puslapyje. Puslapio informacija apima tekstą, sąrašus, lenteles, puslapių pavadinimus, vaizdus ir pastabų žymas. Puslapį sudaro kontūro objektai, prie kurių pridedama dauguma esančių objektų. Kiekvienam puslapiui galima priskirti prasmingo vaizdavimo pavadinimą, o objektus taip pat galima pridėti tiesiogiai prie puslapių. Puslapyje taip pat gali būti antrinių puslapių hierarchinėje sistemoje.

#### Ypatybės ir ypatybių rinkiniai ####

OneNote turinį sudaro ypatybės, ypatybių rinkiniai ir failų duomenų objektai. Ypatybių rinkinys yra ypatybių rinkinys, atspindintis tam tikro tipo turinį. Failo duomenų objektas yra dvejetainių duomenų blokas, kuriame yra paveikslėlių, įterptųjų failų arba garso/vaizdo turinio.

#### OneNote bloknotas ####

Užrašinė yra tame pačiame kataloge saugomų skyrių failų rinkinys. Ypatybių rinkinys naudojamas tokiems parametrams kaip bloknoto sekcijų tvarka ir bloknoto spalva nurodyti.

### Failo struktūra ###

Versijų saugyklos failas PRIVALO prasidėti **Antraštės** struktūra. Likusi failo dalis yra padalinta į baitų blokus, kur kiekvieno bloko dydis ir struktūra nurodomi jį nurodančioje srityje. Blokas pasiekiamas, jei jį nurodo struktūra **Antraštė** arba laukas kitame pasiekiamame bloke. Duomenų, nepriklausančių **Antraštės** struktūrai, ir bet kokių pasiekiamų blokų BŪTINA nepaisyti.

Visos struktūros yra sulygiuotos ant 1 baito ribų. Visi sveikieji skaičiai yra pasirašyti, jei nenurodyta kitaip. Visi laukai yra [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), jei nenurodyta kitaip.

#### Antraštė ####

ONE failo antraštė susideda iš dalių, kuriose yra skirtingi unikalūs ID ir laukai, skirti failo informacijai pateikti, kaip nurodyta toliau:

`guidFileType (16 baitų): GUID, nurodantis versijų saugyklos failo tipą. PRIVALO būti viena iš toliau pateiktos lentelės reikšmių.


|Failo formatas | Reikšmė
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

guidFile (16 baitų): GUID, nurodantis šio versijų saugyklos failo tapatybę. TURI būti unikalus visame pasaulyje.

guidLegacyFileVersion (16 baitų): PRIVALO būti {00000000-0000-0000-0000-000000000000} ir PRIVALO būti ignoruojamas.

`guidFileFormat (16 baitų): GUID, nurodantis, kad failas yra versijų saugyklos failas. TURI būti {109ADD3F-911B-49F5-A5D0-1791EDC8AED8}.

ffvLastCodeThatWroteToThisFile (4 baitai): Nepaženklintas sveikasis skaičius. Priklausomai nuo failo tipo, PRIVALO būti viena iš reikšmių šioje lentelėje.

|Failo formatas | Reikšmė
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 baitai): sveikasis skaičius be ženklo. PRIVALO būti viena iš reikšmių šioje lentelėje, atsižvelgiant į šio failo failo formatą.


|Failo formatas | Reikšmė
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

ffvNewestCodeThatHasWrittenToThisFile (4 baitai): Nepaženklintas sveikasis skaičius. PRIVALO būti viena iš reikšmių šioje lentelėje, atsižvelgiant į šio failo failo formatą.

|Failo formatas | Reikšmė
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

ffvOldestCodeThatMayReadThisFile (4 baitai): Nepaženklintas sveikasis skaičius. PRIVALO būti viena iš reikšmių šioje lentelėje, atsižvelgiant į šio failo failo formatą.

|Failo formatas | Reikšmė
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 baitai): **FileChunkReference32** struktūra, kurios reikšmė PRIVALO būti fcrZero.

fcrLegacyTransactionLog (8 baitai): **FileChunkReference32** struktūra, kuri PRIVALO būti fcrNil.

cTransactionsInLog (4 baitai): nepasirašytas sveikasis skaičius, nurodantis operacijų skaičių operacijų žurnale. NETURI būti nulis.

`cbLegacyExpectedFileLength (4 baitai): sveikasis skaičius be ženklo, kuris PRIVALO būti nulis ir PRIVALO būti ignoruojamas.

rgbPlaceholder (8 baitai): Nepaženklintas sveikasis skaičius, kuris PRIVALO būti nulis ir PRIVALO būti ignoruojamas.

`fcrLegacyFileNodeListRoot (8 baitai): **FileChunkReference32** struktūra, kuri PRIVALO būti fcrNil.

`cbLegacyFreeSpaceInFreeChunkList (4 baitai): sveikasis skaičius be ženklo, kuris PRIVALO būti nulis ir PRIVALO būti ignoruojamas.

fNeedsDefrag (1 baitas): PRIVALO būti ignoruojamas.

fRepairedFile (1 baitas): PRIVALO būti ignoruojamas.

fNeedsGarbageCollect (1 baitas): PRIVALO būti ignoruojamas.

fHasNoEmbeddedFileObjects (1 baitas): Nepaženklintas sveikasis skaičius, kuris PRIVALO būti nulis ir PRIVALO būti ignoruojamas.

guidAncestor (16 baitų): GUID, nurodantis turinio failo lauką **Header.guidFile**, pateiktą šioje lentelėje:


|Turinio failo formatas|Turinio failo vieta
--- | --- |
|Sekcijos failas – .One|Turinio failas yra tame pačiame kataloge kaip ir šis failas.
|Turinio failas – .onetoc2|Turinio failas yra pirminiame šio failo kataloge.

Jei GUID yra 00000000-0000-0000-0000-000000000000}, šis laukas nenurodo turinio failo.

crcName (4 baitai): Nepaženklintas sveikasis skaičius, nurodantis šio versijų saugyklos failo pavadinimo CRC reikšmę. Pavadinimas yra unikodas failo pavadinimo su plėtiniu ir papildomu nuliniu simboliu pabaigoje. Šis CRC visada apskaičiuojamas naudojant .one failo CRC algoritmą, neatsižvelgiant į šio versijų saugyklos failo formatą.

`fcrHashedChunkList (12 baitų): **FileChunkReference64x32** struktūra, nurodanti nuorodą į pirmąjį **FileNodeListFragment** maišos dalių sąraše. Jei **FileChunkReference64x32** struktūros reikšmė yra fcrZero arba fcrNil, maišos dalių sąrašas neegzistuoja.

`fcrTransactionLog (12 baitų): **FileChunkReference64x32** struktūra, kuri nurodo nuorodą į pirmąją **TransactionLogFragment** struktūrą operacijų žurnale. Lauko **fcrTransactionLog** reikšmė NETURI būti fcrZero ir NETURI būti fcrNil.

`fcrFileNodeListRoot (12 baitų): **FileChunkReference64x32** struktūra, nurodanti nuorodą į šakninio failo mazgų sąrašą. Lauko **fcrFileNodeListRoot** reikšmė NETURI būti fcrZero ir NETURI būti fcrNil.

`fcrFreeChunkList (12 baitų): **FileChunkReference64x32** struktūra, nurodanti nuorodą į pirmąją **FreeChunkListFragment** struktūrą. Jei **FileChunkReference64x32** struktūros reikšmė yra fcrZero arba fcrNil, tada nemokamų dalių sąrašo nėra.

cbExpectedFileLength (8 baitai): Nepaženklintas sveikasis skaičius, nurodantis šio versijų saugyklos failo dydį baitais.

`cbFreeSpaceInFreeChunkList (8 baitai): sveikasis skaičius be ženklo, kuris TURI nurodyti laisvos vietos, nurodytos laisvų dalių sąraše, dydį baitais.

`guidFileVersion (16 baitų): GUID. Kai keičiama lauko **cTransactionsInLog** arba lauko **guidDenyReadFileVersion** reikšmė, **guidFileVersion** PRIVALO būti pakeistas į naują GUID.

nFileVersionGeneration (8 baitai): Nepaženklintas sveikasis skaičius, nurodantis, kiek kartų failas buvo pakeistas. PRIVALO būti padidintas, kai pasikeičia laukas **guidFileVersion**.

`guidDenyReadFileVersion (16 baitų): GUID. Kai keičiamas esamas failo turinys, išskyrus failo **Antraštės** struktūrą ir nenaudojamus saugojimo blokus, **guidDenyReadFileVersion** PRIVALO būti pakeistas į naują GUID.

grfDebugLogFlags (4 baitai): PRIVALO būti nulis. BŪTINA ignoruoti.

fcrDebugLog (12 baitų): **FileChunkReference64x32** struktūra, kurios reikšmė PRIVALO būti fcrZero. BŪTINA ignoruoti.

fcrAllocVerificationFreeChunkList (12 baitų): **FileChunkReference64x32** struktūra, kuri PRIVALO būti fcrZero. BŪTINA ignoruoti.

bnCreated (4 baitai): nepasirašytas sveikasis skaičius, nurodantis programos, sukūrusios šį versijų saugyklos failą, versijos numerį. TURI būti ignoruojamas.

bnLastWroteToThisFile (4 baitai): nepasirašytas sveikasis skaičius, nurodantis programos, kuri paskutinį kartą rašė į šį versijų saugyklos failą, versijos numerį. TURI būti ignoruojamas.

bnOldestWritten (4 baitai): Nepaženklintas sveikasis skaičius, nurodantis seniausios programos, kuri rašė į šį versijų saugyklos failą, versijos numerį. TURI būti ignoruojamas.

bnNewestWritten (4 baitai): Nepaženklintas sveikasis skaičius, nurodantis naujausios programos, kuri rašė į šį versijų saugyklos failą, versijos numerį. TURI būti ignoruojamas.

rgbReserved (728 baitai): PRIVALO būti nulis. BŪTINA ignoruoti.

## Nuorodos Nr.

* [[MS-ONESTORE] – „OneNote“ failo formatas](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote – Vikipedija](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


