{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Format de fișier Microsoft OneNote",
  "description":"Aflați despre ONE format de fișier și API-urile care pot crea și deschide ONE fișiere.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier .ONE? ##

Fișierul reprezentat de extensia .ONE este creat de aplicația Microsoft OneNote. OneNote vă permite să culegeți informații utilizând aplicația ca și cum ați folosi blocul de schiță pentru a lua note. Fișierele OneNote pot conține diferite elemente care pot fi plasate în locații nefixate pe paginile documentului. Aceste elemente pot conține text, scris de mână digitizat și obiecte copiate din alte aplicații, inclusiv imagini, desene și clipuri multimedia (audio/video). Microsoft oferă acum versiunea online a OneNote ca parte a Office365, unde notele pot fi partajate cu alți utilizatori OneNote pe internet.

## Specificații de format de fișier .ONE ##

Formatul de fișier OneNote oferă o modalitate eficientă de reprezentare a notelor digitale ca seturi ierarhice de secțiuni și pagini. Fiecare pagină conține conținut definit de utilizator într-o structură specifică pentru reprezentare prin formatul de fișier Document Object Model (DOM). Modelul de date pentru acest format este ilustrat mai jos.

### Prezentare generală a structurii ###

După cum este ilustrat în modelul de date pentru formatul de fișier OneNote, un document OneNote constă din elemente diferite.

#### Secțiune ####

O secțiune este cel mai de sus container dintr-un fișier OneNote care conține în plus diferite elemente, cum ar fi:

* Pagini
* Metadate
* Proprietăți

Metadatele și proprietățile includ numele secțiunii, identificarea paginilor care sunt conținute în secțiune și ordinea în care apar acele pagini. Termenul „secțiune” se referă la toate paginile care se află într-o secțiune și la reprezentarea acelor date într-un fișier de stocare a versiunilor OneNote®, care are extensia de nume de fișier .one.

#### Pagina ####

Conținutul definit de utilizator într-un document OneNote este conținut în interiorul unei pagini. Informațiile despre pagină includ text, liste, tabele, titluri de pagini, imagini și etichete de note. O pagină constă din obiecte de contur la care se adaugă majoritatea obiectelor conținute. Fiecărei pagini i se poate atribui un nume pentru o reprezentare semnificativă, iar obiectele pot fi adăugate direct în pagini. O pagină mai poate conține subpagini într-un sistem ierarhic.

#### Proprietăți și seturi de proprietăți ####

Conținutul OneNote este format din proprietăți, seturi de proprietăți și obiecte de date fișier. Un set de proprietăți este o colecție de proprietăți care reprezintă un anumit tip de conținut. Un obiect de date fișier este un bloc de date binare care conține imagini, fișiere încorporate sau conținut audio/video.

#### Notebook OneNote ####

Un blocnotes este o colecție de fișiere secțiuni care sunt stocate în același director. O colecție de proprietăți este utilizată pentru a specifica setări, cum ar fi ordinea secțiunilor din blocnotes și culoarea blocnotesului.

### Structura fișierului ###

Un fișier de stocare a reviziilor TREBUIE să înceapă cu o structură **Header**. Restul fișierului este împărțit în blocuri de octeți, unde dimensiunea și structura fiecărui bloc sunt specificate de câmpul care face referire la el. Un bloc este accesibil dacă este referit de structura **Header** sau dacă este referit de un câmp dintr-un alt bloc accesibil. Datele din afara structurii **Header** și orice blocuri accesibile TREBUIE ignorate.

Toate structurile sunt aliniate pe granițele de 1 octet. Toate numerele întregi sunt semnate, dacă nu se specifică altfel. Toate câmpurile sunt [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), dacă nu se specifică altfel.

#### Antet ####

Antetul fișierului .ONE este format din bucăți care conțin diferite ID-uri și câmpuri unice pentru reprezentarea informațiilor despre fișier, după cum urmează:

`guidFileType (16 octeți):` Un GUID care specifică tipul fișierului de stocare a reviziilor. TREBUIE să fie una dintre valorile din tabelul următor.


|Format fișier|Valoare
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` Un GUID care specifică identitatea acestui fișier de stocare a versiunilor. TREBUIE să fie unic la nivel global.

`guidLegacyFileVersion (16 bytes):` TREBUIE să fie „{00000000-0000-0000-0000-000000000000}” și TREBUIE ignorat.

`guidFileFormat (16 bytes):` Un GUID care specifică faptul că fișierul este un fișier de stocare a reviziilor. TREBUIE să fie „{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}”.

`ffvLastCodeThatWroteToThisFile (4 octeți):` Un întreg fără semn. TREBUIE să fie una dintre valorile din următorul tabel, în funcție de tipul fișierului.

|Format fișier|Valoare
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bytes):` Un întreg fără semn. TREBUIE să fie una dintre valorile din următorul tabel, în funcție de formatul de fișier al acestui fișier.


|Format fișier|Valoare
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` Un întreg fără semn. TREBUIE să fie una dintre valorile din următorul tabel, în funcție de formatul de fișier al acestui fișier.

|Format fișier|Valoare
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Un întreg fără semn. TREBUIE să fie una dintre valorile din următorul tabel, în funcție de formatul de fișier al acestui fișier.

|Format fișier|Valoare
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bytes):` O structură **FileChunkReference32** care TREBUIE să aibă valoarea „fcrZero”.

`fcrLegacyTransactionLog (8 octeți):` O structură **FileChunkReference32** care TREBUIE să fie „fcrNil”.

`cTransactionsInLog (4 bytes):` Un număr întreg nesemnat care specifică numărul de tranzacții din jurnalul de tranzacții. NU TREBUIE să fie zero.

`cbLegacyExpectedFileLength (4 octeți):` Un întreg fără semn care TREBUIE să fie zero și TREBUIE ignorat.

`rgbPlaceholder (8 bytes):` Un întreg fără semn care TREBUIE să fie zero și TREBUIE ignorat.

`fcrLegacyFileNodeListRoot (8 bytes):` O structură **FileChunkReference32** care TREBUIE să fie „fcrNil”.

`cbLegacyFreeSpaceInFreeChunkList (4 bytes):` Un întreg fără semn care TREBUIE să fie zero și TREBUIE ignorat.

`fNeedsDefrag (1 octet):` TREBUIE ignorat.

`fRepairedFile (1 octet):` TREBUIE ignorat.

`fNeedsGarbageCollect (1 octet):` TREBUIE ignorat.

`fHasNoEmbeddedFileObjects (1 octet):` Un întreg fără semn care TREBUIE să fie zero și TREBUIE ignorat.

`guidAncestor (16 octeți):` Un GUID care specifică câmpul **Header.guidFile** din fișierul de cuprins, dat de următorul tabel:


|Format fișier Cuprins|Locația fișierului Cuprins
--- | --- |
|Fișier de secțiune - .One|Fișierul de cuprins se află în același director cu acest fișier.
|Fișier Cuprins - .onetoc2|Fișierul Cuprins se află în directorul părinte al acestui fișier.

Dacă GUID-ul este {00000000-0000-0000-0000-000000000000}, acest câmp nu face referire la un fișier de cuprins.

`crcName (4 bytes):` Un întreg nesemnat care specifică valoarea CRC a numelui acestui fișier de stocare a versiunilor. Numele este reprezentarea Unicode a numelui fișierului cu extensia sa și un caracter nul suplimentar la sfârșit. Acest CRC este întotdeauna calculat folosind algoritmul CRC pentru fișierul .one, indiferent de formatul de fișier al magazinului de versiuni.

`fcrHashedChunkList (12 bytes):` O structură **FileChunkReference64x32** care specifică o referință la primul **FileNodeListFragment** dintr-o listă de fragmente hashing. Dacă valoarea structurii **FileChunkReference64x32** este „fcrZero” sau „fcrNil”, lista de fragmente hashed nu există.

`fcrTransactionLog (12 octeți):` O structură **FileChunkReference64x32** care specifică o referință la prima structură **TransactionLogFragment** dintr-un jurnal de tranzacții. Valoarea câmpului **fcrTransactionLog** NU TREBUIE să fie „fcrZero” și NU TREBUIE să fie „fcrNil”.

`fcrFileNodeListRoot (12 bytes):` O structură **FileChunkReference64x32** care specifică o referință la o listă de noduri de fișier rădăcină. Valoarea câmpului **fcrFileNodeListRoot** NU TREBUIE să fie „fcrZero” și NU TREBUIE să fie „fcrNil”.

`fcrFreeChunkList (12 octeți):` O structură **FileChunkReference64x32** care specifică o referință la prima structură **FreeChunkListFragment**. Dacă valoarea structurii **FileChunkReference64x32** este „fcrZero” sau „fcrNil”, atunci lista de bucăți libere nu există.

`cbExpectedFileLength (8 octeți):` Un întreg fără semn care specifică dimensiunea, în octeți, a acestui fișier de stocare a versiunilor.

`cbFreeSpaceInFreeChunkList (8 bytes):` Un întreg fără semn care TREBUIE să specifice dimensiunea, în octeți, a spațiului liber specificat de lista de fragmente libere.

`guidFileVersion (16 octeți):` Un GUID. Când valoarea câmpului **cTransactionsInLog** sau a câmpului **guidDenyReadFileVersion** este modificată, **guidFileVersion** TREBUIE schimbat cu un nou GUID.

`nFileVersionGeneration (8 octeți):` Un întreg fără semn care specifică de câte ori s-a schimbat fișierul. TREBUIE să fie incrementat când se modifică câmpul **guidFileVersion**.

`guidDenyReadFileVersion (16 octeți):` Un GUID. Când conținutul existent al fișierului este modificat, excluzând structura **Header** a fișierului și blocurile de stocare neutilizate, **guidDenyReadFileVersion** TREBUIE schimbat într-un nou GUID.

`grfDebugLogFlags (4 octeți):` TREBUIE să fie zero. TREBUIE ignorat.

`fcrDebugLog (12 octeți):` O structură **FileChunkReference64x32** care TREBUIE să aibă o valoare „fcrZero”. TREBUIE ignorat.

`fcrAllocVerificationFreeChunkList (12 octeți):` O structură **FileChunkReference64x32** care TREBUIE să fie „fcrZero”. TREBUIE ignorat.

`bnCreated (4 bytes):` Un număr întreg nesemnat care specifică numărul de compilare al aplicației care a creat acest fișier de stocare a versiunilor. TREBUIE ignorat.

`bnLastWroteToThisFile (4 bytes):` Un număr întreg nesemnat care specifică numărul de compilare al aplicației care a scris ultima dată în acest fișier de stocare a versiunilor. TREBUIE ignorat.

`bnOldestWritten (4 octeți):` Un întreg fără semn care specifică numărul de compilare al celei mai vechi aplicații care a scris în acest fișier de stocare a versiunilor. TREBUIE ignorat.

`bnNewestWritten (4 bytes):` Un număr întreg nesemnat care specifică numărul de compilare al celei mai noi aplicații care a scris în acest fișier de stocare a versiunilor. TREBUIE ignorat.

`rgbReserved (728 de octeți):` TREBUIE să fie zero. TREBUIE ignorat.

## Referințe ##

* [[MS-ONESTORE] - Format de fișier OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

