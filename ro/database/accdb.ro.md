{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier ACCDB și despre API-urile care pot crea și deschide fișiere ACCDB.",
  "title" :"Format de fișier ACCDB - Fișierul bazei de date Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Ce este un fișier ACCDB?

Un fișier cu extensia .accdb este un fișier de bază de date Microsoft Access 2007 care stochează datele utilizatorilor în tabele. Suporta stocarea
formulare personalizate, interogări SQL și alte date. Fișierele ACCDB au înlocuit fișierele [MDB](/ro/database/mdb/) după ce Microsoft a trecut la structura fișierelor bazată pe XML. Fișierele ACCDB pot fi în continuare convertite în MDB cu compatibilitate veche. Cu toate acestea, ACCDB sunt formatul de fișier al bazei de date Access utilizat pe scară largă acum. Microsoft a acceptat, de asemenea, funcții suplimentare în format ACCDB, cum ar fi posibilitatea de a stoca fișiere atașate, date binare și suport pentru câmpuri cu valori multiple.

## Format de fișier ACCDB

La fel ca MDB, nu există specificații publice disponibile pentru formatul de fișier ACCDB. Microsoft acceptă accesarea programelor acestor fișiere prin standardul Open Database Connectivity (ODBC) și Visual Basic for Applications (VBA).

### O perspectivă

O imagine hexagonală a unui fișier ACCDB simplu sugerează că există asemănări generale în structură cu cele mai recente versiuni ale familiei de format MDB predecesoare. Ambele formate de fișiere folosesc dimensiuni fixe de pagină de 4096 de octeți. O altă similitudine între ACCDB și MDB este forma numărului magic, care include șirul „Standard ACE DB” pentru ACCDB. O versiune sau un cod de compatibilitate se află în aceeași locație în ambele formate. mdbtools | Fișierul HACKING afirmă „Offset 0x14 conține versiunea Jet a acestei baze de date” și Ghidul MDB neoficial este de acord. Informațiile din aceste surse, combinate cu intrarea Wikipedia pentru [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), sugerează că o valoare de 0x02 indică ACE 12 (Access 2007) și 0x03 indică ACE 14 (Acces 2010). Cu toate acestea, o bază de date minimă creată în Access 2010 și una similară creată în Access 2016 au ambele 0x02 în această locație. O bază de date minimă creată în Access 2016, dar care definea o coloană cu tipul de date „întreg mare” nou introdus, avea o valoare de 0x05. În fișierele ACCDB, acest indicator pare să reflecte compatibilitatea fișierului, mai degrabă decât versiunea motorului ACE utilizat pentru a-l crea.

## Referințe

* [Acces 2016 Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Motor de bază de date Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Ce format de fișier Access ar trebui să folosesc?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
