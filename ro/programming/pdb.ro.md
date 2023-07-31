{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier PDB - Un fișier de bază de date de program",
  "description":"Aflați despre formatul de fișier PDB și despre API-urile care pot crea și deschide fișiere PDB.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Ce este un fișier PDB?

Un fișier cu extensia .pdb este un fișier de bază de date de program care conține informații de depanare pentru un executabil compilat (EXE/DLL). Fișierele PDB sunt generate de Microsoft Compilers atunci când un program de aplicație este compilat în modul de depanare. Prezența fișierului PDB poate ajuta la ingineria inversă a unui executabil, deoarece conține informații semnificative despre toate simbolurile modulelor. Din acest motiv, aceste fișiere sunt păstrate separat de executabilul final. [API-ul DgbHelp] de la Microsoft (https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) poate deschide un fișier PDB pentru a obține informații precum public și exporturi, simboluri globale, simboluri locale, date de tip, fișiere sursă și numere de rând.

## Format de fișier PDB

PDB este formatul de fișier proprietar al Microsoft și nu a fost încă documentat oficial nicăieri. Cu toate acestea, o documentație de pornire este disponibilă [aici](https://github.com/Microsoft/microsoft-pdb) și poate fi referită.

### Fluxuri PDB

Fișierele PDB constau din mai multe fluxuri în care fiecare flux acționează ca un fișier individual virtual și conține informații. Scriitorii de fișiere PDB pot scrie în aceste fișiere și fișierul este finalizat numai după ce este emisă o comitere explicită. Un compilator poate continua să scrie într-un fișier PDB, dar să comite numai dacă tot codul utilizatorului este compilat cu succes. Un fișier PDB este format din următoarele fluxuri:

|Nr. flux |Cuprins |Descriere scurtă|
---|---|---|
|1| Pdb (header) |Informații despre versiune și informații pentru conectarea acestui PDB la EXE|
|2| Tpi (Manager de tip) |Toate tipurile utilizate în executabil.|
|3| Dbi (Informații de depanare) |Conține contribuțiile secțiunii și lista de „Modificări”|
|4| NameMap| Conține un tabel cu șiruri hash|
|4-(n+4)| n Moduri (informații despre modul)| Fiecare flux de mod conține simboluri și numere de linie pentru un compilaland|
|n+4| Hash simbol global| Un index care permite căutarea în simboluri globale după nume|
|n+5| Hash simbol public| Un index care permite căutarea în simboluri publice după adrese|
|n+6| Înregistrări de simbol| Înregistrări de simboluri reale ale simbolurilor globale și publice|
|n+7| Tastați hash| Hash folosit de fluxul TPI.|

Fiecare flux dintr-un fișier PDB cuprinde mai multe pagini care nu sunt neapărat numerotate consecutiv.

### Antet PDB

Un fișier PDB este cu un antet care constă într-o semnătură pentru identificarea și validarea formatului specific. Lungimea semnăturii depinde de formatul PDB. Antetul poate fi mai lung decât o singură pagină.

### Metadate PDB
Metadatele PDB sunt responsabile să recunoască toate fluxurile componente, oferind lungimea și secvența paginilor pentru fiecare flux. Comenzile sunt date fluxurilor consecutiv; începând cu 0. Există, de asemenea, un flux rădăcină neordonat, care conține unele dintre metadate.

## Referințe
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

