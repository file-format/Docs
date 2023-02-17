{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο wmz", "μορφή αρχείου wmz", "τι είναι ένα αρχείο wmz", "αρχείο", "παράδειγμα wmz", "επέκταση αρχείου wmz", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου WMZ - Συμπιεσμένο μετααρχείο των Windows",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου WMZ και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία WMZ.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Τι είναι ένα αρχείο WMZ;

Ένα αρχείο με επέκταση .wmz είναι μια συμπιεσμένη έκδοση του [WMF](/el/image/wmf/) και χρησιμοποιείται για την αποθήκευση μετα-αρχείων. Είναι ένα αρχείο μεσαίου επιπέδου που δημιουργείται από παλαιότερες εκδόσεις εφαρμογών του Microsoft Office και δεν χρησιμοποιείται πολύ ευρέως. Τα αρχεία WMZ δημιουργούνται κατά την αποθήκευση εγγράφων σε μορφή [HTML](/el/web/html/). Αυτά μπορεί επίσης να δημιουργηθούν κατά την αποστολή εγγράφων μέσω email που περιέχουν ενσωματωμένα clip art, εξισώσεις κ.λπ. Οι εφαρμογές που μπορούν να ανοίξουν αρχεία WMZ περιλαμβάνουν (αλλά δεν περιορίζονται σε) το Corel Winzip και το Apple Archive Utility.

## Μορφή αρχείου WMZ

Τα αρχεία WMZ είναι [Gzip](/el/compression/gz/) συμπιεσμένα και περιέχουν [WMF](/el/image/WMF/) μέσα. Το Gzip χρησιμοποιεί τον αλγόριθμο DEFLATE για τη συμπίεση του αρχείου. Το GZIP είναι διαφορετικό από τη μορφή αρχείου [ZIP](/el/compression/zip/), καθώς εφαρμόζει τον αλγόριθμο συμπίεσης για την ολοκλήρωση της αρχειοθέτησης και όχι για τα μεμονωμένα αρχεία. Η μορφή αρχείου αποτελείται από:

* Κεφαλίδα αρχείου
* Προαιρετικές κεφαλίδες
* Συμπιεσμένα δεδομένα
* Υποσέλιδο αρχείου

Η μορφή αρχείου GZIP [προδιαγραφές έκδοση 4.3](http://tools.ietf.org/html/rfc1952) που δημοσιεύτηκε από το Internet Engineering Task Force (IETF) περιέχει λεπτομερείς πληροφορίες σχετικά με τη μορφή αρχείου.

## βιβλιογραφικές αναφορές

* [RFC1952: Προδιαγραφή μορφής αρχείου GZIP](http://tools.ietf.org/html/rfc1952), από [IETF](https://ietf.org)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)
