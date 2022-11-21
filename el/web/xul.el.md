{
  "date" : "2021-05-24",
  "keywords" :["xul", "File", "Extension", "File Format", "File Extension", "XML User Interface Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - Αρχείο γλώσσας διεπαφής χρήστη XML",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου XUL και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Τι είναι ένα αρχείο XUL;

Ένα αρχείο με επέκταση .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) σημαίνει XML User Interface Language) είναι ένα αρχείο γλώσσας σήμανσης που βασίζεται σε [XML](/el/web/xml/) για δημιουργία διεπαφών χρήστη. Αναπτύχθηκε από τη Mozilla για προγραμματιστές να δημιουργούν στοιχεία γραφικής διεπαφής χρήστη παρόμοια με άλλες γλώσσες σήμανσης που χρησιμοποιούνται για τη δημιουργία ιστοσελίδων. Το XUL χρησιμοποιείται ευρέως από τη Mozilla στο πρόγραμμα περιήγησης Firefox, όπου χρησιμοποίησε τη βάση κώδικα Mozilla. Η απόδοση XUL πραγματοποιείται χρησιμοποιώντας το
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(λογισμικό)). Τα πιρούνια Firefox όπως τα Pale Moon, Basilisk και Waterfox διατηρούν υποστήριξη για τα πρόσθετα XUL. Τα αρχεία XUL προσδιορίζονται με τύπο MIME: application/vnd.mozilla.xul+xml.

## Μορφή αρχείου XUL

Τα αρχεία XUL γράφονται σε απλό κείμενο με βάση τη μορφή αρχείου XML και αποδίδονται χρησιμοποιώντας τη μηχανή Gecko. Τα τρία κύρια μέρη μιας δομής XUL είναι:

* «Περιεχόμενο» - Περιλαμβάνει τις δηλώσεις του παραθύρου και τα στοιχεία διεπαφής χρήστη που περιέχονται σε αυτά.
* «Skin» - Περιλαμβάνει οποιαδήποτε φύλλα στυλ, εικόνες και άλλα αρχεία που σχετίζονται με θέματα. Η εμφάνιση ενός παραθύρου περιγράφεται στα φύλλα στυλ.
* «Τοπική ρύθμιση» - Το κείμενο που εμφανίζεται σε ένα παράθυρο αποθηκεύεται χωριστά και πολλαπλές ομάδες αρχείων γλώσσας μπορούν να χρησιμοποιηθούν από τους χρήστες.

### XUL Παράδειγμα

Το παρακάτω παράδειγμα δημιουργεί τρία κουμπιά που στοιβάζονται το ένα πάνω στο άλλο σε κάθετη κατεύθυνση.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## βιβλιογραφικές αναφορές

* [XUL - Από τη Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [XUL Archived Documentation - By Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

