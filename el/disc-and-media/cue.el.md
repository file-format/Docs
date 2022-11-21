{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "file", "extension", "format", "what is a cue file", "music", "cue file format", "cue file format", "cue sheet", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου CUE και τα API που μπορούν να δημιουργήσουν, να μετατρέψουν και να ανοίξουν αρχεία CUE.",
  "title" :"CUE - Αρχείο Φύλλου Cue",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Τι είναι ένα αρχείο CUE;

Ένα αρχείο με επέκταση .cue, γνωστό και ως αρχείο φύλλου cue, είναι ένα αρχείο μεταδεδομένων που περιέχει πληροφορίες σχετικά με τη διάταξη των κομματιών σε ένα CD ή DVD. Αυτά υποστηρίζονται από προγράμματα αναπαραγωγής πολυμέσων και εφαρμογές δημιουργίας οπτικών δίσκων. Τα κύρια δεδομένα ήχου που είναι αποθηκευμένα στο CD αναφέρονται από το αρχείο υπόδειξης, μαζί με τις προδιαγραφές μήκους κομματιών, τίτλων δίσκων και εκτελεστών. Έτσι, εάν ένα μεμονωμένο αρχείο ήχου περιέχει πολλά κομμάτια, το αρχείο υπόδειξης μπορεί να χρησιμοποιηθεί για να χωρίσει τον ήχο σε πολλά αρχεία ή να παραπέμψει σε διάφορα κομμάτια.

## Μορφή αρχείου CUE

Τα αρχεία CUE ή cue φύλλου αποθηκεύονται σε μορφή απλού κειμένου που είναι αναγνώσιμη από τον άνθρωπο. Οι πληροφορίες σε ένα αρχείο cue είναι εντολές με μία ή περισσότερες παραμέτρους. Αυτές οι εντολές ισχύουν είτε για ολόκληρο το αρχείο είτε για ένα μεμονωμένο κομμάτι, ανάλογα με τη συγκεκριμένη εντολή και το περιβάλλον. Ο οδηγός χρήσης CDRWIN περιγράφει τις προδιαγραφές για τη σύνταξη και τη σημασιολογία του φύλλου υπόδειξης.

## Βασικές εντολές φύλλου CUE

|Εντολή|Περιγραφή|
---|---|
|ΑΡΧΕΙΟ| Αναφέρεται στο αρχείο που περιέχει τα δεδομένα και τη μορφή του, όπως [MP3](/el/audio/mp3/), [WAV](/el/audio/wav/), ή απλή εικόνα δυαδικού δίσκου)|
|ΤΡΟΧΑ| Καθορίζει τις πληροφορίες περιβάλλοντος του κομματιού, όπως τον αριθμό και τον τύπο ή τη λειτουργία του.|
|ΕΥΡΕΤΗΡΙΟ| Αντιπροσωπεύει τη θέση ως ευρετήριο εντός του ΑΡΧΕΙΟΥ. Η μορφή είναι mm:ss:ff (λεπτό-δευτερόλεπτο-καρέ).|
|PREGAP και POSTGAP|Δηλώνει το pregap ή το post-gap ενός κομματιού, το οποίο δεν είναι αποθηκευμένο σε κανένα αρχείο δεδομένων. Το μήκος καθορίζεται στην ίδια μορφή καρέ λεπτού-δευτερόλεπτου όπως για το INDEX.|

### Παράδειγμα φύλλου CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## βιβλιογραφικές αναφορές

* [αρχείο .cda - Από τη Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

