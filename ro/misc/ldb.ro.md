{
"data": "2023-04-20",
  "keywords": [
"fișier ldb",
"Ce este un fișier ldb",
"ce informații conține ldb",
"care este scopul fișierului ldb",
"extensie ldb",
"fişier",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format fișier LDB - Fișier de blocare Microsoft Access",
  "description":"Aflați despre formatul LDB și ce informații conține acesta.",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
      "parent": "misc"
}
},
"lastmod": "2023-04-20"
}

## Ce este un fișier LDB?

Un fișier LDB este un fișier de blocare utilizat de Microsoft Access pentru a împiedica mai mulți utilizatori să editeze aceeași bază de date simultan. Când utilizatorul deschide o bază de date Access, Access creează un fișier LDB corespunzător în același director cu baza de date. Acest fișier conține informații despre cine utilizează în prezent baza de date și ce înregistrări editează.

Fișierul LDB este creat automat de Microsoft Access atunci când baza de date este deschisă și este șters când baza de date este închisă. Este important de reținut că fișierul LDB nu trebuie niciodată șters manual, deoarece acest lucru poate cauza probleme cu baza de date.

Dacă întâmpinați probleme cu baza de date Microsoft Access, o soluție potențială este să încercați să ștergeți fișierul LDB asociat cu acea bază de date. Acest lucru va elibera orice blocaje care vă pot împiedica să accesați baza de date. Cu toate acestea, asigurați-vă că faceți o copie de rezervă a bazei de date înainte de a încerca acest lucru, deoarece ștergerea fișierului LDB poate provoca pierderea sau coruperea datelor dacă este făcută incorect.

## Format de fișier LDB - Mai multe informații

Un fișier LDB din Microsoft Access conține informații despre utilizatorii care accesează în prezent baza de date, cum ar fi numele lor de utilizator, numele computerului și ora de conectare. Fișierul LDB conține, de asemenea, informații despre orice încuietori care au fost plasate în baza de date, cum ar fi ce înregistrări sunt editate de către ce utilizator.

Iată o listă mai detaliată a tipurilor de informații care pot fi găsite într-un fișier LDB:

- **Nume utilizator** - numele utilizatorului care accesează în prezent baza de date
- **Nume computer** - numele computerului de unde utilizatorul accesează baza de date
- **Timp de conectare** - ora la care utilizatorul a deschis prima data baza de date
- **Blocarea înregistrărilor** - informații despre ce înregistrări sunt editate în prezent de către ce utilizator
- **Blocarea obiectelor** - informații despre obiectele bazei de date (cum ar fi tabele, formulare sau rapoarte) care sunt editate în prezent de către ce utilizator
- **Informații de conexiune** - informații despre modul în care utilizatorul este conectat la baza de date (de exemplu, dacă utilizează o conexiune locală sau de rețea)

Informațiile din fișierul LDB sunt utilizate de Microsoft Access pentru a preveni mai mulți utilizatori să facă modificări conflictuale în aceeași bază de date în același timp. Când utilizatorul încearcă să editeze o înregistrare sau un obiect care este deja blocat de un alt utilizator, Microsoft Access va afișa un mesaj care indică faptul că obiectul este deja în uz. Fișierul LDB este actualizat pe măsură ce utilizatorii deschid și închid baza de date și fac modificări obiectelor blocate.

## Referințe
* [Ce este un fișier LDB?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

