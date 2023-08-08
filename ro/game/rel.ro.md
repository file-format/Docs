{
  "date" : "2021-09-08",
  "keywords" :[ "fișier rel", "format fișier rel", "ce este un fișier rel", "fișier", "exemplu rel", "extensie fișier rel", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier REL și despre API-urile care pot crea și deschide fișiere REL.",
  "title" :"REL – Fișier modul relocabil",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Ce este un fișier REL?
Un fișier cu extensia .rel poate fi folosit în mai multe scopuri. Prin urmare, în ceea ce privește clasificarea jocului, este cunoscut ca un fișier modul relocabil folosit de unele jocuri Nintendo Wii, cum ar fi Brawl, Super Smash Bros și Mario Kart Wii. Acesta cuprinde datele de joc, inclusiv modelele de personaje și etapele. Fișierele REL funcționează similar cu fișierele .DLL utilizate de Microsoft Windows.

## Format de fișier REL
Într-un format de fișier REL, fișierul este împărțit în mai multe secțiuni, grupate după acces similar, de exemplu, date numai pentru citire într-o secțiune, tot codul executabil este plasat în alta, etc. Fișierul începe cu o secțiune antet, urmată de:
- Tabel care conține informații despre secțiune.
- Datele secțiunii.
- Informații despre relocare.

### Antetul fișierului
Fișierul începe cu un antet de până la 0x4C octeți:
| Offset | Dimensiune | Nume câmp | Descriere |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Număr de identificare arbitrar. Trebuie să fie unic printre toate REL-urile utilizate de un joc. Nu trebuie să fie 0. |
| 0x04 | 4 | următorul | Indicator către modulul următor, completat în timpul execuției. |
| 0x08 | 4 | prev | Indicator către modulul anterior, completat în timpul execuției. |
| 0x0c | 4 | numSections | Numărul de secțiuni din dosar. |
| 0x10 | 4 | sectionInfoOffset | Deplasare față de începutul tabelului de secțiuni. |
| 0x14 | 4 | numeOffset | Offset la șirul ASCII care conține numele modulului. Poate fi NULL. Relativ la începutul fișierului REL. |
| 0x18 | 4 | numeMărime | Dimensiunea numelui modulului în octeți. |
| 0x1c | 4 | versiunea | Numărul versiunii formatului de fișier REL. |
| 0x20 | 4 | bssSize | Dimensiunea secțiunii „.bss”. |
| 0x24 | 4 | relOffset | Deplasare față de tabelul de relocare. |
| 0x28 | 4 | impOffset | Deplasare la tabelul imp. |
| 0x2c | 4 | impSize | Dimensiunea tabelului imp în octeți. |
| 0x30 | 1 | prologSection | Indexați în tabelul de secțiuni la care este relativ prolog. Omite dacă acest câmp este 0. |
| 0x31 | 1 | epilogSection | Indexați în tabelul de secțiuni la care este relativ epilog. Omite dacă acest câmp este 0. |
| 0x32 | 1 | nerezolvatăSecțiunea | Indexați în tabelul de secțiuni la care este relativ nerezolvat. Omite dacă acest câmp este 0. |
| 0x33 | 1 | bssSection | Indexați în tabelul de secțiuni la care este relativ bss. Umplut în timpul rulării! |
| 0x34 | 4 | prolog | Deplasare în secțiunea specificată a funcției _prolog. |
| 0x38 | 4 | epilog | Deplasare în secțiunea specificată a funcției _epilog. |
| 0x3c | 4 | nerezolvată | Deplasare în secțiunea specificată a funcției _unresolved. |
| 0x40 | 4 | aliniază | Numai versiunea ≥ 2. Constrângere de aliniere pe toate secțiunile, exprimată ca putere de 2. |
| 0x44 | 4 | bssAlign | Numai versiunea ≥ 2. Constrângere de aliniere pe toată secțiunea „.bss”, exprimată ca putere de 2. |
| 0x48 | 4 | fixSize | Numai versiunea ≥ 3. Dacă REL este legat cu OSLinkFixed (în loc de OSLink), spațiul de după această adresă poate fi folosit în alte scopuri (cum ar fi BSS). |

### Tabelul cu informații despre secțiune
Tabelul cu informații despre secțiune conține intrări **numSections** fiecare 0x8 octeți lungime:
| Offset | Dimensiune | Descriere |
-------|------------|-------------|
| 0x0 | 30 de biți | Offset de la începutul REL la secțiune. Dacă acesta este zero, secțiunea este o secțiune neinițializată (adică .bss). |
| 0x3,6 | 1 bit | Necunoscut. |
| 0x3,7 | 1 bit | Steagul executabil; dacă acesta este 1, secțiunea este executabilă. |
| 0x4 | 4 | Lungimea în octeți a secțiunii. Dacă acesta este zero, această intrare este omisă. |
| 0x8 | Următoarea intrare | Următoarea intrare |

### Date de relocare
Datele de relocare sunt una sau mai multe liste de structuri de 0x8 octeți. Sfârșitul fiecărei liste este marcat de codul de tip special 203:
| Offset | Nume | Dimensiune | Descriere |
-------|------------|------------|-----|
| 0x0 | offset | 2 | Offset în octeți față de relocarea anterioară în aceasta. Dacă aceasta este prima mutare în secțiune, aceasta este relativă la începutul secțiunii. |
| 0x2 | tip | 1 | Tipul de relocare. Descris mai jos. |
| 0x3 | sectiunea | 1 | Secțiunea simbolului pe care să o relocați. Pentru tipul special de relocare 202, acesta este în schimb numărul secțiunii din acest fișier căreia i se aplică următoarele înregistrări de relocare. |
| 0x4 | adaugă | 4 | Decalaj în octeți a simbolului față de care trebuie relocat, în raport cu începutul secțiunii sale. Aceasta este o adresă absolută, în schimb, pentru relocari împotriva main.dol. |
| 0x8 | Următoarea intrare | Următoarea intrare | Următoarea intrare |


 




## Referințe


* [Format modul modul obiect relocabil](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


