{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier 4DL și despre API-urile care pot crea și deschide fișiere 4DL.",
  "title" :"4DL - Fișier jurnal al bazei de date a 4-a dimensiune",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-06-14"
}

## Ce este un fișier 4DL?

Un fișier jurnal 4DL este utilizat pentru a înregistra modificările aduse unui fișier de bază de date 4D (.4DD). Acest fișier este stocat alături de fișierul bazei de date și partajează un nume de fișier similar. Scopul său este de a urmări cu acuratețe și de a menține o evidență cuprinzătoare a actualizărilor implementate în baza de date. Un [fișier 4DD](/ro/database/4dd/), în comparație cu fișierul 4DL, este asociat în principal cu 4th Dimensions de către 4D Inc.

## Format de fișier 4DL - Mai multe informații

De obicei, mai multe fișiere 4DL sunt stocate împreună cu un fișier 4DD. Astfel, prima versiune a fișierului jurnal poate fi numită ca 0001.4dl, dar versiunile laterale ale fișierelor jurnal vor fi salvate ca 0002.4dl, 0003.4dl și așa mai departe. Acum, dacă fișierul jurnal în sine suferă 3 salvări ulterioare, acesta va fi etichetat ca "db1[0005-0003].4dl".

## Referințe

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))
