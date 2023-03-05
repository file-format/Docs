{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST – Formatul fișierului Outlook Personal Information Store",
  "description":"Aflați despre formatul de fișier PST și despre API-urile care pot crea și deschide fișiere PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier PST?

Fișierele cu extensia .pst reprezintă fișiere de stocare personale Outlook (numite și tabel de stocare personală) care stochează o varietate de informații despre utilizator. Informațiile despre utilizator sunt stocate în foldere de diferite tipuri, care includ e-mailuri, articole din calendar, note, contacte și alte câteva formate de fișiere. Fișierele PST sunt utilizate pentru arhivarea datelor de e-mail offline, care pot fi ulterior încărcate și vizualizate în diferite aplicații.

## Specificații pentru formatul fișierului PST

Formatul fișierului PST [specificații](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) sunt disponibile de la Microsoft ca licență gratuită și irevocabilă de brevet prin intermediul Open Specification Promise .

### Tip de formate PST

Formatele de fișiere PST sunt clasificate în două tipuri, în funcție de codificarea tipului de fișier. Fișierele PST codificate ANSI sunt formate de fișiere mai vechi și sunt acceptate numai de Outlook 2002 și versiunile anterioare. Astfel de fișiere au o limită de dimensiune maximă de 2 GB (2^^31^^ octeți) și nu acceptă Unicode. Un tip de format de fișier mai modern, bazat pe codificarea Unicode, elimină limitarea dimensiunii fișierului și poate atinge dimensiunea maximă a datelor de 50 GB.

### Organizarea logică a formatului de fișier PST

La baza formatului de fișier PST se află B-Tree care păstrează datele sortate și permite căutări, acces secvențial, inserări, ștergeri etc. în timp logaritmic. Structura generală a unui fișier PST este organizată în trei straturi.

![Logical layers of a PST file](/ro/email/PST-1.png "Logical layers of a PST file")

`Node Database (NDB) Layer` - Stratul de bază de date nod se află la nivelul inferior al unui fișier PST și include baza de date a nodurilor. Aceste noduri reprezintă de fapt facilități de stocare de nivel inferior ale formatului de fișier PST. Stratul NDB cuprinde antet, informații de alocare a fișierelor, blocuri și BTrees (Node BTree și Block BTree) din punct de vedere al stocării. Nodurile și blocurile stratului NDB sunt legate prin Data BID, care este una dintre cele patru proprietăți ale Nod reference, adică NID (Node ID), Parent NID, Data BID (Block BID) și SubNode BID.

`Liste, tabele și stratul de proprietăți -` Stratul LTP oferă înțelegerea logică a conceptelor de nivel superior peste NDB. Pe lângă alte elemente, stratul LTP cuprinde în principal contextul proprietății (PC) și Contextul tabelului (TC). PC este o colecție de proprietăți, în timp ce TC reprezintă o matrice bidimensională de colecție de proprietăți în raport cu prezența acestora. Implementarea eficientă a PC-urilor și a TC-urilor, stratul LTP utilizează următoarele două tipuri de structuri de date deasupra Nodului NDB:

* Heap On Node (HN) - permite sub-alocarea fluxului de date al unui nod în fragmente mici, de dimensiuni variabile.
* BTree on Heap (BTH) - BTH oferă un mod convenabil și practic de căutare prin date PC-urile, descrise mai sus, sunt implementate ca BTH-uri și de aceea este implementat prin construirea în interiorul unei structuri HN.

`Messaging Layer -` Regulile de nivel superior și logica de afaceri pentru lucrul cu fișierele PST sunt implementate la acest nivel. Ieșirea logică a acestui strat rezultă ca obiecte folder, obiecte mesaj, obiecte atașate și proprietăți, care este posibilă prin combinarea straturilor LTP și NDB. Regulile și cerințele, care trebuie respectate la modificarea conținutului PST, sunt, de asemenea, definite la acest nivel.

### Organizarea fizică a formatului de fișier PST

Nivelul ridicat de organizare a fișierelor PST este așa cum se arată în figura de mai jos. Aceasta este doar o prezentare generală a diferitelor concepte din elementele logice ale fișierului PST.

![Physical organization of the PST file format](/ro/email/PST-2.png "Physical organization of the PST file format")


#### Informații antet PST

Structura HEADER a fișierului PST este situată chiar la începutul fișierului la 0 offset. Conține informații despre metadate despre fișierul PST și informațiile ROOT pentru a accesa structurile de date NDB Layer descrise mai sus. Structura HEADER diferă pentru versiunile Unicode și ANSI ale formatului de fișier PST.

Antetul începe cu un cuvânt magic de 4 octeți **!BDN** reprezentat prin octeți (0x21, 0x42, 0x44, 0x4E). Un alt număr magic de 2 octeți, **SM** (0x53, 0x4D), este situat la offset 8 de la începutul fișierului. Informațiile despre versiune (ANSI sau Unicode) se află la un offset de 10 de la începutul fișierului. Valoarea hex (0x17) specifică fișierul PST Unicode, în timp ce 0x0E sau 0x0F reprezintă formatul de fișier ANSI.

|Câmp|Descriere
---|---|
|dwMagic (4 octeți)|TREBUIE să fie „{ 0x21, 0x42, 0x44, 0x4E } (“!BDN”)”
|dwCRCPartial (4 octeți)|Valoarea CRC de 32 de biți a celor 471 de octeți de date pornind de la wMagicClient (0ffset 0x0008)
|wMagicClient (2 octeți)|TREBUIE să fie „{ 0x53, 0x4D }”.
|wVer (2 octeți)|Versiune format fișier. Această valoare TREBUIE să fie 14 sau 15 dacă fișierul este un fișier PST ANSI și TREBUIE să fie 23 dacă fișierul este un fișier PST Unicode.
|wVerClient (2 octeți)|Versiune format fișier client. Versiunea care corespunde formatului descris în acest document este 19. Creatorii unui fișier PST nou bazat pe acest document TREBUIE să inițializeze această valoare la 19.
|bPlatformCreate (1 octet)|Această valoare TREBUIE setată la 0x01.
|bPlatformAccess (1 octet)|Această valoare TREBUIE să fie setată la 0x01.
|dwRezervat (8 octeți)|
|bidUnused (numai 8 octeți Unicode)|Adăugarea neutilizată a fost adăugată când a fost creat formatul de fișier Unicode PST.
|bidNextP (Unicode: 8 octeți; ANSI: 4 octeți)|BID în pagina următoare. Paginile au un contor special pentru alocarea valorilor bidIndex. Valoarea bidIndex pentru BID-uri pentru pagini este alocată din acest contor.
|bidNextB (doar 4 octeți ANSI): |Următorul BID. Această valoare este contorul monoton care indică BID-ul care urmează să fie alocat pentru următorul bloc alocat. Valorile BID avansează în trepte de 4. Pentru mai multe detalii, consultați secțiunea 2.2.2.2.
|dwUnique (4 octeți)|Aceasta este o valoare care crește monoton care este modificată de fiecare dată când se modifică structura HEADER a fișierului PST. Funcția acestei valori este de a furniza o valoare unică și de a se asigura că CRC-urile HEADER sunt diferite după fiecare modificare a antetului.
|rgnid[](128 octeți)|O matrice fixă de 32 NID-uri, fiecare corespunzând unuia dintre cele 32 de NID_TYPE posibile (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,ASSNID_TYPE_MESSAGE)
|qwUnused (8 bytes)|Spatiu neutilizat; TREBUIE setat la zero. Numai în format de fișier Unicode PST.
|rădăcină (Unicode: 72 de octeți; ANSI: 40 de octeți)|O structură ROOT (secțiunea 2.2.2.5).
|dwAlign (4 bytes)|Octeți de aliniere neutilizați; TREBUIE setat la zero. Numai în format de fișier Unicode PST.
|rgbFM (128 bytes)|FMap depreciat. Acesta nu mai este folosit și TREBUIE să fie completat cu 0xFF. Cititorii TREBUIE să ignore valoarea acestor octeți.
|rgbFP (128 de octeți)|FPMap depreciat. Acesta nu mai este folosit și TREBUIE să fie completat cu 0xFF. Cititorii TREBUIE să ignore valoarea acestor octeți.
|bSentinel (1 octet)|TREBUIE să fie setat la 0x80.
|bCryptMethod (1 octet)|Indică modul în care sunt codificate datele din fișierul PST. TREBUIE să fie setat la una dintre valorile predefinite (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbRezervat (2 octeți)| Rezervat; TREBUIE setat la zero.
|bidNextB (8 bytes)|Indică următoarea valoare BID disponibilă. Numai în format de fișier Unicode PST.
|bidNextB (NUMAI Unicode: 8 octeți)|Următorul BID. Această valoare este contorul monoton care indică BID-ul care urmează să fie alocat pentru următorul bloc alocat. Valorile BID avansează în trepte de 4. Pentru mai multe detalii, consultați secțiunea 2.2.2.2.
|dwCRCFull (4 octeți)|Valoarea CRC pe 32 de biți a celor 516 octeți de date începând de la wMagicClient până la bidNextB, inclusiv. Numai în format de fișier Unicode PST.
|ullReserved (8 bytes)|Rezervat; TREBUIE setat la zero. Numai în format de fișier ANSI PST.
|dwReserved (4 bytes)|Rezervat; TREBUIE setat la zero. Numai în format de fișier ANSI PST.
|rgbReserved2 (3 octeți)|
|bRezervat (1 octet) |
|rgbReserved3 (32 octeți) |

### Protejarea datelor ###

Pentru securitate, fișierele PST pot fi, de asemenea, protejate cu parolă, ceea ce necesită ca aplicația de încărcare să aplice parola înainte de a putea fi vizualizate. Parola aplicată fișierului PST este stocată în magazinul de mesaje. Cu toate acestea, acest lucru nu oferă o protecție puternică a datelor, deoarece parola poate fi eliminată de instrumentele disponibile. De asemenea, parola specificată de utilizator nu este utilizată ca parte a cheii pentru codificarea și decodarea algoritmilor de cifrare. Astfel, nu există niciun beneficiu de a proteja datele care urmează să fie accesate de către părți neautorizate. Stocarea parolei ca hash CRC-32 a șirului original o face, de asemenea, o metodă slabă pentru securitatea datelor împotriva abordării forței brute.

## Referințe ##

* [Format de fișier foldere personale Outlook (.pst)](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Specificații de format de fișier al folderului personal](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

