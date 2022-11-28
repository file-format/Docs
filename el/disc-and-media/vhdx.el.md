{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου VHDX και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία VHDX.",
  "title" :"Μορφή αρχείου VHDX - Τι είναι ένα αρχείο VHDX;",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Τι είναι ένα αρχείο VHDX;

Ένα αρχείο VHDX είναι ένα αρχείο εικόνας δίσκου σε μορφή αρχείου Virtual Hard Disk v2. Περιέχει ένα ολόκληρο λειτουργικό σύστημα που μπορεί να φορτωθεί και να χρησιμοποιηθεί ως οποιοδήποτε κανονικό μηχάνημα για τη δοκιμή λογισμικού ή την εκτέλεση λογισμικού που απαιτεί συγκεκριμένο λειτουργικό σύστημα. Ένα VHDX, παρόλο που είναι εικόνα πλήρους δίσκου, αποθηκεύεται σε ένα μόνο αρχείο. Το λογισμικό εικονικής μηχανής όπως το Parallels Desktop, το Windows Virtual Machine και το Virtual Box μπορεί να φορτώσει και να ανοίξει την εικόνα του δίσκου.

Το αρχείο VHDX μπορεί να μετατραπεί σε [VHD](/el/disc-and-media/vhd/) με το Hyper-V Manager ή σε [VDI](/el/disc-and-media/vdi/) με το VirtualBox.

## Μορφή αρχείου VHDX - Περισσότερες πληροφορίες

Οι λεπτομέρειες της μορφής αρχείου VHDX είναι πλήρως τεκμηριωμένες και διαθέσιμες στο διαδίκτυο ως [Προδιαγραφές μορφής αρχείου VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d54774 ) στην Τεκμηρίωση της Microsoft. Είναι μια επέκταση στη μορφή VHD και περιλαμβάνει βελτιωμένες δυνατότητες. Η μορφή αρχείου VHDX παρέχει πρόσθετες λειτουργίες που είναι διαθέσιμες στον εικονικό σκληρό δίσκο και στα επίπεδα αρχείου εικονικού σκληρού δίσκου. Είναι πιο βελτιστοποιημένο και δίνει καλύτερα αποτελέσματα για τη διαμόρφωση και τις δυνατότητες του υλικού αποθήκευσης. Τα αρχεία VHDX μπορούν να ανοίξουν

### Υποστήριξη για εικονικούς σκληρούς δίσκους σε VHDX

Υποστηρίζει τρεις τύπους εικονικών σκληρών δίσκων.

1. **Σταθερός εικονικός σκληρός δίσκος** - Εικονικός σκληρός δίσκος με εκχωρημένο σταθερό μέγεθος δεδομένων. Το μέγεθος του εικονικού σκληρού δίσκου δεν αλλάζει με την προσθήκη ή την αφαίρεση δεδομένων.

1. **Dynamic Virtual Hard Disk** - Εικονικός σκληρός δίσκος με δυναμικό μέγεθος δίσκου. Το μέγεθός του ανά πάσα στιγμή είναι τόσο μεγάλο όσο τα πραγματικά δεδομένα που γράφονται σε αυτό και τα μεταδεδομένα. Το μέγεθος του αρχείου του αυξάνεται δυναμικά καθώς προστίθενται ή αφαιρούνται δεδομένα από αυτό.

1. **Διαφορά εικονικού σκληρού δίσκου** - Αντιπροσωπεύει το ρεύμα του εικονικού σκληρού δίσκου ως ένα σύνολο τροποποιημένων μπλοκ σε σύγκριση με ένα γονικό αρχείο εικονικού σκληρού δίσκου.

## βιβλιογραφικές αναφορές

* [Προδιαγραφές μορφής αρχείου VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - από τη Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))
