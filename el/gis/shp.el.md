{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο shp", "μορφή αρχείου shp", "τι είναι αρχείο shp", "αρχείο", "παράδειγμα shp", "επέκταση αρχείου shp", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI Shapefile",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου SHP και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία SHP.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο SHP;

Το SHP είναι η επέκταση αρχείου για έναν από τους κύριους τύπους αρχείων που χρησιμοποιούνται για την αναπαράσταση του ESRI Shapefile. Αντιπροσωπεύει γεωχωρικές πληροφορίες με τη μορφή διανυσματικών δεδομένων που θα χρησιμοποιηθούν από εφαρμογές Γεωγραφικών Συστημάτων Πληροφοριών (GIS). Η μορφή έχει αναπτυχθεί ως ανοιχτές προδιαγραφές προκειμένου να διευκολυνθεί η διαλειτουργικότητα μεταξύ της ESRI και άλλων προϊόντων λογισμικού.

## Αναπαράσταση δεδομένων

Όπως αναφέρθηκε, μια μορφή αρχείου σχήματος περιγράφει τις γεωχωρικές πληροφορίες ενός συνόλου δεδομένων ως διανυσματικά χαρακτηριστικά. Αυτά τα διανυσματικά χαρακτηριστικά περιλαμβάνουν:

* πόντους
* γραμμές
* πολύγωνα

Αυτά τα χαρακτηριστικά σε συνδυασμό μπορούν να αντιπροσωπεύουν σχεδόν κάθε τύπο σχημάτων όπως πηγάδια νερού, όρια χωρών, χωρικά σημεία, ροή ποταμών, λίμνες κ.λπ. Κάθε διανυσματικό χαρακτηριστικό μπορεί να έχει χαρακτηριστικά που καθορίζουν πραγματικά τον σκοπό αυτού του χαρακτηριστικού. Για παράδειγμα, ένα shapefile που περιέχει πόλεις του Λος Άντζελες μπορεί να έχει το όνομα της πόλης και τη θερμοκρασία ως χαρακτηριστικά που δίνουν ουσιαστική αναπαράσταση στα χωρικά δεδομένα.

## Συσχετισμένα αρχεία

Ένα αυτόνομο αρχείο shp δεν μπορεί να χρησιμοποιηθεί από εφαρμογές λογισμικού για να δώσει νόημα στα δεδομένα που περιέχει. Για να κατανοήσει κανείς τις πληροφορίες που περιέχονται σε ένα τέτοιο αρχείο, ένα shapefile χρησιμοποιεί τα ακόλουθα πρόσθετα υποχρεωτικά αρχεία.

* αρχείο shx - αρχείο ευρετηρίου
* Αρχείο dbf - ένα αρχείο dBASE που αποθηκεύει όλα τα χαρακτηριστικά των σχημάτων στο κύριο αρχείο
* αρχείο prj - αποθηκεύει τις πληροφορίες έργου του αρχείου

Μπορεί να υπάρχουν και άλλα προαιρετικά αρχεία που μοιράζονται το ίδιο όνομα με το κύριο αρχείο.

## Προδιαγραφές μορφής αρχείου SHP

Οι ανοιχτές προδιαγραφές του shapefile είναι διαθέσιμες στο διαδίκτυο από την ESRI με τη μορφή [Τεχνική Περιγραφή](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) και επεξεργάζεται λεπτομερώς τη συνολική δομή του αρχείου. Οι πληροφορίες στο κύριο αρχείο .shp αποτελούνται από κεφαλίδες και εγγραφές. Η κεφαλίδα αρχείου σταθερού μήκους ακολουθείται από εγγραφές μεταβλητού μήκους όπου κάθε εγγραφή αποτελείται από μια κεφαλίδα εγγραφής σταθερού μήκους ακολουθούμενη από περιεχόμενα εγγραφής μεταβλητού μήκους.

### Κύρια κεφαλίδα αρχείου SHP

Η κύρια κεφαλίδα αρχείου ξεκινά από την αρχή του αρχείου και έχει μήκος 100 byte. Η οργάνωση αυτής της κύριας κεφαλίδας αρχείου μαζί με τη θέση, την τιμή, τον τύπο και τη σειρά των byte είναι όπως φαίνεται στον παρακάτω πίνακα.


|Byte|Πεδίο|Τιμή|Τύπος|Σειρά byte
---|---|---|---|---|
|0-3|Κωδικός αρχείου|9994|Ακέραιος|Big Endian
|4-23|Αχρησιμοποίητο|0|Ακέραιος|Big Endian
|24-27|Μήκος αρχείου|Μήκος αρχείου|Ακέραιος|Big Endian
|28-31|Έκδοση|1000|Ακέραιος|Little Endian
|32-35|Τύπος Σχήματος|Τύπος Σχήματος|Ακέραιος|Μικρός Ενδια
|36-67|Ελάχιστο Οριοθετημένο Ορθογώνιο|Xmin, Ymin, Xmax και Ymax|διπλό|Little Endian
|68-83|Bounding Box|Zmin, Zmax|double|Little Endian
|84-99|Bounding Box|Mmin, Mmax|διπλό|

Πρέπει να σημειωθεί ότι η τιμή του μήκους του αρχείου είναι το συνολικό μήκος του αρχείου σε λέξεις 16-bit που περιλαμβάνει επίσης τις πενήντα λέξεις των 16-bit που αποτελούν την κεφαλίδα.

#### Τύποι σχήματος

Οι τιμές των πεδίων τύπων σχήματος στον παραπάνω πίνακα είναι οι εξής:


|Τιμή|Τύπος σχήματος
---|---|
|0|Μηδενικό σχήμα
|1|Σημείο
|3|Πολυγραμμή
|5|Πολύγωνο
|8|Πολυσημείο
|11|ΣημείοΖ
|13|PolyLineZ
|15|ΠολύγωνοΖ
|18|MultiPointZ
|21|ΣημείοΜ
|23|PolyLineM
|25|ΠολύγωνοΜ
|28|ΠολυσημείοΜ
|31|MultiPatch

### Αρχεία δεδομένων ###

Η κεφαλίδα του κύριου αρχείου ακολουθείται από εγγραφές μεταβλητού μήκους όπου κάθε εγγραφή αποτελείται από μια κεφαλίδα εγγραφής σταθερού μήκους ακολουθούμενη από περιεχόμενα εγγραφής μεταβλητού μήκους.

#### Κεφαλίδα εγγραφής ####

Η κεφαλίδα εγγραφής περιέχει πληροφορίες σχετικά με τον αριθμό εγγραφής και το μήκος περιεχομένου της εγγραφής σε σταθερό μήκος 8 byte. Η οργάνωση της κεφαλίδας εγγραφής είναι όπως φαίνεται παρακάτω:


|Byte|Πεδίο|Τιμή|Τύπος|Σειρά byte
---|---|---|---|---|
|0-3|Αριθμός εγγραφής|Αριθμός εγγραφής|Ακέραιος|Μεγάλος
|4-7|Μήκος εγγραφής|Μήκος εγγραφής|Ακέραιος|Μεγάλος

#### Περιεχόμενα εγγραφής ####

Τα περιεχόμενα εγγραφής ενός αρχείου σχήματος αποτελούνται από έναν τύπο σχήματος που ακολουθείται από τα γεωμετρικά δεδομένα για αυτό το σχήμα. Ένας τύπος σχήματος 0 αντιπροσωπεύει ένα μηδενικό σχήμα που δεν έχει γεωμετρικά δεδομένα για το σχήμα. Το μήκος των περιεχομένων της εγγραφής αντανακλά τα μέρη του σχήματος και τις κορυφές. Ας πάρουμε ένα παράδειγμα τύπου Point Shape για να επεξεργαστούμε πώς μια εγγραφή περιέχει πληροφορίες σχετικά με έναν τέτοιο τύπο σχήματος.

Ένα σημείο αντιπροσωπεύει μια συγκεκριμένη γεωγραφική θέση με τη σειρά X,Y όπου κάθε συντεταγμένη αντιπροσωπεύεται από μια τιμή διπλής ακρίβειας. Ο παρακάτω πίνακας δείχνει τη διάταξη ενός τύπου σχήματος σημείου.


|Byte|Τύπος σχήματος|Τιμή|Τύπος|Αριθμός|Σειρά byte
---|---|---|---|---|---|
|0-3|Τύπος σχήματος|1|Ακέραιος|1|Μικρός
|4-11|X|X|διπλό|1|Μικρό
|12-19|Y|Y|διπλό|1|Μικρό

Παραδείγματα άλλων τύπων σχημάτων μπορείτε να βρείτε στο έγγραφο τεχνικής περιγραφής της ESRI.

## Βιβλιογραφικές αναφορές ##

* [Τεχνική περιγραφή ESRI Shapefile](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) από την ESRI
