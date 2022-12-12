{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier NPK",
  "description":"Aflați despre formatul de fișier NPK și despre API-urile care pot crea și deschide fișiere NPK.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Ce este un fișier NPK?

Un fișier NPK este un fișier de pachet de upgrade software utilizat de routerele **MikroTik** pentru actualizarea sistemului de operare al routerului. Vine ca o arhivă binară comprimată care este încărcată în router pentru instalarea actualizărilor software. Informațiile conținute în fișierele NPK includ informații de rețea, cum ar fi adresa IP și serviciul IP, informații despre conectori (interfețe Ethernet și portul serial), configurarea e-mailului, configurarea podului și gestionarea locală a utilizatorilor.

## Format de fișier NPK

Fișierele NPK sunt stocate ca arhivă binară comprimată. Este un format de fișier închis care este folosit doar de MikroTik înșiși. Nu este destinat să creeze suplimente RouterOS prin terțe părți. Fișierele NPK sunt întreținute chiar de MikroTik și versiunile actualizate ale acestora pot fi descărcate din secțiunile de descărcare ale site-ului [MikroTik](https://mikrotik.com/download).

Când un fișier NPK este încărcat pe un router, sistemul de operare al routerului nu intră în vigoare decât dacă este repornit. Prin urmare, este necesară o repornire pentru ca sistemul de operare al routerului să fie actualizat.

## Referințe

* [MikroTik - Actualizarea sistemului de operare al routerului](https://mikrotik.com/download)
* [Cum se creează fișiere NPK](https://forum.mikrotik.com/viewtopic.php?t=87126)

