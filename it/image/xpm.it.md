{
  "date" : "2019-10-11",
  "keywords" :[ "file xpm", "formato file xpm", "cos'è un file xpm", "file", "esempio xpm", "estensione file xpm", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - Formato file X PixMap",
  "description":"Scopri il formato di file XPM e le API che possono creare e aprire file XPM.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file XPM?

Un file con estensione .xpm è un formato di file immagine utilizzato dal sistema X Windows. Supporta pixel trasparenti e di solito mira a creare pixmap di icone. Supporta dati pixmap monocromatici, in scala graduata ea colori. Questi sono stati progettati per essere modificabili a mano e possono essere inclusi nel codice [C](/it/programming/c/). A tale scopo, i file XPM sono in formato di file di testo normale e seguono la sintassi del linguaggio di programmazione C. I file XPM possono essere aperti con una varietà di applicazioni di visualizzazione di immagini come
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView e Canvas X.

## Formato file XPM

Il formato di file XPM utilizza la sintassi C per integrarli nei programmi C e C++. Si compone delle seguenti sei diverse sezioni.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Le sezioni sono in realtà una matrice di stringhe come segue.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Di seguito i dettagli di ciascuna sezione.

`<Values> ` - Questa sezione è una stringa che contiene quattro o sei numeri interi che sono in base 10 e corrispondono a:

* larghezza e altezza della pixmap
* numero di colori
* numero di caratteri per pixel
* coordinate hotspot opzionali e tag XPMEXT

`<Colors> ` - Questa sezione contiene tante stringhe quanti sono i colori. Ogni stringa è la seguente:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Questa sezione è composta da<height> stringhe e<width> \*<chars_per_pixel> personaggi. Ogni<chars_per_pixel> la stringa di lunghezza dovrebbe essere uno dei gruppi precedentemente definiti in<Colors> sezione.

`<Extension> ` - La sezione dell'estensione deve essere etichettata, se non è vuota, nel file<Values> sezione. Può essere composto da diversi<Extension> sottosezioni che possono essere dei seguenti due tipi:

* una stringa stand alone composta come segue: XPMEXT<extension-name><extension-data>
* o un blocco composto da più stringhe:XPMEXT<extension-name><related extension-data composed of several strings>

## Riferimenti

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [Manuale XPM](http://www.xfree86.org/current/xpm.pdf)

