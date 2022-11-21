---
date: 2022-03-20
keywords: mxl, μορφή αρχείου Musepack, επέκταση .mxl
συγγραφέας:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Μάθετε για τη μορφή αρχείου MXL και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MXL."
title: Μορφή αρχείου MXL - Συμπιεσμένο αρχείο MusicXML
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Τι είναι ένα αρχείο MXL;

Ένα αρχείο MXL είναι η συμπιεσμένη μορφή της μορφής αρχείου MusicXML που είναι μια ανοιχτή τυπική μορφή για την ανταλλαγή ψηφιακών παρτιτούρων. Τα αρχεία MusicXML απλού κειμένου έχουν μεγάλο μέγεθος και η χρήση τέτοιων αρχείων ως μορφή διανομής φύλλων επηρεάστηκε από το μεγάλο μέγεθος αρχείου. Αυτό το ζήτημα αντιμετωπίστηκε με το [MusicXML](https://www.musicxml.com/) 2.0 με την εισαγωγή της μορφής αρχείου MXL που συμπιέζει τα αρχεία αρκετά ώστε να μειώνει το μέγεθος του αρχείου παρόμοιο με αυτό των αρχικών αρχείων MIDI. Ο προτεινόμενος τύπος πολυμέσων για αρχεία MXL είναι application/vnd.recordare.musicxml.

## Μορφή αρχείου MXL

Τα αρχεία MXL αποθηκεύονται ως αρχεία [ZIP](/el/compression/zip/) συμπιεσμένα [XML](/el/web/xml/) με επέκταση αρχείου .mxl. Τα αρχεία MXL συμπιέζονται με τον αλγόριθμο DEFLATE όπως ορίζεται στο [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### Δομή αρχείου MXL

Κάθε αρχείο MXL έχει μια μορφή XML που βασίζεται σε ZIP που πρέπει να έχει ένα αρχείο META-INF/container.xml που περιγράφει το σημείο εκκίνησης της έκδοσης MusicXML του αρχείου. Δεν έχει οριστεί αντίστοιχο αρχείο .xsd για τη μορφή αρχείου MXL.

Ένα απλό αρχείο container.xml έχει τα ακόλουθα περιεχόμενα. Αυτό το παράδειγμα προέρχεται από το αρχείο Dichterliebe01.mxl που είναι διαθέσιμο στον ιστότοπο του MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Σε αυτό το παράδειγμα, το<container> στοιχείο είναι το στοιχείο εγγράφου. ο<rootfiles> στοιχείο μπορεί να περιέχει ένα ή περισσότερα<rootfile> στοιχεία, με την πρώτη<rootfile> στοιχείο που περιγράφει τη ρίζα MusicXML. Ένα αρχείο MusicXML που χρησιμοποιείται ως α<rootfile> μπορεί να έχει<score-partwise> ,<score-timewise> , ή<opus> ως στοιχείο εγγράφου του.

## βιβλιογραφικές αναφορές

* [Συμπιεσμένα αρχεία MXL](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

