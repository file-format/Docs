{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου FZP και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία FZP.",
  "title" :"Μορφή αρχείου FZP - Αρχείο περιγραφής τμήματος Fritzing XML",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Τι είναι ένα αρχείο FZP;

Ένα αρχείο FZP είναι ένα αρχείο XML που δημιουργήθηκε από την εφαρμογή πρωτοτύπων και σχεδίασης ηλεκτρονικών κυκλωμάτων [Fritzing](https://fritzing.org/). Περιέχει πληροφορίες σχετικά με τις ιδιότητες, τις συνδέσεις και τους διαύλους του εξαρτήματος σε μορφή αρχείου [XML](/el/web/xml/). Τα αρχεία FPZ δεν μπορούν να χρησιμοποιηθούν ανεξάρτητα στο Fritzing. Αντίθετα, εισάγονται ως μέρος του αρχείου αρχείου FZPZ.

## Μορφή αρχείου FZP - Περισσότερες πληροφορίες

Τα αρχεία FZP είναι αρχεία XML που περιέχουν πληροφορίες σχετικά με τις ιδιότητες, τις συνδέσεις και τους διαύλους του εξαρτήματος. Εκτός από αυτά, τα αρχεία FZP περιέχουν επίσης πληροφορίες σχετικά με τον τίτλο, την περιγραφή, τον συγγραφέα και την ημερομηνία δημοσίευσης του αρχείου FZP. Όταν εξάγεται ένα αρχείο τμήματος Fritzing, η εφαρμογή Fritzing δημιουργεί ένα συμπιεσμένο αρχείο [FZPZ](/el/compression/fzpz/) που περιέχει ένα αρχείο FZP και τέσσερα αρχεία [SVG](/el/image/svg/).

Οι [προδιαγραφές μορφής αρχείου FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) είναι διαθέσιμες στο Github από την Fritzing.

## Παράδειγμα δομής αρχείου FZP

Ένα τυπικό αρχείο FZP έχει την ακόλουθη δομή XML.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## βιβλιογραφικές αναφορές

* [Προδιαγραφές μορφής αρχείου FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Νέα εξαρτήματα με επέκταση fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

