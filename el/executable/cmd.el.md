{
  "date" : "2021-07-12",
  "keywords" :[ "αρχείο cmd", "τι είναι ένα αρχείο cmd", "αρχείο", "παράδειγμα cmd", "επέκταση αρχείου cmd", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CMD και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CMD.",
  "title" :"CMD - Μορφή αρχείου εντολών των Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Τι είναι ένα αρχείο CMD;
Ένα αρχείο CMD αποτελείται από ένα σενάριο που περιέχει μία ή πολλές εντολές με τη μορφή απλού κειμένου που εκτελούνται για την εκτέλεση διαφόρων εργασιών. Είναι παρόμοιο με ένα αρχείο [BAT](/el/executable/bat/), το οποίο επίσης χρησιμοποιείται γενικά για την αποθήκευση μιας παρτίδας εκτελέσιμων εντολών. Τα αρχεία CMD χρησιμοποιούνται ευρέως στο λειτουργικό σύστημα Microsoft Windows. Αυτά τα αρχεία παρουσιάστηκαν σχεδόν στη δεκαετία του '90, αλλά εξακολουθούν να χρησιμοποιούνται στο πιο πρόσφατο λειτουργικό σύστημα Windows. Αυτά τα αρχεία είναι γενικά γραμμένα για να εκτελούν περισσότερες από μία εντολές σε μια ακολουθία.

## Μορφή αρχείου CMD
Το CMD είναι μια μορφή αρχείου που χρησιμοποιείται από εκτελέσιμα προγράμματα τύπου CP/M. Είναι γενικά συγκρίσιμο με το [COM](/el/executable/com/) στο CP/M-80 και το [EXE](/el/executable/exe/) στο DOS. Ένα αρχείο CMD περιέχει 1 έως 8 ομάδες κώδικα ή δεδομένων και μια κεφαλίδα 128 byte. Κάθε ομάδα μπορεί να έχει μέγεθος έως 1 mb. Τα αρχεία CMD μπορούν επίσης να περιέχουν πληροφορίες μετεγκατάστασης και Resident System Extensions (RSX) στις νεότερες εκδόσεις του. Το CMD είναι νέο σε σύγκριση με το αρχείο [BAT](/el/executable/bat/). χρησιμοποιείται για το MS-DOS πριν από την κυκλοφορία των Windows Στο MS-DOS. Παρόλο που μπορείτε ακόμα να αποθηκεύσετε αρχεία με επέκταση .bat σήμερα, πολλοί άνθρωποι χρησιμοποιούν την επέκταση .cmd για να αποθηκεύσουν τα εκτελέσιμα σενάρια τους.

### Προδιαγραφή μορφής CMD

Η αρχή της κεφαλίδας περιέχει τη λίστα των ομάδων που υπάρχουν στο αρχείο μαζί με τους τύπους τους. Κάθε τύπος μπορεί να χρησιμοποιηθεί το πολύ μία φορά. Αυτοί οι τύποι είναι:

- Κωδ
- Δεδομένα
- Έξτρα
- Στοίβα
- Χρήστης 1
- Χρήστης 2
- Χρήστης 3
- Χρήστης 4
- Κοινόχρηστος κώδικας

Ομοίως, Πρόθεμα τμήματος προγράμματος στο DOS, τα πρώτα 256 byte της ομάδας δεδομένων είναι μηδέν. Θα συμπληρωθούν με CP/M-86 με τη μηδενική σελίδα. Εάν δεν υπάρχει ομάδα δεδομένων, τότε θα χρησιμοποιηθούν τα πρώτα 256 byte της ομάδας κώδικα.
## Παράδειγμα αρχείου CMD
Ακολουθεί ένα παράδειγμα δέσμης ενεργειών CMD για την εμφάνιση πληροφοριών συστημάτων.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## βιβλιογραφικές αναφορές

* [Πώς να γράψετε ένα σενάριο CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [Αρχείο CMD (CP/M) - από τη Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))
