{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Αρχείο εικονικής επαφής",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου VCF και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο VCF;

Το VCF (Virtual Card Format) ή vCard είναι μια ψηφιακή μορφή αρχείου για την αποθήκευση στοιχείων επικοινωνίας. Η μορφή χρησιμοποιείται ευρέως για την ανταλλαγή δεδομένων μεταξύ δημοφιλών εφαρμογών ανταλλαγής πληροφοριών. Τα περισσότερα λειτουργικά συστήματα όπως τα Windows και το MacOS διαθέτουν προεπιλεγμένες εφαρμογές για τη δημιουργία και το άνοιγμα αυτών των αρχείων. Ένα μόνο αρχείο VCF μπορεί να περιέχει στοιχεία επικοινωνίας για μία ή πολλές επαφές. Ένα αρχείο VCF συνήθως περιέχει πληροφορίες όπως το όνομα της επαφής, τη διεύθυνση, τον αριθμό τηλεφώνου, το email, τα γενέθλια, τις φωτογραφίες και τον ήχο εκτός από έναν αριθμό άλλων πεδίων. Υποστηριζόμενο από προγράμματα-πελάτες και υπηρεσίες email, δεν υπάρχει απώλεια δεδομένων κατά τη μεταφορά των επαφών μέσω της χρήσης της μορφής vCard. Ο τύπος μέσου για τη μορφή αρχείου VCF είναι text/vcard.

## Μορφή αρχείου VCF

Τα αρχεία VCF είναι από τη φύση τους κειμενικά και είναι αναγνώσιμα από τον άνθρωπο. Αυτά μπορούν να ανοίξουν σε προγράμματα επεξεργασίας κειμένου όπως το Σημειωματάριο στα Microsoft Windows και το TextEdit σε MacOS. Ωστόσο, εάν υπάρχει μια εικόνα στο αρχείο, δεν θα εμφανίζεται στο πρόγραμμα επεξεργασίας κειμένου.

Το [Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) παρέχει υποστήριξη για άνοιγμα αρχείων VCF καθώς και μετατροπή σε μια σειρά από άλλες μορφές, όπως η δημοφιλής μορφή [MSG](/el/email/msg/). Η μορφή αρχείου VCF βελτιώθηκε με το χρόνο από την έκδοση 2.1 έως την 4.0 προσθέτοντας λεπτομερείς πληροφορίες στη μορφή αρχείου. Η μορφή χρησιμοποιείται επίσης για εξαγωγή επαφών τηλεφώνου και αργότερα εισαγωγή σε άλλη συσκευή.

{{< figure src="../VCF.png" alt="Μορφή αρχείου VCF" >}}

### VCF 2.1 Παράδειγμα

Ακολουθεί ένα παράδειγμα της έκδοσης 2.1.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### Παράδειγμα VCF 3.0

Ακολουθεί ένα παράδειγμα της έκδοσης 3.0.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### Παράδειγμα VCF 4.0

Ακολουθεί ένα παράδειγμα της έκδοσης 4.0.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## βιβλιογραφικές αναφορές

* [VCF - Από τη Wikipedia](https://en.wikipedia.org/wiki/VCard)

