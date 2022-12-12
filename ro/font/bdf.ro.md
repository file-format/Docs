{
  "date" : "2021-02-25",
  "keywords" :[ "fișier bdf", "format fișier bdf", "ce este un fișier bdf", "fișier", "exemplu bdf", "extensie fișier bdf", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Format de distribuție a bitmapului Glyph",
  "description":"Aflați despre formatul de fișier BDF și despre API-urile care pot crea și deschide fișiere BDF.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Ce este un fișier BDF?
Fișierele BDF sunt în formă care poate fi citită de om și sunt distribuite de obicei într-o codificare ASCII. Fișierul începe cu informații globale relevante pentru fontul complet, urmate de informațiile și hărțile de biți pentru glifele individuale. Datele din acesta sunt afișate pentru font pentru o orientare cu o singură dimensiune. Valorile de utilizat în mai multe direcții pot fi cuprinse într-un singur fișier. În fișierul BDF, fiecare articol este conținut pe o linie separată de text în fișier. Spațiile sunt folosite pentru a separa elementele pe o linie.

## Format de fișier BDF
Shorts-urile BDF pentru Glyph Bitmap Distribution Format; deținut de Adobe este un format de fișier pentru salvarea fonturilor de tip bitmap. Conținutul ia forma unui fișier text destinat să fie citit de computer și uman. BDF este utilizat în special în mediile Unix X Window. Acesta a fost înlocuit pe scară largă de formatul de font PCF, care se presupune a fi mai eficient, și de fonturile OpenType și TrueType.
### Structura fișierului BDF
Un fișier cu font BDF este format din trei secțiuni:

- o secțiune globală care se aplică tuturor glifelor dintr-un font.
- o secțiune cu o intrare separată pentru fiecare glif.
- declarația ENDFONT.

## Exemplu
Iată un exemplu de font care conține un glif, pentru ASCII majusculă „A”. Declarațiile sale globale încep cu linia „STARTFONT” și se termină cu linia „CHARS”.
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Referințe
* [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Specificație Glyph Bitmap Distribution Format (BDF)](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

