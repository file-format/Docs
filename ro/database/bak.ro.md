{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "extensie", "fișier", "format fișier", "Tip fișier BAK", "Extensie fișier BAK", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier BAK și despre API-urile care pot crea și deschide fișiere BAK.",
  "title" :"Format de fișier BAK - fișier de rezervă a bazei de date",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Ce este un fișier BAK?

Un fișier cu extensia .bak este de obicei un fișier de rezervă care este utilizat de diferite instrumente software pentru a stoca copii de siguranță ale datelor. Din perspectiva bazei de date, un fișier BAK este utilizat de Microsoft SQL Server pentru stocarea conținutului unei baze de date. Toate datele și fișierele asociate cu baza de date sunt stocate în acest format de fișier pentru a fi preluate în cazul în care baza de date poate deveni coruptă sau invalidă din orice motiv. Fișierele de rezervă pot fi stocate și indexate pe alte servere din motive de siguranță. Mai multe aplicații pot crea fișiere BAK, cum ar fi SQL Server Management Studio, Transact-SQL și Windows PowerShell.

## Format de fișier BAK

Detaliile interne ale unui fișier BAK nu sunt cunoscute, dar se presupune că se bazează pe formatul de bandă Microsoft (MTF). Specificațiile MTF sunt disponibile și pot fi consultate pentru înțelegerea structurii fișierului. Documentul oferă detalii despre stocarea MTF pentru oricine are cunoștințe generale despre operațiunile de gestionare a stocării, unitățile de bandă și sistemele de fișiere.

### Seturi de date

Un set de date este o colecție de obiecte scrise pe un mediu de stocare (bandă, disc optic etc.) în timpul copierii sau restaurării datelor. Seturile de date cuprind mai multe medii în cazul unui volum mare de date.

### Elemente fundamentale ale MTF

Un fișier MTF constă din câteva elemente fundamentale care constituie blocurile sale de bază. Aceste elemente sunt:

#### Blocuri descriptori

Blocurile descriptori (DBLK) sunt folosite pentru controlul formatului și constituie bazele principale ale unui fișier MTF. Un singur fișier MTF definește mai multe DBLK pentru fiecare rol unic. Fiecare DBLK este un bloc de date cu lungime variabilă care este împărțit în următoarele patru părți:

* `Common Block Header` - Structură cu lungime fixă care este comună tuturor DBLK-urilor. Acesta este singurul Block Header care este necesar.
* `Informații despre tipul DBLK` - Bloc cu lungime fixă specific tipului de DBLK care este definit
* `Datele sistemului de operare` - Date specifice care sunt definite pe baza tipului de DBLK și a sistemelor de operare
* `Informații DBLK` - Informații specifice DBLK cu lungime variabilă care nu pot fi salvate cu informațiile DBLK cu lungime fixă.

 {{< figure src="../bak.png" alt="Format de fișier de rezervă Microsoft SQL" >}}

#### Flux de date

Fluxurile de date dintr-un fișier MTF sunt utilizate pentru încapsularea și alinierea datelor. Acesta cuprinde un antet de flux, urmat de Datele fluxului. Un antet de flux poate încapsula doar un singur tip de date de flux.

{{< figure src="../bak_datastream.png" alt="Format de fișier de rezervă Microsoft SQL" >}}

#### FileMarks

Un marcaj de fișier este utilizat pentru separarea logică și accesul rapid într-un mediu media. Marcajele de fișiere sunt emulate de driverul de dispozitiv sau prin utilizarea blocului Descriptor de fișiere soft în cazul în care dispozitivul utilizat nu oferă mărci de fișiere.

## Referințe ##

* [[MS-BCP]: Format de copiere în bloc](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5?redirectedfrom=MSDN)

