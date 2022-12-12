{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "fișier", "extensie", "format fișier", "Cuvânt", "Document" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC – Fișier document Microsoft Word",
  "description":"Aflați despre formatul de fișier DOC și despre API-urile care pot crea și deschide fișiere DOC.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Ce este un fișier DOC?

Fișierele cu extensia .doc reprezintă documente generate de Microsoft Word sau alte documente de procesare de text în format de fișier binar. Extensia a fost folosită inițial pentru documentarea text simplu pe mai multe sisteme de operare diferite. Poate conține mai multe tipuri diferite de date, cum ar fi imagini, formatate, precum și text simplu, grafice, diagrame, obiecte încorporate, link-uri, pagini, formatare a paginii, setări de imprimare și multe altele. Formatul a fost popular pentru tot felul de documentație datorită varietății de opțiuni pe care le oferă utilizatorilor pentru redactarea de manuale, propuneri, specificații, CV-uri, articole sau orice documente similare. Versiunea actualizată a DOC este [DOCX](/ro/Word%20Processing/DOCX/) care se bazează pe Office OpenXML ale cărui specificații sunt disponibile în mod deschis.

## Scurt istoric ##

WordPerfect, un produs al [Corel](https://www.corel.com/en/), a folosit DOC ca extensie a formatului lor proprietar. În anii 1980, WordPerfect a rămas alegerea de utilizare pe majoritatea computerelor datorită disponibilității sale ușoare, conformității cu majoritatea computerelor și sistemelor de operare. Cu toate acestea, WordPerfect și-a văzut căderea pe sistemul de operare Windows atunci când Microsoft a introdus Microsoft Word ca produs pentru format de fișier de documente și a ales extensia DOC pentru formatul lor proprietar. Pe măsură ce Microsoft Word a devenit din ce în ce mai popular, formatul de fișier DOC a suferit mai multe revizuiri de la Microsoft Word 97 - 2003. Era în 2007 când formatul implicit de fișier DOC a fost înlocuit cu formatul Office Open XML (cunoscut sub numele de DOCX) și noile versiuni ale Microsoft Word utilizează acum această nouă extensie ca format de fișier implicit.

## Specificații format fișier DOC - Mai multe informații

Microsoft nu a lansat specificațiile de format de fișier DOC mult timp până în 2008. În februarie 2008, specificațiile de format au fost lansate pentru formatul de fișier .doc conform Microsoft Open Specification Promise. Deși specificația nu descrie toate caracteristicile utilizate de formatul DOC, oferă informații ample despre cunoștințele necesare pentru a lucra cu acest format de fișier. Totuși, este necesară inginerie inversă pentru a utiliza informațiile disponibile. Specificațiile au fost actualizate de mai multe ori, iar cea mai recentă [reviziune](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) este 8.0, care a fost actualizată începând cu august 2018 .

### Câteva concepte fundamentale ###

Înainte de a intra în detalii despre specificațiile formatului de fișier pentru DOC, este necesar să înțelegem câteva concepte fundamentale pentru a lucra cu acest format de fișier.

**File Information Base (Fib):** Structura Fib conține informații despre document și specifică indicatorii fișierului către diferite porțiuni care alcătuiesc documentul.
Fib este o structură cu lungime variabilă. Cu excepția porțiunii de bază, care este fixă în dimensiune, fiecare secțiune este precedată de un câmp de numărare care specifică dimensiunea următoarei secțiuni.

**Poziția caracterului:** CP sau Poziția caracterului reprezintă un număr întreg de 32 de biți fără semn care servește ca index pe bază de zero al unui caracter în textul documentului. Locația și dimensiunea fiecărui caracter din fișier nu pot fi preluate direct și trebuie calculate folosind algoritmul prespecificat. Caracterele includ:

* Textul documentului
* Ancore ale obiectelor, cum ar fi notele de subsol sau casetele de text
* Caractere de control, cum ar fi semnele de paragraf și semnele de celule de tabel

**PLC:** Structura PLC este o matrice de CP-uri urmată de o matrice de elemente de date. Elementele de date pentru orice PLC trebuie să aibă aceeași dimensiune de zero sau mai mulți octeți și, din acest motiv, numărul de CP-uri trebuie să fie cu unul mai mult decât numărul de elemente de date. Structurile PLC sunt de diferite tipuri, unde fiecare tip specifică dacă CP-urile duplicat sunt permise pentru acel tip sau nu. O structură PLC constă din:

* **aCP (lungime variabilă):** O matrice de elemente CP. Fiecare tip de structură **PLC** specifică semnificația elementelor CP și domeniul permis.
* **aDate (lungime variabilă):** Fiecare tip de structură **PLC** specifică structura și semnificația elementelor de date, orice restricții privind numărul de elemente de date și orice restricții privind datele conținute în acestea. De asemenea, specifică relația dintre elementele de date și CP-urile corespunzătoare.

**Selectare validă:** Construcțiile fișierului .DOC sunt descrise în principal de o serie de CP. Există o serie de [reguli](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) specificate de Microsoft pentru a fi urmate în acest caz.

**STTB:** STTB este un tabel de șiruri care este alcătuit dintr-un antet care este urmat de o matrice de elemente. Valoarea **cData** specifică numărul de elemente care sunt conținute în matrice.

**Depozitare proprietăți:** Un fișier word poate avea diferite elemente, cum ar fi text, paragrafe, tabele, imagini și secțiuni în care fiecare poate avea propriile sale proprietăți. Proprietățile acestora sunt stocate în fișierul Word ca diferențe față de valoarea implicită. Astfel de diferențe sunt specificate de PRl care constă dintr-un Modificator de Proprietate Unică (Sprm) și operandul acestuia. O aplicație poate determina setul final de proprietăți prin aplicarea listelor de **Prl**-uri.

**Protecție cu parolă:** Fișierele Word pot fi, de asemenea, protejate cu parolă, pentru care poate fi utilizat unul dintre următoarele mecanisme.

* Ofuscare XOR
* Criptare RC4 pentru documente binar Office
* Document binar Office RC4 CryptoAPI criptare

Dacă FibBase.fEncrypted și FibBase.fObfuscation sunt ambele 1, fișierul este ofuscat utilizând opticarea XOR.

Dacă FibBase.fEncrypted este 1 și FibBase.fObfuscation este 0, fișierul este criptat utilizând fie Office Binary Document RC4 Encryption, fie Office Binary Document RC4 CryptoAPI Encryption, cu EncryptionHeader stocat în primii octeți FibBase.lKey ai fluxului Tabel. EncryptionHeader.EncryptionVersionInfo specifică ce mecanism de criptare a fost folosit pentru a cripta fișierul.

### Structura fișierului ###

Un fișier Word binar în originalitatea sa este un fișier compus OLE care cuprinde mai multe stocări și fluxuri. Aceste stocări și fluxuri au propria lor structură și dimensiuni, care specifică parametrii de scriere și citire. Acestea sunt:

#### Flux WordDocument ####

Acest flux conține textul documentului și alte informații la care se face referire din alte părți ale fișierului. Fluxul nu are o structură predefinită, în afară de FIB la început, care este obligatoriu și ar trebui să fie la offset 0. Acest flux nu trebuie să fie mai mare de 2147 MB.

#### 1TableStream sau 0TableStream ####

Un fișier Word binar poate conține fluxuri de tabel cunoscute ca flux 1Table sau flux 0Table. Cel puțin unul dintre acestea ar trebui să fie prezent în document. Totuși, dacă un document conține atât fluxuri 1Table, cât și 0Table, este folosit doar fluxul la care face referire base.fWhichTblStm. Fluxul fără referință TREBUIE ignorat.
Fluxul de tabel NU TREBUIE să fie mai mare de 2147 MB.

#### Flux de date ####

Fluxul de date nu are o structură predefinită. Conține date la care se face referire din FIB sau din alte părți ale fișierului. Acest flux nu trebuie să fie prezent dacă nu există referințe la el. Fluxul de date NU TREBUIE să fie mai mare de 2147 MB.

#### Stocare pool de obiecte ####

Stocarea Pool de obiecte conține stocări pentru obiectele OLE încorporate. Această stocare nu trebuie să fie prezentă dacă nu există obiecte OLE încorporate în document.

#### Stocare de date XML personalizată ####

Stocarea de date XML personalizată este o stocare opțională al cărei nume TREBUIE să fie „MsoDataStore”.

#### Flux de informații rezumate ####

Fluxul de informații rezumate este un flux opțional al cărui nume TREBUIE să fie „\005SummaryInformation”, unde \005 este caracterul cu valoarea 0x0005 și nu literalul șir „\005”.

#### Flux de informații despre rezumatul documentului ####

Fluxul de informații despre rezumatul documentului este un flux opțional al cărui nume TREBUIE să fie „\005DocumentSummaryInformation”, unde \005 este caracterul cu valoarea 0x0005, nu literalul șir „\005”.

#### Flux de criptare ####

Fluxul de criptare este un flux opțional al cărui nume TREBUIE să fie „criptare”. Acest flux NU TREBUIE să fie prezent decât dacă sunt îndeplinite ambele condiții următoare:

* Documentul este criptat cu Office Binary Document RC4 CryptoAPI Encryption.
* Valoarea fDocProps este setată în EncryptionHeader.Flags.

#### Stocare macrocomenzi ####

Stocarea macrocomenzi este o stocare opțională care conține macrocomenzile pentru fișier. Dacă este prezent, TREBUIE să fie un proiect de stocare rădăcină.

#### Stocare semnături XML ####

Stocarea de semnături XML este o stocare opțională al cărei nume TREBUIE să fie „_xmlsignatures”.

#### Flux de semnături ####

Fluxul de semnături este un flux opțional al cărui nume TREBUIE să fie „_signatures”. Acest flux conține semnături digitale.

#### Gestionarea drepturilor la informații Spațiu de stocare a datelor ####

Spațiul de stocare a datelor de gestionare a drepturilor la informații este o stocare opțională al cărei nume TREBUIE să fie „\006DataSpaces”, unde \006 este caracterul cu valoarea 0x0006 și nu literalul șir „\006”. Dacă această stocare este prezentă, Streamul de conținut protejat TREBUIE să fie prezent.
Dacă această stocare este prezentă, toate fluxurile și stocările specificate, altele decât această stocare și fluxul de conținut protejat TREBUIE să fie citite din fluxul de conținut protejat, așa cum este specificat în [MS-OFFCRYPTO] și dacă oricare dintre aceste fluxuri și stocări există în afara conținutului protejat. Stream, acestea TREBUIE ignorate.

#### Flux de conținut protejat ####

Fluxul de conținut protejat este un flux opțional al cărui nume TREBUIE să fie „\009DRRMContent”, unde \009 este caracterul cu valoarea 0x0009 și nu literalul șir „\009”.
Dacă acest flux este prezent, TREBUIE să fie prezent și stocarea spațiului de date pentru gestionarea drepturilor de informare.

## Referințe ##

* [Specificații de formare a fișierelor MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))

