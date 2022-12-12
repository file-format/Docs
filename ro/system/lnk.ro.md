{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "extensie", "fișier", "format", "sistem", "fișier LNK", "link", "fișiere LNK", "documente LNK", "aplicație", "programe"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Format fișier de legătură",
  "description":"Aflați despre formatul de fișier LNK și despre API-urile care pot crea și deschide fișiere LNK.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Ce este un fișier LNK? ##

Un fișier LNK, analog unei identități pe sistemul Mac, este o alternativă sau „link” Windows care servește ca conexiune la un folder sau un program original de documente imagine. Acesta conține tipul, poziția și numele fișierului destinației comenzii rapide, precum și aplicația care deschide documentul țintă și o tastă de comandă rapidă suplimentară.

În Windows, direct un fișier, folder sau program executabil și alegeți Creare comandă rapidă. Locația formatului de fișier și directorul „Început” sunt două caracteristici de bază ale fișierelor LNK. Formatul de fișier al fișierelor LNK este mascat, iar o săgeată curbă indică faptul că acestea sunt comenzi rapide.

## Format fișier LNK ##

Formatele de fișiere LNK au, de obicei, aceeași pictogramă ca și fișierele de destinație, dar cu adăugarea unei mici săgeți ondulate pentru a arăta că fișierul indică o locație diferită. Când se face dublu clic pe scurtătura, se comportă ca și cum utilizatorul ar fi făcut dublu clic pe fișierul real.

Fișierele LNK care conțin comenzi rapide pentru aplicații pot avea proprietăți care afectează modul în care rulează programul. Pentru a modifica atributele, faceți clic dreapta pe fișierul de comandă rapidă și alegeți **Proprietăți**, apoi modificați câmpul Țintă.

În loc să fie extensii de fișiere, fișierele LNK sunt extensii Windows Explorer. Ca extensie de terminal, documentele .lnk pot fi folosite doar în Windows Explorer pentru a înlocui un fișier și au alte scopuri în Windows Explorer, pe lângă faptul că servesc ca scurtătură către un document local. Aceste fișiere încep și cu litera „L”.

În timp ce comenzile rapide leagă la anumite fișiere și directoare atunci când sunt create, acestea pot deveni inoperabile dacă ținta este schimbată într-o locație diferită. Explorer va începe să repare un folder de comenzi rapide care indică o țintă moartă atunci când este deschis.


## Specificatii tehnice ##

Numai când setarea de vizualizare a folderului „Ascundeți extensiile pentru tipurile de fișiere recunoscute” este debifată, Windows nu afișează extensia de document .lnk pentru comenzile rapide pentru documente. Deși nu este recomandat, puteți activa afișarea extensiei de fișier eliminând proprietatea „NeverShowExt” din elementul de registry Windows HKEY_CLASSES_ROOT\lnk.

Pentru a face acest lucru, urmați acești pași:

* Deschideți „Editor de înregistrare” introducând „Regedit” în câmpul de căutare din bara de activități și alegând programul
* În aplicație, navigați la locația Computer\HKEY HKEY_CLASSES_ROOT\lnkfile
* Faceți o copie de rezervă a articolului făcând clic dreapta pe el și alegând Export
* Selectați și ștergeți atributul „NeverShowExt”.
* Windows ar trebui repornit


## Referință ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
