{
  "date" : "2021-02-25",
  "keywords" :[ "file bdf", "formato file bdf", "cos'è un file bdf", "file", "esempio bdf", "estensione file bdf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Formato di distribuzione bitmap glifo",
  "description":"Scopri il formato di file BDF e le API che possono creare e aprire file BDF.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Che cos'è un file BDF?
I file BDF sono in forma leggibile dall'uomo e generalmente distribuiti in una codifica ASCII. Il file inizia con le informazioni globali relative al carattere completo, seguite dalle informazioni e dalle bitmap per i glifi individuali. I dati in esso contenuti vengono mostrati per il carattere per un orientamento a dimensione singola. Le metriche da utilizzare in più direzioni possono essere comprese in un unico file. Nel file BDF, ogni elemento è contenuto su una riga di testo separata nel file. Gli spazi vengono utilizzati per separare gli elementi su una riga.

## Formato file BDF
I cortometraggi BDF per Glyph Bitmap Distribution Format; di proprietà di Adobe è un formato di file per il salvataggio di caratteri di tipo bitmap. Il contenuto assume la forma di un file di testo destinato a essere leggibile dal computer e dall'uomo. Il BDF è particolarmente utilizzato negli ambienti Unix X Window. È stato ampiamente sostituito dal formato dei caratteri PCF che dovrebbe essere più efficiente e dai caratteri OpenType e TrueType.
### Struttura del file BDF
Un file di font BDF è composto da tre sezioni:

- una sezione globale che si applica a tutti i glifi in un font.
- una sezione con una voce separata per ogni glifo.
- l'istruzione ENDFONT.

## Esempio
Ecco un esempio di font contenente un glifo, per la 'A' maiuscola ASCII. Le sue dichiarazioni globali iniziano con la riga "STARTFONT" e terminano con la riga "CHARS".
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



## Riferimenti
* [Formato di distribuzione bitmap glifi](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Specifica Glyph Bitmap Distribution Format (BDF)](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

