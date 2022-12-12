{
  "date" : "2019-10-11",
  "keywords" :[ "fișier xpm", "format fișier xpm", "ce este un fișier xpm", "fișier", "exemplu xpm", "extensie fișier xpm", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - Format de fișier X PixMap",
  "description":"Aflați despre formatul de fișier XPM și despre API-urile care pot crea și deschide fișiere XPM.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier XPM?

Un fișier cu extensia .xpm este un format de fișier imagine care a fost folosit de sistemul X Windows. Acceptă pixeli transparenți și, de obicei, vizează crearea de pictograme pictograme. Acceptă date pixmap monocrome, gra-scale și color. Acestea au fost concepute pentru a fi editabile manual și pot fi incluse în codul [C](/ro/programming/c/). În acest scop, fișierele XPM sunt în format text simplu și urmează sintaxa limbajului de programare C. Fișierele XPM pot fi deschise cu o varietate de aplicații de vizualizare a imaginilor, cum ar fi
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView și Canvas X.

## Format de fișier XPM

Formatul de fișier XPM utilizează sintaxa C pentru ca acestea să fie integrate în programele C și C++. Este format din următoarele șase secțiuni diferite.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Secțiunile sunt de fapt o matrice de șiruri, după cum urmează.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Mai jos sunt detaliile fiecărei secțiuni.

`<Values> ` - Această secțiune este un șir care conține patru sau șase numere întregi care sunt în baza 10 și corespund:

* lățimea și înălțimea hărții de pixeli
* numărul de culori
* numărul de caractere pe pixel
* coordonatele hotspot opționale și eticheta XPMEXT

`<Colors> ` - Această secțiune conține atâtea șiruri câte culori există. Fiecare șir este după cum urmează:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Această secțiune este compusă din<height> șiruri și<width> \*<chars_per_pixel> personaje. Fiecare<chars_per_pixel> șirul de lungime ar trebui să fie unul dintre grupurile definite anterior în<Colors> secțiune.

`<Extension> ` - Secțiunea de extensie trebuie să fie etichetată, dacă nu este goală, în<Values> secțiune. Poate consta din mai multe<Extension> subsecțiuni care pot fi de următoarele două tipuri:

* un șir independent compus după cum urmează: XPMEXT<extension-name><extension-data>
* sau un bloc compus din mai multe șiruri:XPMEXT<extension-name><related extension-data composed of several strings>

## Referințe

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [Manual XPM](http://www.xfree86.org/current/xpm.pdf)

