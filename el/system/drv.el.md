{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "επέκταση", "αρχείο", "μορφή", "σύστημα", "Πρόγραμμα οδήγησης", "Πρόγραμμα οδήγησης συσκευής Windows", "προγράμματα", "υπολογιστής", "εφαρμογή" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Πρόγραμμα οδήγησης συσκευής Windows",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου DRV και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Τι είναι ένα αρχείο DRV; ##

Τα αρχεία με επέκταση .drv ανήκουν στο πρόγραμμα οδήγησης συσκευής των Windows. Το λειτουργικό σύστημα Windows χρησιμοποιεί αυτά τα αρχεία για τη σύνδεση εσωτερικών και εξωτερικών σκληρών συσκευών. Τα αρχεία DRV αποτελούνται από οδηγίες και παραμέτρους για το πώς μια συσκευή και το λειτουργικό σύστημα συνδέονται μεταξύ τους. Αυτά τα αρχεία βοηθούν στην εγκατάσταση προγραμμάτων οδήγησης συσκευών για σωστή λειτουργία με τα Windows. Επίσης, οι συσκευές που συνδέονται με τη μητρική πλακέτα του υπολογιστή μέσω διαύλου ή καλωδίου απαιτούν αρχεία DRV.


## Μορφή αρχείου DRV ##

Τα αρχεία DRV συνήθως συσκευάζονται ως δυναμικές βιβλιοθήκες (αρχεία [DDL](/el/system/dll/) ή αρχεία [EXE](/el/εκτελέσιμα/exe/). Αυτά τα αρχεία μπορούν να υποστηριχθούν σε όλες τις πλατφόρμες συστήματος, όπως smartphone, και δεν υπάρχει καμία διασφάλιση ότι κάθε πλατφόρμα θα υποστηρίξει σωστά αυτά τα αρχεία. Ωστόσο, ορισμένες πιο συνηθισμένες συσκευές που χρησιμοποιούν την επέκταση αρχείου .drv είναι:

* Κάρτες ήχου
* Κάρτες γραφικών
* Εκτυπωτές
* Συσκευές αποθήκευσης
* Προσαρμογείς δικτύου
* Εξαρτήματα υλικού υπολογιστών

Συνιστάται να μην ανοίγετε αρχεία DRV που αποστέλλονται μέσω email, επειδή αυτή η μορφή αρχείου περιέχει ιούς και άλλα κακόβουλα προγράμματα. Βεβαιωθείτε ότι έχετε πραγματοποιήσει μια ολοκληρωμένη σάρωση πριν ανοίξετε οποιοδήποτε άγνωστο αρχείο DRV.


## Παράδειγμα DRV ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

