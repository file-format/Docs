{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο CRL - Λίστα ανάκλησης πιστοποιητικών",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CRL και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CRL.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Τι είναι ένα αρχείο CRL;

Ένα αρχείο CRL (Certificate Revocation List) είναι μια μαύρη λίστα ψηφιακών πιστοποιητικών X.509 που μια αρχή έκδοσης πιστοποιητικών (CA) ανακαλεί πριν από την ημερομηνία ανάκλησης που τους έχει ανατεθεί. Περιέχει πληροφορίες σχετικά με το ζήτημα και την ημερομηνία ανάκλησης που επιτρέπει στους διαχειριστές ασφαλείας να αποκλείουν τα επηρεαζόμενα ψηφιακά πιστοποιητικά. Το CRL δεν περιλαμβάνει πιστοποιητικά που έχουν λήξει, καθώς ο κύριος σκοπός του είναι να ειδοποιεί για τα μη αξιόπιστα και μη έγκυρα πιστοποιητικά.

Οι εφαρμογές που μπορούν **να ανοίξουν αρχεία CRL** περιλαμβάνουν το OpenSSL, το Microsoft IIS Server και το Citrix NetScaler.

## Μορφή αρχείου CRL - Περισσότερες πληροφορίες

Τα αρχεία CRL περιέχουν πληροφορίες στο πρότυπο X.509 το οποίο ορίζει επίσης τη σημασιολογία του για την κοινή χρήση πληροφοριών δημόσιου κλειδιού. Άλλες πληροφορίες που περιέχονται σε ένα αρχείο CRL μπορεί να περιλαμβάνουν το χρονικό όριο για το οποίο έχουν ανακληθεί τα πιστοποιητικά, ο λόγος της ανάκλησης, ο σειριακός αριθμός του ανακληθέντος πιστοποιητικού και η χρονική σήμανση.


### Κορυφαίοι λόγοι για την προσθήκη πιστοποιητικών στο CRL

Μπορεί να υπάρχουν διάφοροι λόγοι για την ανάκληση του πιστοποιητικού του ιστότοπού σας και την προσθήκη στο CRL. Μερικοί από αυτούς θα μπορούσαν να είναι?

1. Το ιδιωτικό κλειδί του πιστοποιητικού σας έχει παραβιαστεί
1. Το πιστοποιητικό σας δεν είναι έγκυρο ή δεν έχει εκδοθεί εσφαλμένα από την ΑΠ
1. Τα στοιχεία οργάνωσης που σχετίζονται με το πιστοποιητικό αλλάζουν και η ΑΠ εκδίδει νέο πιστοποιητικό
1. Κάθε άλλος αναπόφευκτος λόγος για τον οποίο έχει ανακληθεί το πιστοποιητικό

## βιβλιογραφικές αναφορές

* [Εθνικό Ινστιτούτο Προτύπων και Τεχνολογίας (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Λίστα ανάκλησης πιστοποίησης](https://en.wikipedia.org/wiki/Certificate_revocation_list)
