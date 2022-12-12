{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC – Format de fișier TrueType Collection",
  "description":"Un fișier TrueType Collection (TTC) combină mai multe fonturi într-un singur fișier. Atât Apple, cât și Microsoft au folosit TTF pe sistemele de operare Mac și Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Ce este un fișier TTC?
TTC este abreviat ca TrueType Collection este o extensie a formatului True Type. Un fișier TTC poate combina mai multe fișiere cu fonturi în el. Aceste fișiere sunt benefice pentru combinarea mai multor fonturi care au multe simboluri în comun. Înainte de Windows 2000, fișierele TTC erau folosite în versiunile Windows chineză, japoneză și coreeană, dar mai târziu suportul a fost disponibil pentru toate regiunile.


## Structura fișierului de colecție de fonturi
Un fișier TTC constă dintr-un tabel de antet TTC, directoare de tabel și mai multe tabele OpenType. Antetul TTC trebuie găsit la începutul fișierului. Trebuie să existe un director de tabel complet pentru fiecare font. Formatul TableDirectory ar trebui să fie similar cu cel a existat într-un fișier care nu este de colecție. Numărările tabelelor din toate directoarele dintr-un fișier TTC sunt calculate de la începutul unui fișier TTC.
Tabelele dintr-un fișier TTC sunt referite prin directorul de tabel al fonturilor respective. Câteva dintre tabelele OpenType trebuie să apară de mai multe ori, o dată pentru fiecare font adăugat în TTC. În timp ce celelalte tabele pot fi partajate de mai multe fonturi în fișierul TTC.

### Antet TTC
Două versiuni ale tabelului TTC Header sunt disponibile până acum:
- Versiunea 1.0 este utilizată pentru fișierele TTC fără semnături digitale.
- Versiunea 2.0 poate fi folosită pentru fișierele TTC cu sau fără semnături digitale.
Iată tabelele TTC Header ale ambelor versiuni:

**Versiunea antet TTC 1.0:**

|Tip|Nume|Descriere|
---|---|---|
|TAG|ttcTag|Șir ID colecție de fonturi: „ttcf” (utilizat pentru fonturi cu contururi CFF sau CFF2, precum și contururi TrueType)|
|uint16|majorVersion|Versiunea principală a antetului TTC, = 1.|
|uint16|minorVersion|Versiune minoră a antetului TTC, = 0.|
|uint32|numFonts|Numărul de fonturi în TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Matrice de offset-uri către TableDirectory pentru fiecare font de la începutul fișierului|

**Versiunea antet TTC 2.0:**

|Tip|Nume|Descriere|
---|---|---|
|TAG|ttcTag |Șir ID-ul colecției fonturilor: „ttcf”|
|uint16| majorVersion |Versiunea principală a antetului TTC, = 2.|
|uint16| minorVersion |Versiunea minoră a antetului TTC, = 0.|
|uint32| numFonts |Numărul de fonturi în TTC|
|Offset32| tableDirectoryOffsets[numFonts] |Matrice de offset-uri către TableDirectory pentru fiecare font de la începutul fișierului|
|uint32| dsigTag |Etichetă care indică faptul că există un tabel DSIG, 0x44534947 ('DSIG') (nulă dacă nu există semnătură)|
|uint32| dsigLength |Lungimea (în octeți) a tabelului DSIG (null dacă nu există semnătură)|
|uint32| dsigOffset |Decalajul (în octeți) a tabelului DSIG de la începutul fișierului TTC (null dacă nu există semnătură)|

## Referințe
* [Fișierul fontului OpenType](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

