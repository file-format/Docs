{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Format fișier de stocare Outlook",
  "description":"Aflați despre formatul de fișier OST și despre API-urile care pot crea și deschide fișiere OST.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier OST?

OST sau fișierele de stocare offline reprezintă datele căsuței poștale ale utilizatorului în modul offline pe mașina locală la înregistrarea la Exchange Server utilizând Microsoft Outlook. Este creat automat la prima utilizare a Microsoft Outlook la conectarea cu serverul. Odată creat fișierul, datele sunt sincronizate cu serverul de e-mail, astfel încât acestea să fie disponibile și offline în caz de deconectare de la serverul de e-mail. Fișierele OST pot utiliza articole din cutia poștală, cum ar fi e-mailuri, contacte, informații din calendar, note, sarcini și alte date similare. Utilizatorii pot crea e-mailuri și alte elemente de date în fișierul OST chiar și în absența conexiunii la server, dar acestea nu vor fi sincronizate cu serverul. Odată stabilită conexiunea, fișierul local este sincronizat din nou cu serverul, astfel încât atât serverul, cât și copia locală să fie la același nivel de informații.

## Format de fișier OST

Formatul de fișier OST (Offline Storage Table) și [PST](/ro/email/pst/) (Personal Storage Table) este format din fișierul personal folder (PFF) care corespunde stocării e-mailurilor, contactelor și programărilor utilizatorului. Datele dintr-un fișier PFF sunt stocate în little-endian, cu toate datele și orele reprezentate ca FILETIME în UTC. [MS-PST] definește două tipuri de PFF:

* Format ANSI pe 32 de biți
* Format Unicode pe 64 de biți

Formatul fișierului PST [specificații](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), așa cum este disponibil de la Microsoft, se aplică, de asemenea, formatului de fișier OST ca gratuit și licențiere irevocabilă de brevet prin Promisiunea de specificații deschise. Se compune din următoarele elemente distinctive:

* Antetul Fle
* Datele antetului fișierului
* Nod de ramură index
* Nodul frunză index
* (Fișier) index offset
* Index de descriptor (articol).
* Descriptori locali
* Tip tabel de articole

### Informații antet

Structura HEADER a fișierului OST este situată chiar la începutul fișierului la 0 offset. Conține informații despre metadate despre fișierul OST și informațiile ROOT pentru a accesa structurile de date NDB Layer descrise mai sus. Structura HEADER diferă pentru versiunile Unicode și ANSI ale formatului de fișier OST.

Antetul începe cu un cuvânt magic de 4 octeți **!BDN** reprezentat prin octeți (0x21, 0x42, 0x44, 0x4E). Un alt număr magic de 2 octeți, **SM** (0x53, 0x4D), este situat la offset 8 de la începutul fișierului. Informațiile despre versiune (ANSI sau Unicode) se află la un offset de 10 de la începutul fișierului. Valoarea hex (0x17) specifică fișierul OST Unicode, în timp ce 0x0E sau 0x0F reprezintă formatul de fișier ANSI.

|Câmp|Descriere
---|---|
|dwMagic (4 octeți)|TREBUIE să fie „{ 0x21, 0x42, 0x44, 0x4E } (“!BDN”)”
|dwCRCPartial (4 octeți)|Valoarea CRC de 32 de biți a celor 471 de octeți de date pornind de la wMagicClient (0ffset 0x0008)
|wMagicClient (2 octeți)|TREBUIE să fie „{ 0x53, 0x4D }”.
|wVer (2 octeți)|Versiune format fișier. Această valoare TREBUIE să fie 14 sau 15 dacă fișierul este un fișier PST ANSI și TREBUIE să fie 23 dacă fișierul este un fișier PST Unicode.
|wVerClient (2 octeți)|Versiune format fișier client. Versiunea care corespunde formatului descris în acest document este 19. Creatorii unui fișier PST nou bazat pe acest document TREBUIE să inițializeze această valoare la 19.
|bPlatformCreate (1 octet)|Această valoare TREBUIE setată la 0x01.
|bPlatformAccess (1 octet)|Această valoare TREBUIE setată la 0x01.
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
|bCryptMethod (1 byte)|Indică modul în care sunt codificate datele din fișierul PST. TREBUIE să fie setat la una dintre valorile predefinite (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbRezervat (2 octeți)| Rezervat; TREBUIE setat la zero.
|bidNextB (8 bytes)|Indică următoarea valoare BID disponibilă. Numai în format de fișier Unicode PST.
|bidNextB (NUMAI Unicode: 8 octeți)|Următorul BID. Această valoare este contorul monoton care indică BID-ul care urmează să fie alocat pentru următorul bloc alocat. Valorile BID avansează în trepte de 4. Pentru mai multe detalii, consultați secțiunea 2.2.2.2.
|dwCRCFull (4 octeți)|Valoarea CRC pe 32 de biți a celor 516 octeți de date începând de la wMagicClient până la bidNextB, inclusiv. Numai în format de fișier Unicode PST.
|ullReserved (8 bytes)|Rezervat; TREBUIE setat la zero. Numai în format de fișier ANSI PST.
|dwReserved (4 bytes)|Rezervat; TREBUIE setat la zero. Numai în format de fișier ANSI PST.
|rgbReserved2 (3 octeți)|
|bRezervat (1 octet) |
|rgbReserved3 (32 octeți) |

## Referințe

* [Format de fișier foldere personale Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Specificații de format de fișier al folderului personal](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

