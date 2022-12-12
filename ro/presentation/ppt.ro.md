{
  "date" : "2019-12-13",
  "keywords" :[ "fișier ppt", "format fișier ppt", "ce este un fișier ppt", "fișier", "exemplu ppt", "extensie fișier ppt", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier PPT și despre API-urile care pot crea și deschide fișiere PPT.",
  "title" :"PPT - Format de fișier PowerPoint",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier PPT?

Un fișier cu extensia PPT reprezintă un fișier PowerPoint care constă dintr-o colecție de diapozitive pentru afișare ca SlideShow. Specifică formatul de fișier binar utilizat de Microsoft PowerPoint 97-2003. Un fișier PPT poate conține mai multe tipuri diferite de informații, cum ar fi text, marcatori, imagini, multimedia și alte obiecte OLE încorporate. Microsoft a venit cu un format de fișier mai nou pentru PowerPoint, cunoscut sub numele de [PPTX](/ro/presentation/pptx/), începând cu 2007, care se bazează pe Office OpenXML și este diferit de acest format de fișier binar. Mai multe alte programe de aplicație, cum ar fi OpenOffice Impress și Apple Keynote, pot crea, de asemenea, fișiere PPT.

## Scurt istoric ##

Microsoft a introdus formatul de fișier PPT odată cu lansarea PowerPoint în 1987. Formatul binar stabil a fost partajat ca implicit în PowerPoint 97-2003 pentru Windows. Formatul de fișier binar este acceptat pentru citire și scriere de cele mai recente versiuni de PowerPoint, inclusiv de PowerPoint 2016.

## Specificații de format de fișier ##

De la introducerea sa, formatul de fișier PPT a trecut prin mai multe revizuiri pentru adăugarea de noi funcții și îmbunătățiri. Cele mai recente specificații ale versiunii disponibile sunt cele ale versiunii 6.0 care au fost publicate în august 2018, care nu ar trebui amestecate cu numărul de produs real al formatului de fișier PPT, deoarece Microsoft nu mai oferă modificări pentru acest format.

### Prezentare generală a formatului fișierului ###

Unele dintre componentele cheie ale unui format de fișier PPT sunt următoarele:

#### Slide-uri ####

Datele utilizatorului, cum ar fi forme, text, animații și media sunt adăugate la o prezentare în interiorul unui Slide. O prezentare poate conține unul sau mai multe diapozitive care sunt afișate ca prezentare atunci când este rulată o prezentare. O prezentare conține diapozitive principale și diapozitive principale de titlu care acționează ca șablon pentru proprietățile vizuale comune ale diapozitivelor de prezentare. Există, de asemenea, un diapozitiv principal de note și un diapozitiv principal pentru fișe care servesc unui scop similar și oferă proprietăți vizuale comune pentru toate diapozitivele de note și toate fișele tipărite.

#### Forme ####

Formele sunt obiecte care permit utilizatorilor să adauge o varietate de conținut la un diapozitiv sub formă de substituenți, imagini și grafice. Formele de pe un diapozitiv principal definesc date comune pentru grupuri de forme.

#### Substituenți Forme ####

Acestea sunt substituenți speciali care servesc drept containere pentru o varietate de obiecte. Diferite forme de substituent pot fi folosite pentru a oferi indicii pentru a insera anumite tipuri de forme, cum ar fi tabele sau diagrame. În interiorul unui diapozitiv, o formă de substituent adoptă proprietățile vizuale dintr-un diapozitiv principal principal, diapozitiv principal de titlu sau diapozitiv principal de note.

#### Obiecte externe ####

Obiectele externe, cum ar fi conținutul audio încorporat și legat, videoclipul legat, obiectele OLE încorporate și legate și hyperlinkurile pot fi încorporate într-un diapozitiv. Aceste obiecte pot fi folosite pentru a activa obiecte legate pentru accesarea resurselor externe în timpul unei prezentări de diapozitive.

### Structuri de format de fișier ###

Formatele de fișiere binare PowerPoint constau în următoarele fluxuri pentru a reprezenta structura și datele generale ale documentului.

* Flux de utilizator curent
* Flux de documente PowerPoint
* Flux de imagini
* Informații rezumate și informații rezumate document (opțional)

Specificațiile complete pentru formatul de fișier DOC pot fi găsite așa cum sunt furnizate de [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) și ar trebui consultate cu referire la secțiunile menționate în detaliile următoare.

#### Flux de utilizator curent ####

Păstrează evidența ultimului utilizator care a deschis documentul și numele acestuia trebuie să fie „Utilizator actual”.

#### Flux de documente PowerPoint ####

Păstrează evidența tuturor informațiilor despre o prezentare PowerPoint și explică aspectul și conținutul acesteia. Este un flux obligatoriu al cărui nume TREBUIE să fie „PowerPoint Document”. Conținutul acestui flux este specificat de o secvență de înregistrări de nivel superior. Restricțiile de ordonare parțială ale secvenței de înregistrări sunt specificate în înregistrările PersistDirectoryAtom și UserEditAtom.

Ca înregistrări container, înregistrările DocumentContainer, MainMasterContainer (secțiunea 2.5.3), HandoutContainer (secțiunea 2.5.8), SlideContainer (secțiunea 2.5.1) și NotesContainer (secțiunea 2.5.6) sunt fiecare rădăcina unui arbore de înregistrări container și înregistrările atomice. În interiorul oricărei înregistrări container, pot exista alte înregistrări care nu sunt enumerate în mod explicit ca înregistrări copil. Înregistrările necunoscute sunt identificate atunci când câmpul recType al structurii RecordHeader (secțiunea 2.3.1) conține o valoare nespecificată de enumerarea RecordType (secțiunea 2.13.24). Aceste înregistrări necunoscute, dacă sunt întâlnite, TREBUIE ignorate și POATE <1> să fie păstrate. Înregistrările necunoscute pot fi ignorate căutând înainte recLen octeți de la sfârșitul structurii RecordHeader.

De fiecare dată când este scris acest flux, în fluxul existent pot fi adăugate înregistrări noi de nivel superior, o editare de utilizator sau întregul conținut al fluxului poate fi înlocuit cu o secvență actualizată de înregistrări de nivel superior. Dacă întregul flux nu este înlocuit, orice înregistrări de nivel superior existente anterior, care au cuprins orice editare anterioară de utilizator, pot fi depășite de înregistrările de nivel superior adăugate ulterior care cuprind editarea curentă a utilizatorului.

#### Flux de imagini ####

Acesta este un flux opțional care conține date despre imaginile conținute într-o prezentare PowerPoint. Numele său TREBUIE să fie „Imagini”. Conținutul acestui flux este specificat de înregistrarea OfficeArtBStoreDelay, așa cum este specificat în [MS-ODRAW] secțiunea 2.2.21.

#### Flux de informații rezumate ####

Păstrează statistici despre document conform standardului Microsoft Office. Numele fluxului de informații rezumate trebuie să fie „\005SummaryInformation”, unde \005 este caracterul cu valoarea 0x0005, nu literalul șir „\005”. Acest flux TREBUIE să fie omis pentru documentele criptate. Conținutul acestui flux este specificat în [MS-OSHARED] secțiunea 2.3.3.2.1.

#### Flux de informații despre rezumatul documentului ####

Un flux opțional al cărui nume TREBUIE să fie „\005DocumentSummaryInformation”, unde \005 este caracterul cu valoarea 0x0005, nu literalul șir „\005”. Acest flux POATE <2> fi omis pentru documentele criptate. Conținutul acestui flux este specificat în [MS-OSHARED] secțiunea 2.3.3.2.2.

#### Flux de informații rezumate criptate ####

Un flux opțional al cărui nume TREBUIE să fie „EncryptedSummary”. Acest flux există numai într-un document criptat. Conținutul acestui flux este specificat în [MS-OFFCRYPTO] secțiunea 2.3.5.4.

#### Stocarea semnăturii digitale ####

Un stocare opțional al cărui nume TREBUIE să fie „_xmlsignatures”. POATE fi omis și POATE fi ignorat. Conținutul acestei stocări este specificat în [MS-OFFCRYPTO] secțiunea 2.5.2.

#### Stocare de date XML personalizată ####

Un stocare opțional al cărui nume TREBUIE să fie „MsoDataStore”. Conținutul stocării este specificat în [MS-OSHARED] secțiunea 2.3.6.

#### Flux de semnături ####

Un flux opțional al cărui nume TREBUIE să fie „_signatures”. TREBUIE să fie omis și POATE fi ignorat. Conținutul acestui flux este specificat în [MS-OFFCRYPTO] secțiunea 2.5.1.

## Referințe ##

* [Specificații de format de fișier PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: tipuri de date comune și structuri de obiecte Office](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Structura de criptare a documentelor Office](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [Formate de fișiere PowerPoint](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

