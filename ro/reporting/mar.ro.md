{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Fișier de rapoarte Microsoft Access",
  "keywords" :[ "mar", "fișier mar", "format fișier mar", "ce este raportul de acces", "raportul de acces", "raportul de acces Microsoft"],
  "description":"Aflați despre formatul de fișier Acess Report (MAR) utilizat de software-ul Microsoft Access pentru a crea o comandă rapidă sau o legătură către Microsoft Access Report.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Ce este Raportul de acces (fișier MAR)? ##
Un fișier creat de Microsoft Access ca o comandă rapidă a raportului său este salvat cu extensia de fișier .mar. Un **raport Microsoft Access** oferă o modalitate de a formata, vizualiza și rezuma informațiile din baza de date Microsoft Access. Aceste rapoarte vă permit să formatați datele într-un aspect precis și informativ pentru vizualizare pe ecran sau printare. Raportul afișează doar datele statice, ceea ce înseamnă că nu putem modifica datele din tabele atunci când vedem raportul Access. Raportul afișează cele mai recente date când este deschis.

## Format de fișier Microsoft Access Report (MAR).

Formatul de fișier MAR este utilizat de software-ul Microsoft Access pentru a crea o comandă rapidă sau o legătură către Microsoft Access Report, care este un obiect de bază de date care devine util atunci când trebuie să prezentați informațiile din baza de date pentru oricare dintre următoarele utilizări:

- Afișați un rezumat al datelor.
- Arhivați instantanee ale datelor.
- Afișați detalii despre înregistrările individuale.
- Creați etichete.

## Părți ale raportului de acces
Designul unui raport de acces este împărțit în diferite secțiuni care pot fi vizualizate în vizualizarea Design. Următorul tabel explică modul în care funcționează și poate fiecare secțiune vă ajută să creați rapoarte.
| Sectiunea | Cum este afișată secțiunea la imprimare | Unde poate fi folosită secțiunea |
---------|----|------|
| Antet raport | La începutul raportului. | Utilizați antetul raportului pentru informații care ar putea apărea în mod normal pe o pagină de copertă, cum ar fi o siglă, un titlu sau o dată. Când plasați un control calculat care utilizează funcția Sumă agregată în antetul raportului, suma calculată este pentru întregul raport. Antetul raportului este tipărit înaintea antetului paginii. |
| Antet pagină | În partea de sus a fiecărei pagini. | Utilizați un antet de pagină pentru a repeta titlul raportului pe fiecare pagină. |
| Antet grup | La începutul fiecărui nou grup de înregistrări. | Utilizați antetul grupului pentru a tipări numele grupului. De exemplu, într-un raport care este grupat după produs, utilizați antetul grupului pentru a tipări numele produsului. Când plasați un control calculat care utilizează funcția de agregare Sum în antetul grupului, suma este pentru grupul curent. Puteți avea mai multe secțiuni de antet de grup într-un raport, în funcție de câte niveluri de grupare ați adăugat. Pentru mai multe informații despre crearea antetelor și subsolurilor de grup, consultați secțiunea Adăugați grupări, sortare sau totaluri. |
| Detaliu | Apare o dată pentru fiecare rând din sursa de înregistrare. | Aici plasați controalele care alcătuiesc corpul principal al raportului. |
| Subsol grup | La sfârşitul fiecărui grup de înregistrări. | Utilizați un subsol de grup pentru a imprima informații rezumate pentru un grup. Puteți avea mai multe secțiuni de subsol de grup într-un raport, în funcție de câte niveluri de grupare ați adăugat. |
| Subsolul paginii | La sfârșitul fiecărei pagini. | Utilizați un subsol de pagină pentru a imprima numerele de pagină sau informații pe pagină. |
| Subsolul raportului | La finalul raportului. Notă: în vizualizarea Design, subsolul raportului apare sub subsolul paginii. Cu toate acestea, în toate celelalte vizualizări (vizualizarea Layout, de exemplu, sau când raportul este tipărit sau previzualizat), subsolul raportului apare deasupra subsolului paginii, imediat după ultimul subsol de grup sau linie de detaliu de pe pagina finală. | Utilizați subsolul raportului pentru a imprima totalurile raportului sau alte informații rezumative pentru întregul raport. |






## Referințe ##

- [Introducere în rapoartele în Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Proiectarea rapoartelor în acces](https://www.uis.edu/informationtechnologyservices/wp-content/uploads/sites/106/2013/04/DesigningReportsinAccess2010.pdf)

