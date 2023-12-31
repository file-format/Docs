{
  "date" : "2019-10-11",
  "keywords" :[ "fișier u3d", "format fișier u3d", "ce este un fișier u3d", "fișier", "exemplu u3d", "extensie fișier u3d", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title":"U3D – Format de fișier 3D universal",
  "description":"Aflați despre formatul de fișier U3D și despre API-urile care pot deschide și crea fișiere U3D.",
  "linktitle":"U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier U3D?

**U3D** (Universal 3D) este un format de fișier comprimat și o structură de date pentru grafica 3D pe computer. Conține informații despre modelul 3D, cum ar fi rețele triunghiulare, iluminare, umbrire, date de mișcare, linii și puncte cu culoare și structură. Formatul a fost acceptat ca standard [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) în august 2005. Documentele 3D [PDF](/ro/pdf/) acceptă U3D încorporarea obiectelor și poate fi vizualizată în Adobe Reader (versiunea 7 și ulterioară).

Formatul U3D a fost dezvoltat având în vedere scopul de a stabili un standard universal pentru stocarea și schimbul de date tridimensionale. Cu toate acestea, formatul își găsește principala utilizare în codificarea pentru PDF 3D, mai degrabă decât ca format de schimb. Acrobat 3D convertește un tip de fișier 3D acceptat fie în U3D, fie în PRC la conversia în PDF.

## Format de fișier U3D

Fișierele U3D sunt în format de fișier binar care a suferit patru ediții, așa cum este descris de documentul de referință ECMA-363, rezultând actualizarea specificațiilor cu fiecare ediție. Standardul de fișier PDF ISO-32000 acceptă U3D ca adnotare și tip multimedia permis.

Prima ediție a U3D a fost concentrată pe reprezentările cheie ale proprietăților grafice 3D, cum ar fi geometria, culoarea, texturile, iluminarea, oasele și animația bazată pe transformări. Ediția a doua și a treia au corectat unele erori în prima ediție, versiunea a treia fiind tipul cel mai frecvent utilizat în software-ul industrial. A patra ediție oferă definiții pentru primitive de ordin superior (suprafețe curbe). Specificațiile U3D sunt disponibile online pentru referință de utilizator pe site-ul web ECMA.

### Tipuri de date în fișierele U3D

Fișierul binar va conține următoarele tipuri: U8, U16, U32, U64, I16, I32, F32, F64 și String.

* U8: Un întreg fără semn de 8 biți
* U16: un număr întreg de 16 biți fără semn
* U32 : un întreg fără semn pe 32 de biți
* U64: un întreg fără semn pe 64 de biți
* I16 : Un întreg cu semn de 16 biți
* F32: Un float de precizie unică IEEE.
* F64: Un float de precizie dublă IEEE.
* Șir: șirurile dintr-un fișier U3D încep cu un număr întreg nesemnat de 16 biți care definește lungimea totală a caracterelor din șir. Șirurile sunt întotdeauna procesate ca fiind sensibile la majuscule și minuscule.

## Structura fișierului U3D

Un fișier U3D conține o secvență de blocuri. Există 3 tipuri diferite de bloc în fiecare fișier U3D.

* Bloc antet fișier
* Bloc de declarații
* Bloc de continuare

Încărcătorul determină sfârșitul unui bloc dacă datele din acel bloc nu sunt necesare sau dacă nu este disponibil un decodor pentru acel tip de bloc.

{{<figure src="../u3d.png" alt="Format de fișier U3D">}}

### Bloc Antet fișier
Un bloc de antet de fișier conține informații despre fișier care sunt utilizate de către cei încărcați pentru a determina cum să citească fișierul.

### Bloc de declarație

Blocurile de declarație conțin informații despre obiectele din fișier. Obiectele dintr-un bloc de declarare trebuie definite.

### Bloc de continuare

Informații suplimentare pentru obiectele declarate într-un bloc Declarație sunt furnizate în blocul de continuare. Fiecare bloc de continuare trebuie să fie asociat cu un bloc de declarație.

## Referințe

* [Format de fișier U3D - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [Specificații de format de fișier ECMA U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)