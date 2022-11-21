{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB Navigation Control XML File", "extension", "format", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου αρχείου XML Control (NCX) EPUB Navigation Control και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία NCX.",
  "title" :"NCX - Αρχείο XML Ελέγχου Πλοήγησης EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Τι είναι ένα αρχείο NCX; ##

Το αρχείο NCX συντομογραφείται ως αρχείο ελέγχου πλοήγησης για XML, που συνήθως ονομάζεται toc.ncx. Αυτό το αρχείο αποτελείται από τον ιεραρχικό πίνακα περιεχομένων για ένα αρχείο EPUB. Η προδιαγραφή για το NCX αναπτύχθηκε για Digital Talking Book (DTB) και αυτή η μορφή αρχείου διατηρείται από την **DAISY Consortium** και δεν αποτελεί μέρος της προδιαγραφής EPUB. Το αρχείο NCX περιλαμβάνει έναν τύπο mime **εφαρμογής/x-dtbncx+xml** σε αυτό.

## Προδιαγραφές NCX ##

Το αρχείο NCX περιέχει διάφορα είδη ετικετών XML. Οι μετα-ετικέτες όπως `meta name="dtb:uid"` χρησιμοποιούνται για την αναφορά του αναγνωριστικού. Το στοιχείο `meta name="dtb:depth"` ορίζεται ίσο με το βάθος του στοιχείου ετικέτας `navMap`. Τα στοιχεία `navPoint` μπορούν να ενσωματωθούν για να δημιουργήσουν έναν ιεραρχικό πίνακα περιεχομένων. Το περιεχόμενο του `navLabel` είναι το κείμενο που εμφανίζεται στον πίνακα περιεχομένων που δημιουργείται από συστήματα ανάγνωσης που χρησιμοποιούν το .ncx. Το περιεχόμενο του στοιχείου `navPoint` οδηγεί σε ένα έγγραφο περιεχομένου που παρατίθεται στη δήλωση και μπορεί επίσης να περιλαμβάνει ένα αναγνωριστικό στοιχείου

Μια περιγραφή ορισμένων εξαιρέσεων στην προδιαγραφή NCX όπως χρησιμοποιείται στο EPUB. Εδώ μπορείτε να δείτε το παράδειγμα ενός αρχείου NCX:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## Βιβλιογραφικές αναφορές ##

* [EPUB Από τη Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Τι αρχεία να συμπεριληφθούν στο toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

