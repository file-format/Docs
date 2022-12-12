{
  "date" : "2021-02-10",
  "keywords" :[ "fișier jpx", "format fișier jpx", "ce este un fișier jpx", "fișier", "exemplu jpx", "extensie fișier jpx", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Format fișier imagine",
  "description":"Aflați despre formatul de fișier JPX și despre API-urile care pot crea și deschide fișiere JPX.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Ce este un fișier JPX? ##

Un fișier cu extensia .jpx este o extensie a formatului de fișier JPEG 2000. Utilizează în primul rând compresia JPEG 2000 și oferă, de asemenea, funcții avansate, cum ar fi mai multe straturi pentru o imagine, diferite spații de culoare, opacitate și fluxuri de cod fragmentate. JPX permite și alte compresii, cum ar fi JBIG, CCITT Group3, CCITT Group4 etc., în plus față de compresia JPEG 2000. Formatul de fișier JPX a fost aprobat ca standard [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html), dar nu a putut primi o recepție caldă din cauza utilizării extinse a [JPEG ](/ro/image/jpeg/) format de fișier. Aplicațiile care pot deschide fișiere JPX includ Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 și CorelDraw Graphics Suite 2020.

## Scurt istoric

În 2000, comitetul Joint Photographic Experts Group a proiectat JP2 cu obiectivul de a-și îmbunătăți propriul standard JPEG bazat pe transformarea cosinusului discret cu această nouă metodă bazată pe wavelet. Comitetul JPEG și-a propus să ofere metodele de bază fără taxe de licență. în licența JP2, câștigând concurență între 20 de companii, au câștigat cu o mustață. JPEG 2000 a fost declarat ca standard ISO, deși majoritatea browserelor web nu sunt pregătite să dea o mână de ajutor JPEG 2000 din 2017. În 2004, formatul ISO/IEC 15444-2 a fost acceptat public ca extensie a formatului de fișier JP2.

## Format de fișier JPX

Formatul de fișier JPX a fost formulat pentru a îndeplini cerințele aplicațiilor care aveau nevoie de structuri de date dincolo de funcționalitatea definită de formatul de fișier [JP2](/ro/image/jp2/). Un fișier JP2 cu extensii incompatibile ar putea duce la confuzie pe piață, unde unii cititori pot interpreta unele fișiere JP2, dar nu altele. JPX este răspunsul pentru evitarea unor astfel de probleme în aplicații.

### Identificarea fișierului

Fișierele JPX sunt stocate ca [JPF](/ro/image/jpf/) atunci când sunt stocate în sistemul de fișiere tradițional al computerului. De aceea, termenul JPX este cel mai puțin utilizat în comparație cu JPF. Un fișier JPX începe cu următorii octeți:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Organizarea fișierelor

Similar cu JP2, un fișier JPX este o colecție de casete având o structură binară, cu casetele aranjate într-o ordine adiacentă. Prima casetă oferă începutul fișierului cu primul său octet, iar ultimul octet al ultimei casete reprezintă ultimul octet al fișierului.
Structura binară a unei casete dintr-un fișier JPX este identică cu cea definită în formatul de fișier [JP2](/ro/image/jp2/).

### Stocarea CodeStream în JPX

Formatul de fișier JPX permite ca fluxul de cod al imaginii să fie împărțit în fragmente. Acest lucru face posibilă modificarea unei singure plăci a imaginii și scrierea plăcii modificate la sfârșitul fișierului fără a rescrie întregul fișier. Formatul original de fișier [JP2](/ro/image/jp2/) restricționează întregul flux de cod pentru a fi stocat într-o porțiune adiacentă a fișierului, ceea ce poate fi problematic pentru aplicațiile de editare a imaginilor care ar putea dori să modifice o singură dală a imaginii și să obțină suportabilitatea de mai sus prin formatul de fișier JPX. Fragmentarea fluxului de cod al imaginii face ca formatul de fișier JPX să fie superior față de formatul de fișier JP2. În plus, formatul de fișier JPX permite combinarea mai multor fluxuri de cod și producerea unui rezultat redat. Codestream-urile pot fi combinate ca compoziție și animație.

## Referințe ##

* [Prezentare generală despre JPEG 2000](https://jpeg.org/jpeg2000)

