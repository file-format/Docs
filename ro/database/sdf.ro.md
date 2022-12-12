{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "fișier sdf", "ce este fișierul sdf", "cum se deschide un fișier sdf", "extensie", "fișier", "format fișier sdf", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere baze de date" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier SDF și despre API-urile care pot crea și deschide fișiere SDF.",
  "title" :"SDF - Fișierul bazei de date SQL Server Compact",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Ce este un fișier SDF?
Un fișier cu extensia .sdf conține baza de date Microsoft SQL Server Compact (SQL CE), care este cunoscută și ca bază de date relațională compactă; produs de Microsoft pentru aplicațiile realizate pentru dispozitive mobile și desktop. Suportă atât sistemul de operare pe 32, cât și pe 64 de biți, iar conținutul complet al bazei de date este inclus într-un singur fișier SDF și poate ocupa mai mult de 4 GB spațiu pe disc. Din motive de securitate, un fișier .sdf poate fi criptat cu criptare pe 128 de biți. Runtime-ul SQL CE stabilește accesul multi-utilizator paralel la fișierul .sdf. Fișierul SDF poate fi copiat prin **QuickOnce** sau pur și simplu poate fi copiat la destinație pentru implementarea sistemului.

## Format de fișier SDF
Un fișier SDF conține o bază de date care este de obicei numită bază de date relațională compactă. Un fișier SDF conține toate informațiile legate de baza de date, iar SQL Server Compact este un motor de bază de date ușor și gratuit, care este utilizat pentru a gestiona fișierele .sdf. Dimensiunea fișierului .sdf nu trebuie să depășească limita de 4 GB. Fișierele SDF nu stochează informații despre procedurile stocate, declanșatoare sau vizualizări. Aplicațiile care utilizează o bază de date SQL CE nu trebuie să specifice calea către un fișier SDF în șirul de conexiune ADO.NET, ci poate fi menționat ca |DataDirectory|\database_name.sdf, definind directorul de date fiind definit în manifestul de asamblare pentru aplicație
Convenția de denumire .sdf este opțională și orice extensie poate fi folosită pentru a salva fișierul. Configurarea unei parole pentru fișierul bazei de date este un pas opțional. Pentru a comprima sau repara baza de date, fișierul trebuie salvat cu opțiunea **bază de date compactată/reparată**.

## Referințe

* [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Utilizarea SQL Server Compact pentru aplicații web ASP.NET](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


