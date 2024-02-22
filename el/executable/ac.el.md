{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Μάθετε για τη μορφή αρχείου AC και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ACCDB.",
  "title" : "Μορφή αρχείου AC - Αρχείο Σεναρίου Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-el",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Τι είναι ένα αρχείο AC;

Το αρχείο AC είναι το αρχείο σεναρίου Autoconf. Το **Autoconf** είναι ένα επεκτάσιμο πακέτο μακροεντολών M4 που παράγουν σενάρια φλοιού για αυτόματη ρύθμιση παραμέτρων πακέτων πηγαίου κώδικα λογισμικού. Αυτά τα σενάρια μπορούν να προσαρμόσουν τα πακέτα σε πολλά είδη συστημάτων που μοιάζουν με UNIX χωρίς χειροκίνητη παρέμβαση του χρήστη. Το Autoconf δημιουργεί μια δέσμη ενεργειών διαμόρφωσης για ένα πακέτο από ένα αρχείο προτύπου που παραθέτει τις δυνατότητες του λειτουργικού συστήματος που μπορεί να χρησιμοποιήσει το πακέτο, με τη μορφή κλήσεων μακροεντολών M4.

Producing configuration scripts using Autoconf requires GNU M4. Θα πρέπει να εγκαταστήσετε το GNU M4 (τουλάχιστον την έκδοση 1.4.6, αν και συνιστάται η 1.4.13 ή μεταγενέστερη) πριν ρυθμίσετε τις παραμέτρους του Autoconf, έτσι ώστε το σενάριο ρύθμισης παραμέτρων του Autoconf να μπορεί να το βρει. Τα σενάρια διαμόρφωσης που παράγονται από το Autoconf είναι αυτόνομα, επομένως οι χρήστες τους δεν χρειάζεται να έχουν Autoconf (ή GNU M4).

## Πώς να ανοίξετε το αρχείο AC;

Το AC σημαίνει Automatic Configuration. Είναι ένα σενάριο που δημιουργήθηκε από το GNU Autoconf που επιτρέπει την προσαρμογή του πηγαίο κώδικα λογισμικού σε διάφορα συστήματα που μοιάζουν με Posix δοκιμάζοντας για τις απαραίτητες δυνατότητες στο πακέτο. Το σενάριο ονομάζεται αρχείο AC.

## Κύρια εξαρτήματα Autotools

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Το Autotools είναι μια συλλογή σχετικών πακέτων τα οποία, όταν χρησιμοποιούνται μαζί, αφαιρούν μεγάλο μέρος της δυσκολίας που συνεπάγεται η δημιουργία φορητού λογισμικού. Αυτά τα εργαλεία, μαζί με μερικά σχετικά απλά αρχεία εισόδου που παρέχονται από την αρχή, χρησιμοποιούνται για τη δημιουργία του συστήματος κατασκευής για ένα πακέτο.

**Μια βασική επισκόπηση του τρόπου με τον οποίο ταιριάζουν τα κύρια εξαρτήματα των αυτόματων εργαλείων.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

Σε μια απλή ρύθμιση:

- Το πρόγραμμα autoconf παράγει ένα σενάριο ρύθμισης παραμέτρων είτε από το configure.in είτε από το configure.ac.
- Το πρόγραμμα «automake» παράγει ένα Makefile.in από ένα Makefile.am.
- Το σενάριο «configure» εκτελείται για την παραγωγή ενός ή περισσότερων αρχείων Makefile από αρχεία Makefile.in.
- Το πρόγραμμα «make» χρησιμοποιεί το Makefile για τη μεταγλώττιση του προγράμματος.

## βιβλιογραφικές αναφορές
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [The Basics of Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



