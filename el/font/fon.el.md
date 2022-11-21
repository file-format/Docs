{
  "date" : "2020-08-20",
  "keywords" :[ "αρχείο fon", "μορφή αρχείου fon", "τι είναι ένα αρχείο fon", "αρχείο", "παράδειγμα fon", "επέκταση αρχείου fon", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Αρχείο βιβλιοθήκης γραμματοσειρών",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου FON και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Τι είναι ένα αρχείο FON;

Ένα αρχείο με επέκταση .fon είναι μια βιβλιοθήκη γραμματοσειρών των Microsoft Windows 3.x που είναι στην πραγματικότητα ένα εκτελέσιμο αρχείο αλλά μετονομάστηκε σε .fon. Είναι μια συλλογή αρχείων [.fnt](/el/font/fnt/) από μόνη της και οι εφαρμογές το αναφέρουν κατά την πρόσβαση στη γραμματοσειρά συστήματος. Αυτός είναι ο λόγος που λειτουργεί ως αρχείο πόρων. Μπορεί να ανοίξει σε λειτουργικό σύστημα Windows χρησιμοποιώντας την εφαρμογή Microsoft Windows Font View.

## Μορφή αρχείου FON

Ένα αρχείο FON περιέχει πόρους γραμματοσειράς και έχει μορφή αρχείου Resource (.res). Η μορφή αρχείου .res καθορίζει την κεφαλίδα του αρχείου καθώς και τις προδιαγραφές της ενότητας δεδομένων. Το .fnt είναι επίσης ένα αρχείο δεδομένων πόρων που περιλαμβάνεται σε ένα αρχείο πόρων. Τα αρχεία FON έχουν δυαδική μορφή αρχείου και έχουν τύπο MIME εφαρμογής/οκτάδας ροής.

Οι πόροι γραμματοσειρών, σε αντίθεση με άλλους τύπους πόρων, δεν προστίθενται στους πόρους μιας εφαρμογής. Αντίθετα, προστίθενται στα αρχεία EXE και μετονομάζονται σε αρχεία .fon, με αποτέλεσμα να δημιουργούνται αρχεία βιβλιοθήκης αντί για εφαρμογές. Πολλαπλές μεμονωμένες γραμματοσειρές αποτελούν στοιχεία μιας ομάδας γραμματοσειρών όπου κάθε ομάδα ακολουθεί μια δομή ομάδας πόρων. Οι πόροι γραμματοσειρών χρησιμοποιούν αυτές τις δομές ομάδας πόρων. Η κεφαλίδα της ομάδας έχει όλες τις πληροφορίες που απαιτούνται για την πρόσβαση σε μια συγκεκριμένη γραμματοσειρά από την ομάδα. Ένας πόρος στοιχείου γραμματοσειράς έχει την ακόλουθη μορφή.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/el/font/fnt/) file)
```
Ένα μεμονωμένο αρχείο πόρων .rc μπορεί να έχει μικτές δηλώσεις πόρων. Οι ομάδες γραμματοσειρών μπορούν να βρίσκονται οπουδήποτε στο αρχείο πόρων και δεν χρειάζεται να είναι γειτονικές. Είναι απαραίτητο για τα προγράμματα που δημιουργούν αρχεία .RES να προσθέσουν χειροκίνητη καταχώρηση του FONTDIR. Ακολουθεί η δομή της κεφαλίδας ομάδας.

```
[Κανονική κεφαλίδα πόρων (τύπος = 7)]

WORD NumberOfFonts; // Συνολικός αριθμός στο αρχείο .RES
```     
The remaining data is repeated for every font in the .RES file.

```
γραμματοσειρά WORDOrdinal;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPoints;
WORD dfVertRes;
WORD dfHorizRes;
WORD dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfItalic;
BYTE dfΥπογράμμιση;
BYTE dfStrikeOut;
WORD dfWeight;
BYTE dfCharSet;
WORD dfPixWidth;
WORD dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfAvgWidth;
WORD dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD dfReserved;
char szΌνομα συσκευής[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

