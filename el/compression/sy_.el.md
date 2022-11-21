{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ Μορφή αρχείου - Συμπιεσμένο αρχείο SYS",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου SY_ και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Τι είναι ένα αρχείο SY_;

Ένα αρχείο SY_ είναι ένα συμπιεσμένο αρχείο .sys που χρησιμοποιείται από προγράμματα εγκατάστασης λογισμικού για τη μείωση του μεγέθους των αρχείων εγκατάστασης που είναι συσκευασμένα μέσα στο πρόγραμμα εγκατάστασης. Αυτό μειώνει το συνολικό μέγεθος του προγράμματος εγκατάστασης. Τα αρχεία SY_ μπορούν να επεκταθούν χρησιμοποιώντας το βοηθητικό πρόγραμμα γραμμής εντολών Microsoft Expand που επεκτείνει ένα ή περισσότερα συμπιεσμένα αρχεία.

## SY_ Μορφή αρχείου - Περισσότερες πληροφορίες

Τα αρχεία SY_ αποθηκεύονται στο δίσκο ως συμπιεσμένα δυαδικά αρχεία. Ωστόσο, η εσωτερική τους μορφή αρχείου δεν είναι διαθέσιμη δημόσια. Το βοηθητικό πρόγραμμα γραμμής εντολών Microsoft Expand μπορεί να επεκτείνει τα αρχεία SY_ χρησιμοποιώντας μία από τις ακόλουθες γραμμές εντολών.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Όταν αναπτυχθούν, τα αρχεία SY_ μετατρέπονται σε αρχείο [SYS](https://docs.fileformat.com/system/sys/).

Τα αρχεία SY_ είναι παρόμοια με τα αρχεία EX_ και DL_.

## βιβλιογραφικές αναφορές

* [StuffIt - By Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

