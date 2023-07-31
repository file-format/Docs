{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - Script de resurse compilat C++",
  "description":"Aflați despre formatul de fișier RES cu exemplu RES și API-uri care pot crea și deschide fișiere RES.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Ce este un fișier RES?
Fișierul cu sufix sau extensie .res poate aparține mai multor categorii de formate de fișiere. Aici discutăm despre formatul de fișier RES, care este un script de resurse compilat C++; un fișier binar creat de Microsoft Resource Compiler (rc) care conține date despre resurse; pe baza conținutului fișierului de definire a resursei; relevante pentru proiectul software-mamă. Fișierul .res este de obicei reformatat într-un fișier obiect resursă pentru a-l lega la fișierul executabil al unei aplicații.

## Format de fișier RES
Formatul de fișier RES aparține Microsoft Resource Compiler (rc). Compilatorul de resurse este un instrument care compilează resurse precum cursoare, pictograme, meniuri și casete de dialog, pe care le utilizează aplicația dvs. Fișierele de resurse au de obicei o extensie .res; conține resurse, cum ar fi cursore, imagini și informații despre versiune. Un fișier RES poate fi un fișier de resurse pe 16 sau 32 de biți.
## Structura fișierului de resurse
Un fișier de resurse conține o serie de diverse intrări de resurse. Fiecare intrare conține un antet de resursă și date relevante. Un antet de resurse este de obicei aliniat la DWORD în fișier și conține următoarele:

- Un **DWORD** pentru a specifica dimensiunea antetului resursei
- Un **DWORD** pentru a specifica dimensiunea datelor despre resurse
- Tipul de resursă
- Numele resursei
- Informații suplimentare despre resurse

Structura antetului resursei definește formatul fișierului RES. Datele pentru resursă urmează antetul resursei. Unele resurse adaugă, de asemenea, un model de antet de grup specific resurselor pentru a oferi informații despre un grup de resurse. Următoarele sunt câteva dintre tipurile de intrare de resurse și descrierea acestora:

### Resurse pentru tabelul acceleratorului
Un tabel accelerator este o intrare de resursă într-un fișier RES fără antet de grup. Modelul **ACCELTABLEENTRY** definește fiecare intrare din tabelul accelerator. Un fișier RES poate avea mai multe tabele acceleratoare.

### Resurse pentru cursor și pictograme
Deși, sistemul consideră fiecare pictogramă și cursor ca un singur fișier, dar acestea sunt stocate în fișierele RES ca un grup de resurse de pictograme sau un grup de resurse de cursor. Formatele de fișier ale resurselor pictogramei și cursorului sunt aceleași. Un antet de grup de resurse urmează toate componentele individuale ale pictogramelor sau ale grupului de cursor din fișierul .res.

### Resurse casetei de dialog
O casetă de dialog este, de asemenea, realizată ca o intrare de resursă în fișierul RES. Conține un model de antet al casetei de dialog **DLGTEMPLATE** și un model **DLGITEMTEMPLATE** pentru fiecare control specific din caseta de dialog. Modelele **DLGTEMPLATEEX** și **DLGITEMTEMPLATEEX** explică formatul resurselor casetei de dialog extinse.

### Resurse de fonturi
O resursă de meniu conține un model **MENUHEADER**, ulterior unul sau mai multe modele **NORMALMENUITEM** sau **POPUPMENUITEM**, câte unul pentru fiecare element de meniu din șablonul de meniu. Modelele **MENUEX_TEMPLATE_HEADER** și **MENUEX_TEMPLATE_ITEM** explică formatul resurselor meniului extins.

### Resurse pentru tabelul de mesaje
Un tabel de mesaje este format din text formatat pentru afișare ca mesaj de eroare sau într-o casetă de mesaj. Modelul principal dintr-o resursă de tabel de mesaje este structura **MESSAGE_RESOURCE_DATA**.

### Resurse versiuni
Modelul principal dintr-o resursă de versiune este **VS_FIXEDFILEINFO**. Modelele suplimentare includ **VarFileInfo** pentru a stoca date legate de informații despre limbă și **StringFileInfo** pentru informații despre șiruri personalizate.




## Referințe

* [Formate de fișiere de resurse](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



