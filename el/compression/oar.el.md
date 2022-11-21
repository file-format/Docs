{
  "date" : "2021-04-08",
  "keywords" :[ "αρχείο oar", "μορφή αρχείου oar", "τι είναι αρχείο oar", "αρχείο", "παράδειγμα oar", "επέκταση αρχείου oar", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - Μορφή αρχείου αρχείου OpenSimulator",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου OAR και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Τι είναι ένα αρχείο OAR;

Ένα αρχείο με επέκταση .oar είναι ένα αρχείο αρχειοθέτησης που χρησιμοποιείται από την εφαρμογή OpenSimulator που είναι ένας διακομιστής εφαρμογών 3D ανοιχτού κώδικα για τη δημιουργία ενός εικονικού περιβάλλοντος προσβάσιμου σε πολλούς χρήστες μέσω του δικτύου. Η μορφή αρχείου OAR παρέχει τα απαραίτητα δεδομένα περιουσιακών στοιχείων που απαιτούνται για την πλήρη φόρτωση του εδάφους, των υφών αντικειμένων και των αποθεμάτων σε ένα διαφορετικό σύστημα. Το OpenSimulator διαθέτει επίσης προαιρετικό υπερδίκτυο που επιτρέπει στους χρήστες να επισκέπτονται άλλες εγκαταστάσεις OpenSimulator σε ολόκληρο τον ιστό. Τα αρχεία OAR έχουν εφαρμογή/κουπί τύπου MIME και περιέχουν ένα ή περισσότερα αρχειοθετημένα αρχεία.


## Μορφή αρχείου OAR

Το OAR είναι δυαδικά αρχεία που αποθηκεύονται σε συμπιεσμένη μορφή αρχείου. Η πιο πρόσφατη έκδοση της μορφής αρχείου OAR είναι [έκδοση 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) που έχει σημαντικές αλλαγές από την προηγούμενη [έκδοση 0.8](http://opensimulator.org/wiki/OAR_Format_0 .8). Η πιο πρόσφατη έκδοση υποστηρίζει την αποθήκευση πολλών περιοχών σε ένα μόνο OAR και δεν είναι συμβατή με τις εκδόσεις του OpenSimulator πριν από την 0.7.5. Ένα αρχείο OAR είναι ένα αρχείο tar με μορφή gzip (tar.gz) στην αρχική μορφή unix tar (όχι USTAR).

## Παράδειγμα περιοχών OAR
Τα αρχεία AOR μπορούν να περιέχουν πολλές περιοχές. Η δομή του αρχείου είναι η εξής (αυτό το παράδειγμα περιέχει 4 περιοχές):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

Το αρχείο ελέγχου αρχειοθέτησης περιέχει έναν κύριο αριθμό έκδοσης για τον καθορισμό της συμβατότητας με μελλοντικές αλλαγές μορφής. Η παρουσία στοιχείων σε μορφή OAR υποδεικνύεται από το boolean στοιχείο<assets_included> . Οι πληροφορίες σχετικά με τις περιοχές που περιλαμβάνονται περιέχονται σε ένα μανιφέστο που υπάρχει στο αρχείο ελέγχου. Ένα παράδειγμα του Archive.xml είναι το ακόλουθο.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## βιβλιογραφικές αναφορές

* [Μορφή OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

