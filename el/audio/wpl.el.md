{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl αρχείο", "επέκταση", "μορφή", "τι είναι ένα αρχείο wpl", "μουσική", "μορφή αρχείου wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου WPL και τα API που μπορούν να δημιουργήσουν, να μετατρέψουν και να ανοίξουν αρχεία WPL.",
  "title" :"WPL - Αρχείο λίστας αναπαραγωγής Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Τι είναι ένα αρχείο WPL;

Ένα αρχείο με επέκταση .wpl περιέχει τη λίστα αναπαραγωγής των τραγουδιών που θα εκτελεστούν στο Microsoft Windows Media Player. Αυτά τα αρχεία δημιουργούνται συνήθως από χρήστες για τις συλλογές βίντεο και ήχου τους. Το περιεχόμενο που είναι γραμμένο σε ένα αρχείο WPL, είναι απλώς διαδρομές καταλόγου ή θέσεις για τα αρχεία πολυμέσων που έχουν επιλεγεί από τον δημιουργό του αρχείου .wpl, ώστε η εφαρμογή αναπαραγωγής πολυμέσων να μπορεί να βρει και να αναπαράγει αμέσως το περιεχόμενο πολυμέσων από τις θέσεις του καταλόγου τους.

## Μορφή αρχείου WPL

Το WPL (Windows Media Player Playlist) είναι μια ιδιόκτητη μορφή αρχείου που χρησιμοποιείται στις εκδόσεις 9 ή μεταγενέστερες του Microsoft Windows Media Player. Είναι μια μορφή αρχείου υπολογιστή που αποθηκεύει λίστες αναπαραγωγής πολυμέσων. Από προεπιλογή, η λίστα αναπαραγωγής αποθηκεύεται με μια επέκταση .wpl (Windows Media Player Playlist). Μπορείτε να χρησιμοποιήσετε την επέκταση [.m3u](/el/audio/m3u/), Αν θέλετε να αναπαράγετε τους δίσκους δεδομένων σας σε μια συσκευή που δεν υποστηρίζει αυτήν την επέκταση. Τα στοιχεία ενός αρχείου WPL αντιπροσωπεύονται σε μορφή XML.

Το στοιχείο ανώτατου επιπέδου "smil" προσδιορίζει ότι τα στοιχεία του αρχείου ακολουθούν τη δομή συγχρονισμένης γλώσσας ολοκλήρωσης πολυμέσων (SMIL). Το αρχείο δημιουργείται και αποθηκεύεται με την επέκταση .wpl και ο τύπος MIME του είναι application/vnd.ms-wpl.

### Παράδειγμα WPL

Ακολουθεί ένα παράδειγμα αρχείου wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Βιβλιογραφικές αναφορές ##

* [MPEG-1 Audio Layer II - By Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

