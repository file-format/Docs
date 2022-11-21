{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST File Format- ReStructuredText File",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου RST και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Τι είναι ένα αρχείο RST;

Ένα αρχείο RST είναι μια μορφή αρχείου τεχνικής τεκμηρίωσης, που χρησιμοποιείται κυρίως στην κοινότητα προγραμματισμού Python. Είναι ένα αρχείο κειμένου γραμμένο στη γλώσσα σήμανσης reStructuredText που εφαρμόζει στυλ και μορφοποίηση σε έγγραφα απλού κειμένου για τη δημιουργία τεκμηρίωσης. Τα αρχεία RST χρησιμοποιούν τα σχόλια και άλλες πληροφορίες στον κώδικα προγραμμάτων Python για τη δημιουργία τεχνικής τεκμηρίωσης της εφαρμογής. Ωστόσο, αυτά μπορούν επίσης να περιέχουν κείμενο που μπορεί να μετατραπεί σε απλές ιστοσελίδες και [eBooks](/el/ebook/). Επεξεργαστές κειμένου όπως Github Atom, GNU Emacs (cross-platform), Microsoft Notepad (Windows), Apple TextEdit (Mac) και Vim (Linux) μπορούν να χρησιμοποιηθούν για το άνοιγμα αρχείων RST.

## Μορφή αρχείου RST

Τα αρχεία RST περιέχουν κώδικα που είναι γραμμένος σε γλώσσα σήμανσης reStructuredText. Αποτελεί μέρος του έργου Docutils της Python Doc-SIG (Ομάδα Ειδικού Ενδιαφέροντος Τεκμηρίωσης) που παρέχει ένα σύνολο εργαλείων για την Python παρόμοια με το Javadoc για Java. Ο αναλυτής για τη μορφή αρχείου RST είναι ενσωματωμένος στα Docutils και μπορεί να εξάγει πληροφορίες από προγράμματα Python για τη μορφοποίησή τους σε τεκμηρίωση προγράμματος.

### Παράδειγμα ReStructuredText RST

Ας πάρουμε ένα παράδειγμα κειμένου γραμμένο σε μορφή αρχείου RST ως εξής.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Όταν αυτό το κείμενο εισάγεται σε έναν επεξεργαστή rST όπως το Docutils, η έξοδος είναι η εξής.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Αναφορά ##

* [reStructuredText - by Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

