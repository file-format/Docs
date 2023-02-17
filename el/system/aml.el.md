{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο AML - Αρχείο γλώσσας μηχανής ACPI",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου ACPI AML και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Τι είναι ένα αρχείο AML;

Ένα αρχείο AML είναι ένα αρχείο συστήματος που δημιουργήθηκε με τη γλώσσα Advanced Configuration and Power Interface (ACPI) που χρησιμοποιείται για τη διαμόρφωση ιδιοτήτων υλικού. Περιέχει έναν ανεξάρτητο από μηχανή κώδικα byte που χρησιμοποιείται για τη διαμόρφωση του υλικού ακόμα και για απλές λειτουργίες, όπως ο τερματισμός λειτουργίας ενός υπολογιστή. Τα αρχεία AML ενδέχεται να περιέχουν οδηγίες ανάλογα με το σκοπό για τον οποίο πρόκειται να εγκατασταθούν στο μηχάνημα. Η εφαρμογή των προτύπων ACPI σάς επιτρέπει να βελτιώσετε τη λειτουργικότητα διαχείρισης ενέργειας και μια ισχυρή διεπαφή για τη διαμόρφωση συσκευών μητρικής πλακέτας όπως οι μητρικές πλακέτες P55.

## Μορφή αρχείου ACPI AML

Τα αρχεία AML αποθηκεύονται ως δυαδικά αρχεία σε δίσκο με περιεχόμενα γραμμένα σε κώδικα byte. Οι προδιαγραφές μορφής αρχείου του προτύπου ACPI είναι διαθέσιμες στο [uefi](https://uefi.org/node/735). Η γλώσσα έχει σχεδιαστεί για να προσφέρει σταθερότητα και συμβατότητα προς τα πίσω, απαιτώντας λιγότερες επανεγγραφές ή ανακατασκευές της στοίβας εφαρμογών.

## Προδιαγραφές μορφής αρχείου AML

Ένα αρχείο AML αποτελείται από πίνακες DSDT και SSDT. Ο κώδικας byte AML διαβάζεται και αναλύεται από την αρχή καθενός από αυτούς τους πίνακες. Αυτό παρέχει πληροφορίες σχετικά με τους ορισμούς των συσκευών και των αντικειμένων στον χώρο ονομάτων ACPI. Χρησιμοποιώντας αυτές τις πληροφορίες, ο διερμηνέας AML μπορεί να δημιουργήσει μια λίστα με όλες τις συσκευές που είναι διαθέσιμες στο σύστημα και τις υποστηριζόμενες ιδιότητες και λειτουργίες τους.

### Παράδειγμα κώδικα ASL για ένα DSDT

Ένα παράδειγμα κώδικα ASL για ένα DSDT είναι το ακόλουθο.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## βιβλιογραφικές αναφορές

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)
