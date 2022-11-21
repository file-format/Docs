{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "επέκταση", "αρχείο", "μορφή αρχείου", "Τύπος αρχείου βάσης δεδομένων", "μορφή αρχείου βάσης δεδομένων", "βάση δεδομένων Btrieve" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου BTR και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία BTR.",
  "title" :"BTR - Αρχείο βάσης δεδομένων Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Τι είναι ένα αρχείο BTR;

Ένα αρχείο με επέκταση .btr είναι ένα αρχείο βάσης δεδομένων που δημιουργήθηκε από την εφαρμογή βάσης δεδομένων συναλλαγών [Btrieve](https://www.actian.com/). Σε αντίθεση με τα συστήματα διαχείρισης σχεσιακών βάσεων δεδομένων (RBMS), το Btrieve βασίζεται στη μέθοδο Indexed Sequential Access Method (ISAM), η οποία είναι ένας τρόπος αποθήκευσης δεδομένων για γρήγορη ανάκτηση. Το αρχείο BTR αποθηκεύει μια συλλογή εγγραφών και χρησιμοποιείται για τη δημιουργία αναφορών σύμφωνα με τις απαιτήσεις. Τα αρχεία BTR μπορούν να ανοίξουν χρησιμοποιώντας το Pervasive Btrieve Database Manager, το Pervasive PSQL Maintenance Utility και το Legend Software BTRIEVE Viewer.

## Δομή αρχείου BTR - Περισσότερες πληροφορίες

Η εσωτερική δομή δεδομένων και η στοίχιση κάθε byte στη δομή ενός αρχείου BTR δεν είναι δημόσια διαθέσιμα. Ωστόσο, Btrieve
παρέχει το [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) που μπορεί να χρησιμοποιηθεί για την ανάγνωση των πληροφοριών από αρχεία BTR. Είναι συμβατό με τις ακόλουθες γλώσσες προγραμματισμού και περιβάλλοντα ανάπτυξης.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Η ανάκτηση δεδομένων από ένα αρχείο BTR εξαρτάται από το σχετικό αρχείο DDF με αυτό. Χωρίς το DDF, δεν θα είναι εύκολο να ανακτήσετε τις πληροφορίες από ένα τέτοιο αρχείο.

## βιβλιογραφικές αναφορές

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Εισαγωγή στα Btreive API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

