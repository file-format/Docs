{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "file", "extension", "format", "what is mod file format", "music", "mod file format", "mod vs MP3", "mod file format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου MOD και τα API που μπορούν να δημιουργήσουν, να μετατρέψουν και να ανοίξουν αρχεία MOD.",
  "title" :"MOD - Αρχείο ενότητας μουσικής",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Τι είναι ένα αρχείο MOD;
Ένα αρχείο με επέκταση .mod είναι ένα αρχείο μονάδας μουσικής που δημιουργήθηκε χρησιμοποιώντας την τυπική μορφή ενότητας μουσικής, η οποία βασίζεται στη μορφή **Amiga module** που αναπτύχθηκε από τον Karsten Obarski και κυκλοφόρησε με το λογισμικό **Ultimate Soundtracker** για το Commodore Σύστημα Amiga. Παρόμοια με ένα αρχείο [MIDI](/el/audio/mid/), αποτελείται από μοτίβα νότων και δείγματα ήχου, που αντιπροσωπεύουν διαφορετικά όργανα που αναπαράγονται σύμφωνα με τις νότες. Τα αρχεία MOD χρησιμοποιούνται ιδιαίτερα σε βιντεοπαιχνίδια ως μουσική υπόκρουση και στην υποκουλτούρα τέχνης του υπολογιστή **demoscene**.

## Μορφή αρχείου MOD

Το MOD είναι μια μορφή αρχείου υπολογιστή που χρησιμοποιείται η βασική του λειτουργία είναι να αναπαριστά μουσική και ήταν η πρώτη μορφή αρχείου ενότητας. Τα αρχεία MOD χρησιμοποιούν την επέκταση αρχείου .mod, εκτός από το **Amiga** που διαβάζει την κεφαλίδα ενός αρχείου για να καθορίσει τον τύπο αρχείου, επομένως δεν βασίζεται σε επεκτάσεις ονόματος αρχείου. Ένα αρχείο MOD αποτελείται από ένα σύνολο διαφόρων οργάνων με τη μορφή δειγμάτων, έναν αριθμό μοτίβων που καθορίζουν πώς και πότε θα παιχτούν τα δείγματα και μια λίστα με ποια μοτίβα θα παιχτούν με ποια σειρά.

### Προδιαγραφές μορφής αρχείου MOD

Ένα μοτίβο αρχείου MOD είναι στην πραγματικότητα σχεδιασμένο σε μια διεπαφή χρήστη sequencer ως πίνακας με μία στήλη ανά κανάλι. Επομένως, αυτός ο πίνακας έχει τέσσερις στήλες (μία για κάθε κανάλι υλικού Amiga. Κάθε στήλη έχει 64 σειρές).

Ένα κελί στον πίνακα μπορεί να προκαλέσει μια από τις ακόλουθες ενέργειες να συμβεί στο κανάλι της στήλης του όταν φτάσει η ώρα της σειράς του:

- Ξεκινήστε ένα όργανο παίζοντας μια νέα νότα σε αυτό το κανάλι σε μια δεδομένη ένταση, πιθανώς με ένα ειδικό εφέ σε αυτό
- Αλλάξτε την ένταση ή το ειδικό εφέ που εφαρμόζεται στην τρέχουσα σημείωση
- Αλλαγή ροής μοτίβου. μεταβείτε σε μια συγκεκριμένη θέση τραγουδιού ή μοτίβου ή βρόχο μέσα σε ένα μοτίβο
- Μην κάνεις τίποτα; οποιαδήποτε υπάρχουσα νότα που παίζει σε αυτό το κανάλι θα συνεχίσει να παίζει

Ένα όργανο είναι ένα μεμονωμένο δείγμα μαζί με μια προαιρετική προδιαγραφή του οποίου τμήμα του δείγματος μπορεί να επαναληφθεί για να κρατήσει μια σταθερή νότα.

### Χρονοδιάγραμμα
Το ελάχιστο χρονικό πλαίσιο ήταν 0,02 δευτερόλεπτα στο αρχικό αρχείο MOD ή ένα διάστημα "κάθετου κενού" (VSync), επειδή το αρχικό λογισμικό χρησιμοποιούσε το χρονισμό VSync της οθόνης που εκτελούσε τα 50 Hz (για PAL) ή 60 Hz (για NTSC) για χρονισμό.

## βιβλιογραφικές αναφορές

* [MOD (μορφή αρχείου) - Από τη Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))

