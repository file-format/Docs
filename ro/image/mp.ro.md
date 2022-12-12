{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier MP - Fișier LaTeX MetaPost",
  "description":"Aflați despre formatul de fișier MP și despre API-urile care pot crea și deschide fișiere MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Ce este un fișier MP?

Un fișier MP este un fișier imagine vectorială generat de limbajul de programare MetaPost pentru a crea imagini. Imaginile vectoriale create folosind formatul de fișier MP sunt salvate ca fișiere [EPS](/ro/image/eps/) (Encapsulated PostScript). În plus, MetaPost vine distribuit cu cadre TeX și Metafont, iar fișierele MP pot fi generate din fișierele TEX și LTX utilizate de aceste aplicații. Fișierele MP conțin instrucțiuni de desen și desen algoritmic matematic pentru redarea fișierului EPS de ieșire. Motorul PDFTex poate folosi EPS creat pentru a genera direct fișiere [PDF](/ro/pdf/).

## Format de fișier MP

Fișierele MP sunt salvate pe disc ca fișiere binare și generează rezultate EPS atunci când sunt exportate în format de fișier imagine vectorială. Desenele create folosind MetaPost sunt incluse în formă formatată în documentele tehnice și publicațiile de jurnal create cu LaTex.

### Exemplu de fișier MetaPost MP

Urmează un exemplu, la care se face referire din [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), care conține o săgeată și litera „A” chiar deasupra mijlocului săgeată.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## Referințe ##

* [MetaPost de la Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Eșantion de latex Metapost de la Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

