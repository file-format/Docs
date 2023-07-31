{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Τι είναι ένα αρχείο APPX;",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου APPX και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Τι είναι ένα αρχείο APPX;

Ένα αρχείο APPX είναι μια μορφή αρχείου πακέτου με δυνατότητα διανομής που χρησιμοποιείται για τη διανομή και την εγκατάσταση μιας εφαρμογής. Εισήχθη με τα Windows 8 για να δημοσιευτεί στο Microsoft Windows Store. Περιέχει όλα τα αρχεία που απαιτούνται για την εγκατάσταση μιας εφαρμογής Windows. Αυτά περιλαμβάνουν μεταδεδομένα, αρχεία και πληροφορίες διαπιστευτηρίων. Μια πιο σύγχρονη μορφή αρχείου συσκευασίας είναι το MSIX που σήμερα χρησιμοποιείται πιο συχνά σε σύγκριση με το APPX.

## Μορφή αρχείου APPX - Περισσότερες πληροφορίες

Τα αρχεία APPX αποθηκεύονται ως συμπιεσμένα αρχεία σε μορφή αρχείου [ZIP](/el/compression/zip/). Αυτό καθιστά ολόκληρο το πακέτο ως αρχείο αρχειοθέτησης με μειωμένο μέγεθος αρχείου που είναι εύκολο να μεταφορτωθεί στο Microsoft Store.

## Πώς να προβάλετε αρχεία σε ένα αρχείο APPX;

Για να δείτε τα περιεχόμενα ή τα αρχεία μέσα σε ένα αρχείο APPX, θα πρέπει να ακολουθήσετε τα παρακάτω βήματα.

1. Επειδή τα αρχεία APPX αποθηκεύονται ως συμπιεσμένα αρχεία ZIP, μετονομάστε το αρχείο σε επέκταση .zip
1. Χρησιμοποιήστε οποιοδήποτε εργαλείο αποσυμπίεσης, όπως 7-Zip, WinZip ή WinRAR για να εξαγάγετε τα αρχεία που περιέχονται στο αρχείο APPX

## Πώς να δημιουργήσετε ένα αρχείο APPX;

Υπάρχουν δύο μέθοδοι που μπορούν να χρησιμοποιηθούν για τη δημιουργία αρχείων APPX.

1. Χρήση του MakeApp.exe - Το [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) χρησιμοποιείται για τη δημιουργία και των δύο πακέτα εφαρμογών (.msix ή .appx) και αρχεία πακέτου εφαρμογών .msixbundle ή .appxbundle). Επιπλέον, μπορεί να εξαγάγει αρχεία από ένα πακέτο εφαρμογών. Το MakeApp.exe είναι διαθέσιμο με το Windows 10 SDK και μπορεί να χρησιμοποιηθεί από τη γραμμή εντολών.
1. Χρήση του Microsoft Visual Studio - Οι προγραμματιστές συνήθως [δημιουργούν αρχεία APPX](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) χρησιμοποιώντας το Microsoft Visual Studio. Μόλις ολοκληρωθεί η ανάπτυξη της εφαρμογής και η εφαρμογή είναι έτοιμη για δημοσίευση, το αρχείο πακέτου APPX μπορεί να δημιουργηθεί δημοσιεύοντας το μέσα από το Visual Studio.

## βιβλιογραφικές αναφορές

* [Δημιουργήστε ένα πακέτο ή πακέτο MSIX με το MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Δημιουργία αρχείων APPX χρησιμοποιώντας το Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

