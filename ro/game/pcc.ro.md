{
  "date" : "2021-09-08",
  "keywords" :[ "fișier pcc", "format fișier pcc", "ce este un fișier pcc", "fișier", "exemplu pcc", "extensie fișier pcc", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier PCC Mass Effect și despre API-urile care pot crea și deschide fișiere PCC.",
  "title" :"PCC - Fișier pachet Mass Effect",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Ce este un fișier PCC?

Un fișier cu .pcc este un fișier [Joc Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3) care conține date despre joc pentru a modifica conținutul jocului, cum ar fi modele, texturi și camere. Mass Effect 2 și 3 sunt primele jocuri cu împușcături bazate pe motorul de jocuri Unreal Engine 3. Jocul a fost dezvoltat inițial de [Bioware](https://www.bioware.com/about/) care a păstrat majoritatea resurselor jocului în formatul de fișier PCC proprietar. Bioware a fost achiziționat de Electronic Arts, un important editor mondial de divertisment interactiv.

## Format de fișier PCC - Mai multe informații

Fișierele PCC conțin structuri comprimate și/sau necomprimate care contribuie la organizarea generală a fișierelor.

### Structură PCC comprimată

Un fișier PCC comprimat este format din tabele și date care sunt segmentate în bucăți. Fiecare bucată conține un număr variabil de blocuri comprimate.

* `Chunks Header` - Un antet comun de 16 octeți, care conține informații despre fragmente.
* `Chunk Header` - Un antet de 16 octeți care conține informații despre datele brute comprimate conținute în formularul bloc.

### Structură PCC necomprimată

Fișierele PCC necomprimate sunt împărțite în următoarele cinci părți.

* `Header` - conține informații de bază despre structura fișierului PCC.
* `Name Table` - conține numele găsit în pachet, inclusiv clase de import, exporturi și proprietăți de export.
* `Import Table` - conține toate clasele și obiectele importate de PCC.
* `Export Table` - conține toate obiectele stocate în pachet. Fiecare export poate varia în dimensiune.

## Referințe

* [Me3Explorer - Format de fișier PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Joc Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

