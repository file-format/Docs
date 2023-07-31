{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Αρχείο αναφοράς Macro Microsoft Office",
  "description":"Μάθετε για το αρχείο MSO και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Τι είναι ένα αρχείο MSO;

Ένα αρχείο MSO είναι μια μορφή αρχείου κοντέινερ δεδομένων που δημιουργείται όταν αποστέλλεται ένα μήνυμα HTML χρησιμοποιώντας το Microsoft Outlook. Αυτό συμβαίνει κυρίως με τις εφαρμογές του Microsoft Office 2000. Στις περισσότερες περιπτώσεις, το μήνυμα email επισυνάπτεται με το όνομα **Oledata.mso** αρχείο. Ο παραλήπτης email, όταν ανοίγει ένα τέτοιο email, μπορεί να δει το αρχείο σωστά ακόμα κι αν δεν έχει εγκατεστημένο το ίδιο λογισμικό. Τα αρχεία MSO αναφέρονται στο [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Μορφή αρχείου Microsoft MSO

Τα αρχεία MSO αποθηκεύονται σε Μορφή αρχείου σύνθετου εγγράφου της Microsoft (MCDF), η οποία είναι επίσης γνωστή ως Σύνδεση και Ενσωμάτωση Αντικειμένου (OLE) ή Μοντέλο Αντικειμένου Στοιχείου (COM) δομημένη μορφή δυαδικού αρχείου υλοποίησης σύνθετων αρχείων αποθήκευσης.

### Δομή μορφής αρχείου MSO

Η εσωτερική δομή μορφής αρχείου της μορφής αρχείου MSO είναι καλά καθορισμένη στο [Structures](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd) ενότητα της τεκμηρίωσης του MCDF. Ο πίνακας κατανομής αρχείων (FAT) διαχειρίζεται την κατανομή τομέα και τις αλυσίδες τομέα. Περιέχει μια σειρά από αριθμούς τομέων 32 bit. Κάθε δείκτης στον πίνακα αντιπροσωπεύει έναν αριθμό τομέα, ενώ η τιμή του αντιπροσωπεύει τον επόμενο τομέα στην αλυσίδα ή μια ειδική τιμή.

## βιβλιογραφικές αναφορές

* [COM Structured Storage](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

