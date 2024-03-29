{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο vrml", "μορφή αρχείου vrml", "τι είναι αρχείο vrml", "αρχείο", "παράδειγμα vrml", "επέκταση αρχείου vrml", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου VRML",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου VRML και τα API που μπορούν να ανοίξουν και να δημιουργήσουν αρχεία VRML.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο VRML;
Η Virtual Reality Modeling Language (VRML) είναι μια μορφή αρχείου για την αναπαράσταση διαδραστικών [3D](/el/3d/) παγκόσμιων αντικειμένων στον Παγκόσμιο Ιστό (www). Βρίσκει τη χρήση του στη δημιουργία τρισδιάστατων αναπαραστάσεων περίπλοκων σκηνών όπως εικονογραφήσεις, ορισμός και παρουσιάσεις εικονικής πραγματικότητας. Η μορφή έχει αντικατασταθεί από [X3D](/el/3d/x3d/). Πολλές εφαρμογές τρισδιάστατης μοντελοποίησης μπορούν να αποθηκεύσουν αντικείμενα και σκηνές σε μορφή VRML.

## Μορφή αρχείου VRML

Το VRML είναι μια μορφή αρχείου κειμένου που καθορίζει πληροφορίες όπως κορυφές και άκρες ενός τρισδιάστατου πολυγώνου μαζί με πληροφορίες όπως το χρώμα της επιφάνειας, τις υφές με αντιστοίχιση UV, τη γυαλάδα, τη διαφάνεια και ούτω καθεξής. Έχει τη δυνατότητα αναπαράστασης στατικών και κινούμενων αντικειμένων εκτός από υπερσυνδέσμους με άλλα μέσα όπως ήχος, ταινίες και εικόνες. Αυτό επιτρέπει το άνοιγμα στοιχείων υπερσύνδεσης όταν ο χρήστης κάνει κλικ σε αυτά τα αντικείμενα.

Τα αρχεία TVRML στην κοινή ορολογία ονομάζονται "worlds" και έχουν την επέκταση .wrl. Η κειμενική φύση αυτών των αρχείων καθιστά δυνατή τη μείωση του μεγέθους του αρχείου χρησιμοποιώντας μορφές συμπίεσης όπως το gzip, καθιστώντας τα πιο ευνοϊκά για γρήγορη μεταφορά μέσω Διαδικτύου. Οι προδιαγραφές μορφής αρχείου για το [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) λειτουργούν ως αναφορά του προγραμματιστή για τη δημιουργία εφαρμογών συμβατών για την ανάγνωση/εγγραφή αυτών των αρχείων.

## Κριτήριο σχεδίασης ##

Ο στόχος και ο σχεδιασμός του VRML περιστρέφεται γύρω από τις ακόλουθες απαιτήσεις.

* **Δυνατότητα εξουσιοδότησης** - Καθιστά δυνατή την ανάπτυξη δημιουργών εφαρμογών και επεξεργαστών και εισαγωγή δεδομένων από άλλες βιομηχανικές μορφές
* **Πληρότητα** - Παρέχει όλες τις απαραίτητες πληροφορίες για την υλοποίηση και την αντιμετώπιση ενός πλήρους συνόλου χαρακτηριστικών για ευρεία αποδοχή από τον κλάδο
* **Συνθεσιμότητα** - Η δυνατότητα χρήσης στοιχείων του VRML σε συνδυασμό και, κατά συνέπεια, δυνατότητα επαναχρησιμοποίησης.
* **Επεκτασιμότητα** - Η δυνατότητα προσθήκης νέων στοιχείων.
* **Δυνατότητα υλοποίησης** -Δυνατότητα υλοποίησης σε ένα ευρύ φάσμα συστημάτων.
* **Δυνατότητα πολλών χρηστών** - Δεν πρέπει να αποκλείει την εφαρμογή περιβαλλόντων πολλών χρηστών.
* **Ορθογωνικότητα** - Τα στοιχεία του VRML θα πρέπει να είναι ανεξάρτητα μεταξύ τους ή οποιεσδήποτε εξαρτήσεις πρέπει να είναι δομημένες και καλά καθορισμένες.
* **Απόδοση** - Τα στοιχεία πρέπει να σχεδιάζονται με έμφαση στη διαδραστική απόδοση σε μια ποικιλία υπολογιστικών πλατφορμών.
* **Επεκτασιμότητα** - Τα στοιχεία του VRML πρέπει να σχεδιάζονται για απείρως μεγάλες συνθέσεις.
* **Τυπική πρακτική** - Μόνο εκείνα τα στοιχεία που αντικατοπτρίζουν την υπάρχουσα πρακτική, που είναι απαραίτητα για την υποστήριξη της υπάρχουσας πρακτικής ή που είναι απαραίτητα για την υποστήριξη προτεινόμενων προτύπων θα πρέπει να τυποποιούνται.
* **Καλά δομημένο** - Ένα στοιχείο πρέπει να έχει μια καλά καθορισμένη διεπαφή και έναν απλώς δηλωμένο σκοπό χωρίς όρους. Στοιχεία πολλαπλών χρήσεων και παρενέργειες θα πρέπει να αποφεύγονται.

## Βιβλιογραφικές αναφορές ##

* [VRML - Από τη Wikipedia](https://en.wikipedia.org/wiki/VRML)
* [Προδιαγραφές μορφής αρχείου VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html)

