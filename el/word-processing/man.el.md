{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Εγχειρίδιο Unix",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου FODT και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Τι είναι ένα αρχείο MAN;

Ένα αρχείο με επέκταση .man σημαίνει man page που είναι ένα εγχειρίδιο χρήστη προγραμματισμού Unix σε μορφή τεκμηρίωσης λογισμικού. Χρησιμοποιείται από το βοηθητικό πρόγραμμα «Man», που περιλαμβάνεται στο Unix, το οποίο χρησιμοποιείται για την προβολή της τεκμηρίωσης. Η τεκμηρίωση λογισμικού περιέχει πληροφορίες σε ενότητες και σελίδες που μπορούν να ανακτηθούν χρησιμοποιώντας το βοηθητικό πρόγραμμα Man από το τερματικό εντολών με την έκδοση εντολών. Όντας διαθέσιμο στον υπολογιστή ως μαλακό αντίγραφο τεκμηρίωσης, δεν απαιτεί κανένα έντυπο αντίγραφο ή σύνδεση στο Διαδίκτυο για πρόσβαση σε αυτό.

## Unix Manual Man File Format - Περισσότερες πληροφορίες

Οι σελίδες Man αποθηκεύονται σε μορφή απλού κειμένου και μπορούν να δημιουργηθούν και να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου για προβολή ή επεξεργασία. Στο UNIX, οι πληροφορίες από τις σελίδες Man ανακτώνται με την έκδοση εντολών από το τερματικό που περιλαμβάνουν αναφορά σε αριθμούς ενότητας και σελίδων από το εγχειρίδιο.

### Ενότητες και σελίδες

Το Unix man είναι το εγχειρίδιο του συστήματος όπου κάθε όρισμα σελίδας στην εντολή αναφέρεται στο όνομα ενός προγράμματος, ενός βοηθητικού προγράμματος ή μιας συνάρτησης. η εντολή, εάν παρέχεται με πληροφορίες ενότητας, θα αναζητήσει τη σελίδα στη συγκεκριμένη ενότητα. Ωστόσο, η προεπιλεγμένη συμπεριφορά είναι η αναζήτηση της σελίδας σε όλες τις ενότητες και η εμφάνιση της πρώτης σελίδας ανεξάρτητα από το αν υπάρχει σε πολλές ενότητες.

### Αριθμοί Ενοτήτων

Ακολουθούν οι πληροφορίες σχετικά με τους αριθμούς ενοτήτων του εγχειριδίου, ακολουθούμενες από τους τύπους σελίδων που περιέχουν.

|Αριθμός Ενότητας|Είδος σελίδων|
---|---|
|1|Εκτέλεσιμα προγράμματα ή εντολές φλοιού|
|2|Κλήσεις συστήματος (συναρτήσεις παρέχονται από τον πυρήνα)|
|3|Κλήσεις βιβλιοθήκης (λειτουργίες εντός βιβλιοθηκών προγραμμάτων)|
|4|Ειδικά αρχεία (συνήθως βρίσκονται στο /dev)|
|5|Μορφές και συμβάσεις αρχείων, π.χ. /etc/passwd|
|6|Παιχνίδια|
|7|Διάφορα (συμπεριλαμβανομένων πακέτων μακροεντολών και συμβάσεων), π.χ. man(7), groff(7)|
|8|Εντολές διαχείρισης συστήματος (συνήθως μόνο για root)|
|9|Ρουτίνες πυρήνα [Μη τυπική]|

## Παράδειγμα - Πώς να διαβάσετε τις σελίδες MAN;

Ακολουθεί ένα παράδειγμα πώς να ανακτήσετε πληροφορίες σχετικά με την εντολή MkDir χρησιμοποιώντας την εντολή Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## βιβλιογραφικές αναφορές

* [OpenDocument Technical Specifications - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — σελίδα εγχειριδίου Linux](https://man7.org/linux/man-pages/man1/man.1.html)
