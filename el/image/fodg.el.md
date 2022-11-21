{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο fodg", "μορφή αρχείου fodg", "τι είναι ένα αρχείο fodg", "αρχείο", "παράδειγμα fodg", "επέκταση αρχείου fodg", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - Μορφή αρχείου σχεδίασης OpenDocument",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου FODG και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία FODG.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο FODG;

Ένα αρχείο με επέκταση .fodg είναι μια μορφή αρχείου Apache OpenOffice Drawing για την αποθήκευση στοιχείων σχεδίασης. Βασίζεται στις προδιαγραφές μορφής αρχείου που περιγράφονται από το Advancement of Structural Information Standards (OASIS). Μια άλλη παρόμοια μορφή αρχείου για γραφικά OpenOffice είναι το [ODG](/el/image/odg/) που αποθηκεύει στοιχεία σχεδίασης ως διανυσματική εικόνα. Τα αρχεία FODG μπορούν να ανοίξουν με το OpenOffice καθώς και με το LibreOffice. Άλλες μορφές αρχείων που υποστηρίζονται από το OpenOffice, για παράδειγμα, περιλαμβάνουν τα [ODT](/el/word-processing/odt/), ODF, [ODP](/el/presentation/odp/) και [ODS](/el/spreadsheet/ods/).

## Μορφή αρχείου FODG

Το FODG βασίζεται στη μορφή αρχείου XML του OpenDocument που συμμορφώνεται με το πρότυπο OASIS OpenDocument Format ISO/IEC 26300. Έχει εφαρμογή Internet Media Type/vnd.oasis.opendocument.graphics και συμμορφώνεται επίσης με το org.oasis-open.opedocument public.composite-content . Η δομή XML είναι κοινή για όλους τους τύπους εγγράφων, όπως υπολογιστικά φύλλα, αρχεία σχεδίων και έγγραφα κειμένου. Τα έγγραφα του OpenOffice εκμεταλλεύονται τον διαχωρισμό των ανησυχιών διαχωρίζοντας το περιεχόμενο, τα στυλ, τα μεταδεδομένα και τις ρυθμίσεις της εφαρμογής σε τέσσερα ξεχωριστά αρχεία XML.

`<office:document-content> ` - Περιεχόμενο εγγράφου και αυτόματα στυλ που χρησιμοποιούνται στο περιεχόμενο.
`<office:document-styles> ` - Στυλ που χρησιμοποιούνται στο περιεχόμενο του εγγράφου και αυτόματα στυλ που χρησιμοποιούνται στα ίδια τα στυλ.
`<office:document-meta> ` - Έγγραφο μεταδεδομένων, όπως ο συγγραφέας ή η ώρα της τελευταίας ενέργειας αποθήκευσης.
`<office:document-settings> ` - Ρυθμίσεις για συγκεκριμένες εφαρμογές, όπως το μέγεθος του παραθύρου ή οι πληροφορίες του εκτυπωτή.

## Βιβλιογραφικές αναφορές ##
* [Μελλοντικές προδιαγραφές για την τυποποίηση έκδοσης 1.3 ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Μορφή OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

