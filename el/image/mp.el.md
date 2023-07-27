{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο MP - Αρχείο LaTeX MetaPost",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου MP και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Τι είναι ένα αρχείο MP;

Ένα αρχείο MP είναι ένα διανυσματικό αρχείο εικόνας που δημιουργείται από τη γλώσσα προγραμματισμού MetaPost για τη δημιουργία εικόνων. Οι διανυσματικές εικόνες που δημιουργούνται με τη μορφή αρχείου MP αποθηκεύονται ως αρχεία [EPS](/el/page-description-language/eps/) (Encapsulated PostScript). Επιπλέον, το MetaPost διανέμεται με πλαίσια TeX και Metafont και μπορούν να δημιουργηθούν αρχεία MP μέσα από τα αρχεία TEX και LTX που χρησιμοποιούνται από αυτές τις εφαρμογές. Τα αρχεία MP περιέχουν δηλώσεις σχεδίασης και μαθηματικά αλγοριθμικά σχέδια για την απόδοση του αρχείου EPS εξόδου. Η μηχανή PDFTex μπορεί να χρησιμοποιήσει το EPS που δημιουργήθηκε για να δημιουργήσει απευθείας αρχεία [PDF](/el/pdf/).

## Μορφή αρχείου MP

Τα αρχεία MP αποθηκεύονται στο δίσκο ως δυαδικά αρχεία και δημιουργούν έξοδο EPS όταν εξάγονται σε μορφή αρχείου διανυσματικής εικόνας εξόδου. Τα σχέδια που δημιουργούνται με τη χρήση MetaPost περιλαμβάνονται σε μορφοποιημένη μορφή στα τεχνικά έγγραφα και τις δημοσιεύσεις περιοδικών που έχουν δημιουργηθεί με LaTex.

### Παράδειγμα αρχείου MetaPost MP

Ακολουθεί ένα παράδειγμα, που αναφέρεται από το [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), που περιέχει ένα βέλος και το γράμμα "A" ακριβώς πάνω από τη μέση του βέλος.

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
## Βιβλιογραφικές αναφορές ##

* [MetaPost από τη Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Δείγμα Latex Metapost by Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

