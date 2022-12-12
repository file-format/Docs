{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "extensie", "fișier dbf", "format fișier dbf", "Tip fișier bază de date", "Format fișier bază de date", "ce este un fișier dbf", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier DBF și despre API-urile care pot crea și deschide fișiere DBF.",
  "title" :"DBF - fișierul bazei de date dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Ce este un fișier DBF?
Fișierul cu extensia .dbf este un fișier de bază de date utilizat de o aplicație de sistem de gestionare a bazelor de date numită **dBASE**. Inițial, baza de date dBASE a fost numită Project Vulcan; început de **Wayne Ratliff** în 1978. Tipul de fișier DBF a fost introdus cu dBASE II în 1983. Aranjează mai multe înregistrări de date cu câmpuri de tip Array. Software-ul de bază de date **xBase**, care este pupul datorită compatibilității sale cu o gamă largă de formate de fișiere; acceptă și fișierele DBF.

## Format de fișier DBF
Formatul de fișier DBF aparține sistemului de management al bazei de date dBASE, dar poate fi compatibil cu xBase sau cu alte programe DBMS. Versiunea inițială a fișierului dbf a constat dintr-un tabel simplu care putea avea date adăugate, modificate, șterse sau tipărite folosind setul de caractere ASCII. Odată cu trecerea timpului, .dbf a fost îmbunătățit și au fost adăugate fișiere suplimentare pentru a crește caracteristicile și capacitățile sistemului de baze de date.

În dBASE modern, un fișier DBF constă dintr-un antet, înregistrările de date și markerul EOF (Sfârșitul fișierului).

- Antetul conține informații despre fișier, cum ar fi numărul de înregistrări și numărul de tipuri de câmpuri utilizate în înregistrări.
- Înregistrările conțin datele reale.
- Sfârșitul fișierului este marcat de un singur octet, cu valoarea 0x1A.

### Antetul fișierului
Aspectul antetului fișierului în dBase este prezentat în următorul tabel:

| octet | Cuprins | Înțeles |
---|---|---|
| 0 | 1 octet | dBASE valid pentru fișierul DOS; biții 0–2 indică numărul versiunii, bit 3 indică prezența unui fișier memo dBASE pentru DOS, biții 4–6 indică prezența unui tabel SQL, biții 7 indică prezența oricărui fișier memo (fie dBASE m PLUS sau dBASE pentru DOS) |
| 1–3 | 3 octeți | Data ultimei actualizări; formatat ca YYMMDD |
| 4–7 | număr pe 32 de biți | Numărul de înregistrări din fișierul bazei de date |
| 8–9 | număr pe 16 biți | Numărul de octeți din antet |
| 10–11 | număr pe 16 biți | Numărul de octeți din înregistrare |
| 12–13 | 2 octeți | Rezervat; umple cu 0 |
| 14 | 1 octet | Indicator care indică tranzacția incompletă[nota 1] |
| 15 | 1 octet | Flag de criptare[nota 2] |
| 16–27 | 12 octeți | Rezervat pentru dBASE pentru DOS într-un mediu multi-utilizator |
| 28 | 1 octet | Steagul fișierului .mdx de producție; 1 dacă există un fișier .mdx de producție, 0 dacă nu |
| 29 | 1 octet | ID driver de limbă |
| 30–31 | 2 octeți | Rezervat; umple cu 0 |
| 32–n [nota 3][nota 4] | 32 de octeți fiecare | matrice de descriptori de câmp (a se vedea mai jos pentru aspectul descriptorilor) |
| n + 1 | 1 octet | 0x0D ca terminator al matricei de descriptor de câmp |

- Funcția ISMARKEDO verifică acest flag (BEGIN TRANSACTION îl setează la 1, END TRANSACTION și ROLLBACK îl resetează la 0).
- Dacă acest indicator este setat la 1, apare mesajul Baza de date criptată.
- Numărul maxim de câmpuri este de 255.
- n înseamnă ultimul octet din matricea de descriptori de câmp.

### Matrice de descriptori de câmp
Aspectul descriptorilor de câmp în dBASE:

| octet | Cuprins | Înțeles |
---|---|---|
| 0–10 | 11 octeți | Numele câmpului în ASCII (complet cu zero) |
| 11 | 1 octet | Tipul câmpului. Valori permise: C, D, F, L, M sau N (a se vedea tabelul următor pentru semnificații) |
| 12–15 | 4 octeți | Rezervat |
| 16 | 1 octet | Lungimea câmpului în binar (maximum 254 (0xFE)). |
| 17 | 1 octet | Numărarea câmpurilor zecimale în binar |
| 18–19 | 2 octeți | ID zona de lucru |
| 20 | 1 octet | Exemplu |
| 21–30 | 10 octeți | Rezervat |
| 31 | 1 octet | Steagul câmp MDX de producție; 1 dacă câmpul are o etichetă index în fișierul MDX de producție, 0 dacă nu |

### Înregistrările bazei de date
Fiecare înregistrare începe cu un steag de ștergere (1-octet). Câmpurile sunt împachetate în înregistrări fără separatori de câmp. Toate datele de câmp sunt ASCII. În funcție de tipul câmpului, aplicația impune restricții suplimentare. Iată tipurile de câmpuri în dBase:

| Tip câmp | Mnemonic | Ce acceptă |
-------|-----|----|
| C | Personaj | Orice text ASCII (completat cu spații până la lungimea câmpului) |
| D | Data | Numere și un caracter pentru a separa luna, ziua și anul (stocate intern ca 8 cifre în format AAAAMMZZ) |
| F | virgulă flotantă | -, ., 0–9 (justificat la dreapta, umplut cu spații albe) |
| L | logic | Y, y, N, n, T, t, F, f sau ? (când este neinițializată) |
| M | Memo | Orice text ASCII (stocat intern ca 10 cifre reprezentând un număr de bloc .dbt, justificat la dreapta, completat cu spații albe) |
| N | Numeric | -, ., 0–9 (justificat la dreapta, umplut cu spații albe) |









## Referințe ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

