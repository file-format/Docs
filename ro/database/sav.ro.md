{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "extensie", "fișier sav", "format fișier sav", "Tipul fișierului bazei de date", "Format fișierului bazei de date", "ce este un fișier sav" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier SAV și despre API-urile care pot crea și deschide fișiere SAV.",
  "title" :"SAV - SPSS Data File",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Ce este un fișier SAV?
Fișierul SAV este un fișier de date creat de Pachetul Statistic pentru Științe Sociale (SPSS), care este o aplicație utilizată pe scară largă de cercetătorii de piață, cercetătorii în domeniul sănătății, companiile de anchetă, guvern, cercetătorii educației, organizațiile de marketing, minerii de date pentru analiză statistică. SAV salvat într-un format binar proprietar și constă dintr-un set de date, precum și un dicționar care reprezintă setul de date, salvează datele în rânduri și coloane.

## Format de fișier SAV
Formatul de fișier SAV a devenit relativ stabil, dar nu putem spune că este static. Compatibilitatea înapoi și înainte este disponibilă opțional acolo unde este necesar, dar nu este întreținută corespunzător. Datele dintr-un fișier SAV sunt clasificate în următoarele secțiuni:

### Antetul fișierului
Este format din 176 de octeți. Primii 4 octeți indică șirul **$FL2** sau **$FL3** în codificarea caracterelor utilizată pentru fișier. Ultimii trei octeți reprezintă faptul că datele din fișier sunt comprimate folosind **ZLIB**. Următorul șir de 60 de octeți începe **@(#) SPSS DATA FILE** și determină, de asemenea, sistemul de operare și versiunea SPSS care a creat fișierul. Antetul continuă apoi cu câmpuri de șase cifre, care conțin numărul de variabile per observație și un cod de cifre pentru compresie și se termină cu date de caractere care indică data și ora creării și o etichetă de fișier.
### Înregistrări de descriptori variabile
Înregistrarea conține o secvență fixă de câmpuri, clasificând tipul și numele variabilei împreună cu informațiile de formatare utilizate de SPSS. Fiecare înregistrare variabilă poate conține opțional o etichetă variabilă de până la 120 de caractere și până la trei specificații de valoare lipsă.
### Etichete de valoare
Etichetele valorii sunt opționale și stocate în perechi de înregistrări cu etichetele întregi 3 și 4. Prima înregistrare care este eticheta 3 are o secvență de perechi de câmpuri, fiecare pereche conținând o valoare și eticheta valorii asociată. A doua înregistrare, care este eticheta 4, reprezintă variabilele cărora li se aplică setul de valori/etichete.
### Documente
Înregistrări simple sau multiple cu etichetă întreg 6. Documentație opțională. conține linii de 80 de caractere.
### Înregistrări de extensie
Înregistrări unice sau multiple cu etichetă întreg 7. Înregistrările de extensie oferă informații care pot fi ignorate în siguranță, dar păstrate, în multe situații, permite fișierelor scrise de software-ul mai nou să păstreze compatibilitatea cu versiunea anterioară. Înregistrările de extensie au etichete de subtip întreg.
### Dicţionar terminator
Înregistrați numai cu eticheta întreg 999. Separă dicționarul de observațiile de date.
### Observații de date
Se consideră că datele sunt în ordinea observației, de exemplu toate valorile variabile pentru prima observație, urmate de toate valorile pentru a doua observație etc. Formatul înregistrării de date variază în funcție de codul de compresie din înregistrarea antetului fișierului. Porțiunea de date a unui fișier .sav poate fi decomprimată:
- **cod 0**: comprimat de bytecode
- **codul 1**: comprimat folosind compresia ZLIB
 







## Referințe ##

* [SPSS System Data File Format Family (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

