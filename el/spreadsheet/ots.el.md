{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "αρχείο", "επέκταση", "μορφή αρχείου", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου OTS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία OTS.",
  "title" :"OTS - Μορφή αρχείου προτύπου υπολογιστικού φύλλου OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Τι είναι ένα αρχείο OTS;

Ένα αρχείο με επέκταση .ots είναι ένα αρχείο προτύπου υπολογιστικού φύλλου OpenDocument που δημιουργείται με το λογισμικό εφαρμογής Calc που περιλαμβάνεται στο Apache OpenOffice. Το λογισμικό εφαρμογής Calc είναι παρόμοιο με το Excel που διατίθεται στο Microsoft Office. Η μορφή αρχείου OTS χρησιμοποιείται για τη δημιουργία προτύπων που περιέχουν προκαθορισμένες ρυθμίσεις που σχετίζονται με στυλ, γραμματοσειρά, δεδομένα, διάταξη υπολογιστικού φύλλου και μορφοποίηση. Τα αρχεία OTF έχουν "mime-type application/vnd.oasis.opedocument.spreadsheet-template". Αυτά τα αρχεία προτύπων μπορούν να χρησιμοποιηθούν ως αφετηρία για τη δημιουργία και αποθήκευση πραγματικών αρχείων δεδομένων που είναι αποθηκευμένα σε [μορφή αρχείου ODS](/el/spreadsheet/ods/). Τα αρχεία OTS μπορούν να χρησιμοποιηθούν με εφαρμογές όπως το OpenOffice και το LibreOffice.

## Μορφή αρχείου OTS

Τα αρχεία OTS αποθηκεύονται σε μορφή αρχείου που βασίζεται σε OpenDocument XML του OASIS που αποτελείται από μια συλλογή πολλών δευτερευόντων εγγράφων με ένα πακέτο ως αρχείο [ZIP](/el/compression/zip/). Κάθε αρχείο zip αποθηκεύει μέρος του πλήρους εγγράφου και κάθε δευτερεύον έγγραφο αποθηκεύει μια συγκεκριμένη πτυχή του εγγράφου. Για παράδειγμα, ένα δευτερεύον έγγραφο περιέχει τις πληροφορίες στυλ και ένα άλλο δευτερεύον έγγραφο περιέχει το περιεχόμενο του εγγράφου. Ένα τυπικό έγγραφο ODF έχει τα ακόλουθα στοιχεία:

### OTS Content.xml

Το αρχείο content.xml περιέχει το πραγματικό περιεχόμενο του εγγράφου. Ωστόσο, αυτό δεν περιλαμβάνει δυαδικά δεδομένα, όπως εικόνες.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml της μορφής αρχείου OTS

Το αρχείο styles.xml περιέχει πληροφορίες στυλ και χρησιμοποιείται σε μεγάλο βαθμό για μορφοποίηση και διάταξη. Οι τύποι στυλ περιλαμβάνουν:

* Στυλ παραγράφου
* Στυλ σελίδας
* Στυλ χαρακτήρων
* Στυλ πλαισίων
* Λίστα στυλ

### Meta.xml

Το αρχείο meta.xml περιέχει πληροφορίες σχετικά με τα μεταδεδομένα του αρχείου, όπως Συγγραφέας, Ημερομηνία Τελευταία Τροποποίησης κ.λπ.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

Το αρχείο `settings.xml` περιλαμβάνει ρυθμίσεις σε επίπεδο εγγράφου όπως ο συντελεστής ζουμ και η θέση του δρομέα.

## Βιβλιογραφικές αναφορές ##

* [Προδιαγραφή OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

