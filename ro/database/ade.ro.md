{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier ADE și despre API-urile care pot crea și deschide fișiere ADE.",
  "title" :"ADE - Accesați fișierul de extensie a proiectului",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Ce este un fișier ADE?

Un fișier cu extensia .ade este un fișier Microsoft Access Project care conține rezultatul compilat al informațiilor conținute în fișierul de proiect Microsoft Access ADP. Informațiile din fișierul de proiect Access, altele decât Visual Basic pentru aplicații (VBA), sunt disponibile în formă compilată în fișierele ADE. Datele sunt stocate în format comprimat în aceste fișiere pentru a reduce dimensiunea fișierului și a îmbunătăți performanța în Access. Deoarece ADE este ieșirea compilată a fișierului de proiect Access, orice cod sursă VBA care face parte din proiect rămâne protejat nepermițându-i să facă parte din ieșire. Fișierele ADE pot fi deschise în Microsoft Access 365.

## Format de fișier ADE - Mai multe informații

ADE sunt fișiere de bază de date Access compilate care sunt stocate pe disc ca fișiere binare. Structura internă a fișierelor acestor fișiere nu este cunoscută.

Fișierele ADE pot crea probleme la deschidere pe baza versiunii Microsoft Access care a fost utilizată pentru a crea aceste fișiere. Bazele de date Access care utilizează versiunea pe 64 de biți a Microsoft Access 2010 și care sunt compilate ca fișiere MDE, [ACCDE](/ro/database/accde/) sau ADE trebuie să fie recompilate în Microsoft Access 2021 Service Pack 1 (SP1) pentru funcționează corect cu Access 2010 SP1. Această problemă apare deoarece Access 2010 SP1 utilizează o versiune mai nouă a fișierului VBE7.dll (versiunea 7.00.1619).

## Referințe

* [Problemă cu fișierele Access ADE](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Ce formate de fișiere de acces să utilizați](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

