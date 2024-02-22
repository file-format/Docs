{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Αρχείο MPK - Μορφή αρχείου πακέτου χάρτη ArcGIS",
  "description":"Μάθετε για τη μορφή αρχείου MPK και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-el",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Τι είναι ένα αρχείο MPK;

Ένα αρχείο MPK είναι ένα αρχείο πακέτου χάρτη ArcGIS που δημιουργείται με το ArcGIS. Περιέχει ένα έγγραφο χάρτη .mxd και σχετικά δεδομένα. Επιπλέον, περιέχει πρόσθετες πληροφορίες, όπως επίπεδα αναφοράς, σύμβολα και άλλους πόρους. Το αρχείο MPK χρησιμοποιείται για την κοινή χρήση χαρτών και δεδομένων με άλλους χρήστες. Αυτό εξαλείφει τη διαθεσιμότητα άλλων που έχουν την αρχική πηγή δεδομένων και βοηθά επίσης στη διανομή χαρτών που θα χρησιμοποιηθούν σε φορητή συσκευή.

## Μορφή αρχείου MPX

Οι λεπτομέρειες της εσωτερικής μορφής αρχείου των αρχείων MPX δεν είναι διαθέσιμες δημόσια για αναφορά του προγραμματιστή.

### Δημιουργία αρχείου MPK χρησιμοποιώντας ArcGIS

Τα αρχεία MPK μπορούν να δημιουργηθούν χρησιμοποιώντας το ArcGIS. Η επιλογή Κοινή χρήση ως στο μενού Πακέτο χάρτη μπορεί να χρησιμοποιηθεί για τη δημιουργία ενός αρχείου .mpk που περιέχει το έγγραφο του χάρτη και όλα τα αναφερόμενα δεδομένα και πόρους του. Αυτό το αρχείο MPK μπορεί στη συνέχεια να μοιραστεί με άλλους και μπορεί να ανοίξει στο ArcMap και στο ArcGIS Pro για να προβάλετε τον χάρτη και τα δεδομένα.

### Δημιουργία αρχείου MPK χρησιμοποιώντας Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Χρήση Python για τη δημιουργία πακέτων χαρτών για όλα τα έγγραφα χάρτη σε έναν φάκελο

Ο παρακάτω κώδικας Python βρίσκει και δημιουργεί πακέτα χαρτών για όλα τα έγγραφα χάρτη που βρίσκονται σε έναν καθορισμένο φάκελο.

```
# Name: PackageMap.py
# Description:  Find all the map documents that reside in a specified folder and create map packages for each map document.

# import system modules
import os
import arcpy

# Set environment settings
arcpy.env.overwriteOutput = True
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing"

# Loop through the workspace, find all the mxds and create a map package using the same name as the mxd
for mxd in arcpy.ListFiles("*.mxd"):
    print ("Packaging: {0}".format(mxd))
    arcpy.PackageMap_management(mxd, os.path.splitext(mxd)[0] + '.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```

## βιβλιογραφικές αναφορές

* [Χάρτης πακέτου](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


