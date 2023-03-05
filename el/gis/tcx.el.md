{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX File Format- Training Center XML File",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου TCX και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Τι είναι ένα αρχείο TCX;

Ένα αρχείο TCX (Training Center XML) είναι μια μορφή ανταλλαγής δεδομένων που χρησιμοποιείται για την κοινή χρήση δεδομένων μεταξύ συσκευών γυμναστικής. Παρουσιάστηκε το 2008 με το προϊόν Garmin's Training Center. Τα δεδομένα προπόνησης όπως ο καρδιακός ρυθμός, ο ρυθμός τρεξίματος, ο ρυθμός ποδηλάτου, οι θερμίδες και ο χρόνος γύρου αποθηκεύονται σε μορφή [XML](/el/web/xml/) μέσα στο αρχείο TCX. Επιπλέον, περιληπτικά δεδομένα σχετικά με το κομμάτι προπόνησης περιλαμβάνονται επίσης στο αρχείο TCX. Τα αρχεία TCX είναι παρόμοια με τα αρχεία [FIT](/el/gis/fit/) που δημιουργούνται με φορητές συσκευές Garmin Sports.

## Μορφή αρχείου TCX - Περισσότερες πληροφορίες

Τα αρχεία TCX αποθηκεύονται στο δίσκο ως αρχεία XML με κάθε εγγραφή να αποθηκεύεται ως δραστηριότητα. Μια δραστηριότητα περιλαμβάνει όλα τα δεδομένα μιας προπόνησης, όπως χρόνος, χρόνος γύρου, αναγνωριστικό, καρδιακός ρυθμός, ένταση, ρυθμός και πληροφορίες κομματιού που περιέχουν τα ζεύγη θέσεων μαζί με τη χρονική σήμανση για αυτήν τη θέση lat-long παρόμοια με το [GPX](/el/gis/gpx/) αρχεία.

### Εκδόσεις μορφής αρχείου TCX

Υπάρχουν δύο εκδόσεις αυτής της μορφής με τα δικά τους σχήματα XML που φιλοξενούνται από την Garmin. Ακολουθούν μερικά από αυτά:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Πρωτόκολλο δεδομένων TCX

Μια γρήγορη έκδοση της μορφής TCX XML είναι διαθέσιμη στο Github ως [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Βιβλιογραφικές αναφορές ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

