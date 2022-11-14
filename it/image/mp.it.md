{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File MP - File MetaPost LaTeX",
  "description":"Scopri il formato di file MP e le API che possono creare e aprire file MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Che cos'è un file MP?

Un file MP è un file di immagine vettoriale generato dal linguaggio di programmazione MetaPost per creare immagini. Le immagini vettoriali create utilizzando il formato file MP vengono salvate come file [EPS](/it/image/eps/) (Encapsulated PostScript). Inoltre, MetaPost viene distribuito con i framework TeX e Metafont e i file MP possono essere generati dall'interno dei file TEX e LTX utilizzati da queste applicazioni. I file MP contengono istruzioni di disegno e disegni algoritmici matematici per il rendering del file EPS di output. Il motore PDFTex può utilizzare l'EPS creato per generare direttamente file [PDF](/it/pdf/).

## Formato file MP

I file MP vengono salvati su disco come file binari e generano output EPS quando vengono esportati in formato file immagine vettoriale di output. I disegni creati con MetaPost sono inclusi in forma formattata all'interno di documenti tecnici e pubblicazioni di riviste create con LaTex.

### Esempio di file MP MetaPost

Di seguito è riportato un esempio, a cui si fa riferimento da [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), che contiene una freccia e la lettera "A" appena sopra il centro del freccia.

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
## Riferimenti ##

* [MetaPost di Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Esempio di lattice Metapost di Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

