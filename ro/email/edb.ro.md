{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier EDB - Un fișier de bază de date Exchange Mail",
  "description":"Aflați despre formatul de fișier EDB și despre API-urile care pot crea și deschide fișiere EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Ce este un fișier EDB?

Un fișier cu extensia de fișier .edb este o bază de date de cutie poștală creată de Microsoft Exchange Server pentru a stoca date legate de e-mail. EDB, Exchange Database, stochează mesajele care sunt în proces și non-SMTP. EDB sunt cunoscute și ca fișiere de bază de date Extensible Storage Engine (ESE) și stochează fișiere folosind structura b-tree. Fiind fișiere de stocare, fișierele EDB pot fi convertite în alte formate de fișiere de stocare e-mail, cum ar fi [PST](/ro/email/pst/) și [OST](/ro/email/ost/).

## Format de fișier EDB

Nu există specificații de format de fișier EDB oficiale/deschise disponibile care să poată fi referite. S-au făcut unele progrese pentru ingineria inversă a formatului fișierului, rezultând decodificarea parțială a specificațiilor. Conform acestora, un fișier EDB constă din:
* Antet fișier - Conține informații despre antetul fișierului bazei de date
* Pagini cu dimensiuni fixe - Conține baza de date care constă din tabele și indecși

### Antet fișier bază de date
Antetul fișierului bazei de date se află în prima pagină a bazei de date și are cel puțin 668 de octeți. Antetul fișierului conține „Versiune format fișier” și „Tip fișier” în plus față de alte câmpuri.

#### Tipuri de fisiere
|Tip|Descriere
---|---|
|0| Baza de date|
|1| Streaming|

„Notă:” identificatorii pentru aceste tipuri nu sunt cunoscuți.

#### Versiune format fișier
Formatul original al EDB a început în aprilie 1997 și a continuat să evolueze pentru modificări ulterioare.

|Data revizuirii|Versiune|Versiune|descriere
---|---|---|---|
|Apr 1997| 0x00000620|0x00000000| Formatul beta al sistemului de operare original.|
|Mai 1997 |0x00000620|0x00000001| Adăugați coloane în catalog pentru indexarea condiționată și OLD.|
|Iun 1997|0x00000620|0x00000002|Adăugați indicatorul fLocalizedText în IDB.|
|Oct 1997|0x00000620|0x00000003|Adăugați SPLIT_BUFFER la paginile rădăcină a arborelui spațial.|
|Ian 1998|0x00000620|0x00000002|Reveniți revizuirea pentru ca ESE97 să rămână compatibil înainte.|
||0x00000620|0x00000003|Adăugați noi coloane etichetate în catalog („CallbackData” și „CallbackDependencies”).|
|Mai 1998|0x00000620|0x00000004|Suport Super Long Value (SLV): signSLV, fSLVExists in dbheader.|
|Mai 1998|0x00000620|0x00000005|Arbore spațial nou SLV.|
|Oct 1998|0x00000620|0x00000006|Hartă spațială SLV.|
|Dec 1998|0x00000620|0x00000007|4-byte IDXSEG.|
|Ian 1999|0x00000620|0x00000008|Noul format de coloană șablon.|
|Iun 1999|0x00000620|0x00000009|Coloane șablon sortate. Folosit în Windows XP SP3|
||0x00000620|0x0000000b|Conține antetul paginii cu suma de verificare ECCUsed in Exchange|
||0x00000620|0x0000000c|Utilizat în Windows Vista (SP0)|
||0x00000620|0x00000011|Suport pentru pagini de 2 KiB, 16 KiB și 32 KiB. Antet de pagină extins cu sume de verificare ECC suplimentare. Comprimarea coloanelor. Sugestii de spațiu. Folosit în Windows 7 (SP0)|
|Mai 1999|0x00000623|0x00000000|New Space Manager.|

### Fișiere baze de date

Fișierul bazei de date EDB conține schema pentru toate tabelele din baza de date. În plus, include, de asemenea, înregistrări pentru toate tabelele bazei de date și indecși pentru tabele. Locația sa este determinată de următorii identificatori.

* JetCreateDatabase
* JetCreateDatabase2
* JetAttachDatabase
* JetAttachDatabase2

Pe baza acestora, starea bazei de date poate fi evaluată după cum urmează.

|Valoare|Identificator|Descriere
---|---|---|
|1|JET_dbstateJustCreated|Baza de date tocmai a fost creată.|
|2|JET_dbstateDirtyShutdown|Baza de date necesită o recuperare hard sau soft pentru a fi rulată pentru a deveni utilizabilă sau mobilă. Nu ar trebui să încerci să muți bazele de date în această stare.|
|3|JET_dbstateCleanShutdown|Baza de date este într-o stare curată. Baza de date poate fi atașată fără fișiere jurnal.|
|4|JET_dbstateBeingConverted|Baza de date este în curs de modernizare.|
|5|JET_dbstateForceDetachInternal|Această valoare este introdusă în WindowsXP|
 

## Referințe
* [Specificații pentru fișierul de bază de date (EDB) Extensible Storage Engine (ESE)](https://github.com/libyal/libesedb/tree/main/documentation)

