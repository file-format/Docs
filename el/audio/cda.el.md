{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "αρχείο", "επέκταση", "μορφή", "τι είναι ένα αρχείο cda", "μουσική", "μορφή αρχείου cda", "προδιαγραφή μορφής αρχείου cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου CDA και τα API που μπορούν να δημιουργήσουν, να μετατρέψουν και να ανοίξουν αρχεία CDA.",
  "title" :"CDA - Αρχείο συντόμευσης κομματιού ήχου CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Τι είναι ένα αρχείο CDA;

Ένα αρχείο με επέκταση .cda είναι ένα μικρό αρχείο στέλεχος που δημιουργείται από τα Microsoft Windows για κάθε κομμάτι ήχου σε ένα CD ήχου. Αυτά τα αρχεία περιέχουν τυπικές πληροφορίες, όπως χρόνους κομματιού και μια συντόμευση των Windows που επιτρέπει στους χρήστες να έχουν πρόσβαση στα συγκεκριμένα κομμάτια ήχου. Τα αρχεία CDA δεν είναι μουσική, αλλά δείχνουν ένα αρχείο μουσικής που υπάρχει κάπου στο χώρο αποθήκευσης. Μπορούμε να το πούμε ως συντόμευση ενός αρχείου ήχου που βρίσκεται σε ένα CD.

## Μορφή αρχείου CDA

Η μορφή αρχείου CDA χρησιμοποιείται για να πει σε έναν υπολογιστή ποιο αρχείο ήχου να παίξει σε ένα CD. Έτσι, τα αρχεία CDA γίνονται άχρηστα χωριστά από ένα CD που αντιπροσωπεύουν. Τα αρχεία CDA θεωρούνται συνήθως ως πόροι RIFF. Υπάρχει μόνο ένα κομμάτι που ονομάζεται "CDDA" και περιέχει μόνο ένα μπλοκ δεδομένων που ονομάζεται "FMT" στην τρέχουσα έκδοση του αρχείου .cda. Αυτό το μπλοκ έχει μήκος 24 byte. Το αναγνωριστικό που δημιουργήθηκε από τα Windows χρησιμοποιείται από τη μονάδα CD που σχετίζεται με τα Windows 95 και Windows 98 και η συσκευή αναπαραγωγής του δεν μπορεί να συνδεθεί στο FreeDB ή στο CDDB. Για να μπορεί να εμφανίζει τον τίτλο του τραγουδιού και το όνομα του καλλιτέχνη, τα οποία πρέπει να εισάγετε χειροκίνητα αυτές τις πληροφορίες στο αρχείο cdplayer.ini.

### Οργάνωση ενός αρχείου CDA

Ο παρακάτω πίνακας δείχνει τις πληροφορίες σχετικά με τις τυπικές μετατοπίσεις:
| αντιστάθμιση | μήκος | περιεχόμενο |
---|---|---|
| 0x00 | 4 | οι 4 χαρακτήρες ASCII "RIFF" |
| 0x04 | 4 | το μέγεθος του παρακάτω κομματιού: πάντα 36 (44 - 8), σε 4 byte (παραγγελία Intel) |
| 0x08 | 4 | Αναγνωριστικό κομματιού: οι 4 χαρακτήρες ASCII "CDDA" |
| 0x0C | 4 | οι 3 χαρακτήρες ASCII "fmt" ακολουθούμενοι από ένα κενό |
| 0x10 | 4 | μήκος του κομματιού: πάντα 24, σε 4 byte (παραγγελία Intel) |
| 0x14 | 2 | έκδοση της μορφής CD, σε 2 byte (παραγγελία Intel). Τον Μάιο του 2006, πάντα ίσο με 1. |
| 0x016 | 2 | αριθμός της περιοχής, σε 2 byte (παραγγελία Intel). Το πρώτο κομμάτι έχει τον αριθμό 1. |
| 0x18 | 4 | αναγνωριστικό που υπολογίζεται από τα Windows για το cdplayer.exe. |
| 0x1c | 4 | μετατόπιση εύρους, σε αριθμό καρέ (παραγγελία Intel) |
| 0x20 | 4 | διάρκεια του κομματιού, συνολικός αριθμός καρέ (παραγγελία Intel) |
| 0x24 | 1 | θέση εμβέλειας: πλαίσια |
| 0x25 | 1 | θέση εμβέλειας: δευτερόλεπτα |
| 0x26 | 1 | θέση εμβέλειας: λεπτά |
| 0x27 | 1 | ένα μηδενικό byte (δυαδική τιμή 0) |
| 0x28 | 1 | διάρκεια του κομματιού: καρέ |
| 0x29 | 1 | διάρκεια του κομματιού: δευτερόλεπτα |
| 0x2a | 1 | διάρκεια του κομματιού: λεπτά |
| 0x2b | 1 | ένα μηδενικό byte (δυαδική τιμή 0) |

## βιβλιογραφικές αναφορές

* [αρχείο .cda - Από τη Wikipedia](https://en.wikipedia.org/wiki/.cda_file)
