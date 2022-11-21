
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο ADS - Μορφή αρχείου προδιαγραφών Ada",
  "description":"Μάθετε τι είναι η μορφή αρχείου ADS με παραδείγματα και API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Τι είναι ένα αρχείο ADS;

Ένα αρχείο ADS είναι ένα αρχείο προδιαγραφών για ένα έργο προγραμματισμού Ada. Είναι παρόμοιο με μια κλάση για Java ή το ζεύγος κεφαλίδας και υλοποίησης στην περίπτωση της C++. Οι δημόσιες και ιδιωτικές προδιαγραφές του πακέτου Ada αποθηκεύονται στο αρχείο .ads. Αντίθετα, το αρχείο .adb περιέχει την υλοποίηση ή σώματα Ada. Όπως το [C++](/el/programming/cpp/), το Ada προσφέρει διαχωρισμό μεταξύ προδιαγραφών και υλοποιήσεων ανεξάρτητα από το OOP.

Τα αρχεία ADS μπορούν να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου όπως το Microsoft Notepad, το Notepad++ και το Atom.

## Μορφή αρχείου ADS

Τα αρχεία ADS είναι σε απλή μορφή αρχείου απλού κειμένου και μπορούν να ανοίξουν/επεξεργαστούν με οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου. Τα πακέτα Ada μπορούν να οργανωθούν σε ιεραρχίες. Μια θυγατρική μονάδα μπορεί να δηλωθεί με τον ακόλουθο τρόπο:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## βιβλιογραφικές αναφορές

* [Πακέτα Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

